<h2>Add gems to Gemfile</h2>
<pre>
gem 'carrierwave'
gem 'mini_magick'
gem 'fog'
</pre>

$ <b>number install --without production</b>

$ <b>rails g scaffold <em>Image</em> name:string picture:string user:reference</b>

$ <b>rake db:migrate</b>

$ <b>rails generate bootstrap:themed <em>Images</em><b>

<h2>Update models</h2>

<pre>
<em># user.rb</em>

  class User < ActiveRecord::Base
  has_many :images
end
</pre>
<pre>
<em># image.rb</em>

class Image < ActiveRecord::Base
  belongs_to :user
end
</pre>

<h2>Generate uploader</h2>

$ <b>rails generate uploader Picture</b>

<h2>Modify Image model</h2>
<pre>
<em># image.rb</em>

class Image < ActiveRecord::Base
  belongs_to :user
  mount_uploader :picture, PictureUploader
</pre>
