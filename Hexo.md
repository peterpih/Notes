[Really useful tutorial to get you going](http://js.tomordonez.com/Javascript/Hexo-Tutorial-To-Build-A-Static-Website-With-Node-JS/)

###[Prereq: Install Node.js and npm with Homebrew](http://blog.teamtreehouse.com/install-node-js-npm-mac)
<pre>
  <b>brew install node</b>
</pre>
To check installation
<pre>
  <b>node -v</b>  <em>( check version )</em>
  <b>npm -v</b>
</pre>

###Install Hexo
<pre>
  <b>npm install -g hexo-cli</b>
</pre>

###Create blog directory
<pre>
  <b>mkdir</b> <em>hexo</em>  <em>( you can put all your hexos under a root directory )</em>
  <b>cd</b> <em>hexo</em>
  
  <b>hexo init</b> <em>code-blog</em> 
  <b>cd</b> <em>code-blog</em>
  <b>npm install</b>
  <b>git init</b>
</pre>

Check with a local hexo server
<pre>
  <b>hexo server</b>
</pre>

###Create new Post
<pre>
  <b>hexo new</b> <em>"name-of-post"</em> <em>( in quotes )</em>
</pre>


###Modify configuration file _config.yml.

Scroll down to Deployment and edit:
<pre>
    <b>type: git</b>
    <b>repo: git@github.com:</b><em>your-username/your-username</em>.github.io.git <em>( your-username necessary for github.io pages )</em>
  <b>branch: master</b>
</pre>


You can clone into <em>code-blog</em> as usual
