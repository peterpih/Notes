####The easiest way to get a forwarding page on Heroku is using 3 files in PHP

<b>main.html</b>  <em>(copy and paste)</em>

<pre>
&lt;html&gt;
   &lt;head&gt;
   
      &lt;script type="text/javascript"&gt;
         &lt;!--
            function Redirect() {
               window.location="<em>put target url here</em>";
            }
            
            document.write("You will be redirected to main page in 10 sec.");
            setTimeout('Redirect()', 10000);
         //-->
      &lt;/script&gt;
      
   &lt;/head&gt;
   
   &lt;body&gt;
   &lt;/body&gt;
&lt;/html&gt;
</pre>

<b>index.php</b> <em>(copy and paste)</em>
<pre>
&lt;?php include_once("main.html"); ?&gt;
</pre>

<b>config.json</b> <em>(type command)</em>

$ <b>cat '{}' > config.json</b>
 <pre>
{}
</pre>

<b>After creating those 3 files, intialize git on the directory</b>

$ <b>git init</b>   
$ <b>git add -A</b>   
$ <b>git commit -m</b> <em>"first commit"</em>   
<pre>
[master (root-commit) 6bc75a0] first commit
 3 files changed, 21 insertions(+)
 create mode 100644 composer.json
 create mode 100644 index.php
 create mode 100644 main.html
</pre>

<b>Now Create a new app in heroku</b>  <em>enigmatic-brook-80258</em>

$ <b>git remote add</b> <em>heroku https://git.heroku.com/enigmatic-brook-80258.git</em>  

$ <b>git push</b> <em>heroku master</em>
</pre>

####Heroku should self detect that it is a PHP app
<pre>
Counting objects: 5, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 581 bytes | 0 bytes/s, done.
Total 5 (delta 0), reused 0 (delta 0)
remote: Compressing source files... done.
remote: Building source:
remote: 
remote: -----> PHP app detected
remote: -----> Bootstrapping...
remote: -----> Installing platform packages...
remote:        NOTICE: No runtime required in composer.lock; using PHP ^5.5.17
remote:        - apache (2.4.20)
remote:        - nginx (1.8.1)
remote:        - php (5.6.26)
remote: -----> Installing dependencies...
remote:        Composer version 1.2.1 2016-09-12 11:27:19
remote: -----> Preparing runtime environment...
remote:        NOTICE: No Procfile, using 'web: vendor/bin/heroku-php-apache2'.
remote: -----> Checking for additional extensions to install...
remote: -----> Discovering process types
remote:        Procfile declares types -> web
remote: 
remote: -----> Compressing...
remote:        Done: 13.6M
remote: -----> Launching...
remote:        Released v3
remote:        https://enigmatic-brook-80258.herokuapp.com/ deployed to Heroku
remote: 
remote: Verifying deploy... done.
To https://git.heroku.com/enigmatic-brook-80258.git
 * [new branch]      master -> master
</pre>

<b>You should be good to go!</b>
