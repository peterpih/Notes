###Steps using <b>git clone</b>

1 - create a repository on GitHub, include a README.md

2 - under the "Clone or Download" button, <b>copy</b> the url for the repository
<pre>
<b>https://github.com/</b><em>user-name</em>/<em>repo-name</em><b>.git</b>
</pre>

3 - <b>cd</b> <em>directory-above-where-app-will-live</em>

4 - <b>git clone https://github.com/</b><em>user-name</em>/<em>repo-name</em>.<b>git</b>  <em>new-app</em>
<pre>
Cloning into '<em>new-app</em>'...
remote: Counting objects: 64, done.
remote: Compressing objects: 100% (51/51), done.
remote: Total 64 (delta 2), reused 64 (delta 2), pack-reused 0
Unpacking objects: 100% (64/64), done.
</pre>

5 - <b>rails new</b> <em>new-app</em>
<pre>
     create  
      create  README.rdoc
      create  Rakefile
      create  config.ru
      ...
      run  bundle install
Fetching gem metadata from https://rubygems.org/
Fetching version metadata from https://rubygems.org/
Fetching dependency metadata from https://rubygems.org/
Resolving dependencies.....
      ...
Bundle complete! 12 Gemfile dependencies, 56 gems now installed.
Use `bundle show [gemname]` to see where a bundled gem is installed.
         run  bundle exec spring binstub --all
* bin/rake: spring inserted
* bin/rails: spring inserted
</pre>

6 - $ <b>git add -A</b>

7 - $ <b>git commit -m</b> "<em>first commit</em>"
<pre>
[master (root-commit) fd598c5] first commit
 57 files changed, 987 insertions(+)
 create mode 100644 .gitignore
        ...
</pre>

8 - $ <b>git push -f</b> <em>origin</em> <b>master</b>
<pre>
Counting objects: 64, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (53/53), done.
Writing objects: 100% (64/64), 16.57 KiB | 0 bytes/s, done.
Total 64 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/peterpih/another-test.git
 + ebce808...fd598c5 master -> master 
</pre>
 
9 - $ <b>git status</b>
<pre>
On branch master
nothing to commit, working tree clean
</pre>

##You are ready to go!
