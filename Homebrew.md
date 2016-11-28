###[Homebrew Repository](https://github.com/Homebrew/homebrew)

<brew cheatsheet](http://ricostacruz.com/cheatsheets/homebrew.html)

http://braumeister.org
<pre>
$ <b>brew update</b>                     # <em>update casks</em>   
$ <b>brew list</b>                       # <em>list installed packages</em>   

$ <b>brew info</b> <em>node</em>                  # <em>shows which version of node.js <b>will be</b> installed</em>   

$ <b>brew doctor</b>                     # <em>check status of casks</em>  
</pre>

###Install a specific version
<pre>
Installed version of software are in <b>/usr/local/Cellar</b>

$ <b>brew list --versions</b> <em>postgresql</em>        # <em>shows installed versions</em>

$ <b>brew tap homebrew/versions</b>  
$ <b>brew search</b> <em>node</em>                      # <em>display versions of "node"</em>

<em>node
node010
node020
node040
</em>
</pre>
<pre>
$ <b>brew unlink</b> <em>node</em>                      # <em>may need to symbol unlink previous version</em>  
$ <b>brew install</b> <em>node010</em>    
$ <b>brew link --overwrite</b> <em>node010</em>   
</pre>
