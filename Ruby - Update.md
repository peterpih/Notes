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

in the project root directory make sure there is a
<pre>
# .ruby-version

<em>2.3.3</em>
</pre>

<b>rbenv</b> uses this file to figure out which version of Ruby to use

<b>Check the Ruby version</b>

$ <b>ruby -v</b>
<pre>
ruby 2.3.3p222 (2016-11-21 revision 56859) [x86_64-darwin16]
</pre>
