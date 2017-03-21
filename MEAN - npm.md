[A Beginner’s Guide to npm — the Node Package Manager](https://www.sitepoint.com/beginners-guide-node-package-manager/)  

Move the global <b>prefix</b> to <b>.node_modules_global</b> this is where global modules will be installed so `sudo` is not necessary

Add the "local" modules onto $PATH
<pre>
$ export PATH="$HOME/.node_modules_global/bin:$PATH"
</pre>

###Commands
<pre>
$ npm install <em>module-name</em>   
$ npm uninstall <em>module-name</em>   
$ npm update <em>module-name</em>   
$ npm outdated  
$ npm search <em>module-name</em>  
   
  
$ npm ls -g    <em>(show all modules installed globally)</em>   
$ npm ls       <em>(show all modules installed locally)</em>
</pre>
