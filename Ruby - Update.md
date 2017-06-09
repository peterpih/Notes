Use <b>rbenv</b> to install versions of Ruby  

$ <b>rbenv install</b> <em>n.n.n</em>

To see the different versions which are available to be installed.  

$ <b>rbenv install --list</b>  

then

<pre>
$ <b>rbenv install</b> <em>2.3.3</em>

Downloading ruby-2.3.3.tar.bz2...
-> https://cache.ruby-lang.org/pub/ruby/2.3/ruby-2.3.3.tar.bz2
Installing ruby-2.3.3...
Installed ruby-2.3.3 to /Users/peterpih/.rbenv/versions/2.3.3
</pre>

in the <b>project root directory</b> make sure there is a
$ <b>echo "2.3.3" > .ruby_version</b>
<pre>
<em># .ruby-version</em>

2.3.3
</pre>

<b>rbenv</b> uses this file to figure out which version of Ruby to use

<b>Check Ruby is running correctly by checking the version</b>

$ <b>ruby -v</b>
<pre>
ruby 2.3.3p222 (2016-11-21 revision 56859) [x86_64-darwin16]
</pre>

##You may need to also update bundler for the new ruby version

$ <b>gem install bundler</b>
<pre>
Fetching: bundler-1.13.6.gem (100%)
Successfully installed bundler-1.13.6
1 gem installed
</pre>

then

$ <b>rbenv rehash</b>

this will setup the correct PATHs, then test bundler is working

$ <b>bundle -v</b>
<pre>
Bundler version 1.13.6
</pre>

then install new dependencies with

$<b>bundle install</b>
<pre>
Fetching gem metadata from https://rubygems.org/..........
Fetching version metadata from https://rubygems.org/..
Fetching dependency metadata from https://rubygems.org/.
Resolving dependencies...
Installing rake 12.0.0
Installing concurrent-ruby 1.0.2
...
Bundle complete! 20 Gemfile dependencies, 71 gems now installed.
Use `bundle show [gemname]` to see where a bundled gem is installed.
</pre>
