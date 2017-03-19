[<h2>Installing a specific version of a homebrew package</h2>](http://effectif.com/mac-os-x/installing-specific-version-of-homebrew-formula)  
Look for the version you want:   
$ <b>brew search postgres</b>
<pre>
check_postgres      postgres-xc         <b>postgresql</b> ✔        <b>postgresql@9.4</b> ✔    postgresql@9.5      postgrest
Caskroom/cask/navicat-for-postgresql    Caskroom/cask/postgres                  Caskroom/cask/sqlpro-for-postgres
Caskroom/cask/photo-supreme-postgresql  Caskroom/cask/postgrespreferencepane
</pre>

Then use:   
$ <b>brew install postgresql@9.4</b>


Search Brew http://searchbrew.com - search for a package  
Listing of the Master Repository https://github.com/Homebrew/homebrew/tree/master/Library/Formula"


<h2>Install a specific version</h2>
<pre>
Installed versions of software are in <b>/usr/local/Cellar</b>

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

[<h2>Homebrew Repository</h2>](https://github.com/Homebrew/homebrew)

[brew cheatsheet](http://ricostacruz.com/cheatsheets/homebrew.html)

[Braumeister.org](http://braumeister.org)  online package browser for Homebrew
<pre>
$ <b>brew update</b>                     # <em>update casks</em>   
$ <b>brew list</b>                       # <em>list installed packages</em>   

$ <b>brew info</b> <em>node</em>                  # <em>shows which version of node.js <b>will be</b> installed</em>   

$ <b>brew doctor</b>                     # <em>check status of casks</em>  
</pre>
