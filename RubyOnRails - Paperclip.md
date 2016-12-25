<pre>
##################################################
#  NOTE FOR UPGRADING FROM 4.3.0 OR EARLIER       #
##################################################

Paperclip is now compatible with aws-sdk >= 2.0.0.

If you are using S3 storage, aws-sdk >= 2.0.0 requires you to make a few small
changes:

* You must set the `s3_region`
* If you are explicitly setting permissions anywhere, such as in an initializer,
  note that the format of the permissions changed from using an underscore to
  using a hyphen. For example, `:public_read` needs to be changed to
  `public-read`.

For a walkthrough of upgrading from 4 to 5 and aws-sdk >= 2.0 you can watch
http://rubythursday.com/episodes/ruby-snack-27-upgrade-paperclip-and-aws-sdk-in-prep-for-rails-5
</pre>

##What Needs To Change
<pre>
# Gemfile

</pre>

<b>config/env_variables.rb</b>
<pre>
ENV['AWS_REGION'] = 'us-west-2'
ENV['AWS_BUCKET_NAME'] = 'bucket-name'
ENV['AWS_ACCESS_KEY_ID'] = 'access-key-id'
ENV['AWS_SECRET_ACCESS_KEY'] = 'secret-access-key'
</pre>

<b>config/environment.rb</b>
<pre>
# Load the Rails application.
require File.expand_path('../application', __FILE__)

<b># Load the app's custom environment variables here, so that they are loaded before environments/*.rb
env_variables = File.join(Rails.root, 'config', 'env_variables.rb')
load(env_variables) if File.exists?(env_variables)
</b>
# Initialize the Rails application.
Rails.application.initialize!
</pre>

<b>config/initializers/paperclip.rb</b>
<pre>
PAPERCLIP_STORAGE_OPTS = {
  storage: :s3,
  s3_region: ENV['AWS_REGION'],
  s3_host_name: "s3-#{ENV['AWS_REGION']}.amazonaws.com",
  s3_credentials: {
    bucket: ENV['AWS_BUCKET_NAME'],
    access_key_id: ENV['AWS_ACCESS_KEY_ID'],
    secret_access_key: ENV['AWS_SECRET_ACCESS_KEY']
  }
}
</pre>

To use .url, the following needs to be used as there is an outstanding bug [Issue#2151](https://github.com/thoughtbot/paperclip/issues/2151)
<pre>
config.paperclip_defaults = { s3_host_name: "<b>s3-#{ENV['AWS_REGION']}.amazonaws.com</b>", }
</pre>

<b>There must be validation in the model!</b>

<b>app/models/sermon.rb</b>
<pre>
class Sermon < ActiveRecord::Base

  has_attached_file :clip, PAPERCLIP_STORAGE_OPTS 

  validates :clip, attachment_presence: true
  #validates_attachment :clip, :presence =&gt; true   # oldstyle
  #validates_attachment :clip, :content_type =&gt; {:context_type =&gt; 'image&#47;jpg'}
  do_not_validate_attachment_file_type :clip
end
</pre>
