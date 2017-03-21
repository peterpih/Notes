[A Beginner’s Guide to npm — the Node Package Manager](https://www.sitepoint.com/beginners-guide-node-package-manager/)  

Move the global <b>prefix</b> to point <b>.node_modules_global</b> this is where global modules will be installed so `sudo` is not necessary
<pre>
$ cd && mkdir .node_modules_global
$ npm config set prefix=$HOME/.node_modules_global
</pre>

Add the new "global" modules onto $PATH
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

$ npm config get <em>variable</em>    <em>(show config variable value)</em>
$ npm config get prefix

$ npm ls -g    <em>(show all modules installed globally)</em>   
$ npm ls       <em>(show all modules installed locally)</em>
</pre>
