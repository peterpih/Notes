###Steps to take after

1- <b>cd</b> <em>directory-above-where-app-will-live</em>

2 - <b>rails new</b> <em>new-app</em>
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

3 - $ <b>cd</b> <em>new-app</em>  
4 - $ <b>git init</b>
<pre>
Initialized empty Git repository in /Users/user-name/new-app/.git/
</pre>

<b>Connect to GitHub</b>

5 - create a repository on GitHub, include a README.md

6 - under the "Clone or Download" button, get the url for the repository and add as a remote
<pre>
$ <b>git remote add</b> <em>origin</em> <b>https://github.com/</b><em>user-name</em>/<em>repo-name</em><b>.git</b>
</pre>

7 - $ <b>git remote -v</b>
<pre>
origin	https://github.com/<em>user-name</em>/<em>repo-name</em>.git (fetch)
origin	https://github.com/<em>user-name</em>/<em>repo-name</em>.git (push)
</pre>

8 - $ <b>git add -A</b>

9 - $ <b>git commit -m</b> "<em>first commit</em>"
<pre>
[master (root-commit) fd598c5] first commit
 57 files changed, 987 insertions(+)
 create mode 100644 .gitignore
        ...
</pre>

10 - $ <b>git push -f</b> <em>origin</em> <b>master</b>
<pre>
Counting objects: 64, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (53/53), done.
Writing objects: 100% (64/64), 16.57 KiB | 0 bytes/s, done.
Total 64 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/peterpih/another-test.git
 + ebce808...fd598c5 master -> master (forced update)
</pre>
 
11 - $ <b>git status</b>
<pre>
On branch master
nothing to commit, working tree clean
</pre>

##You are ready to go!
