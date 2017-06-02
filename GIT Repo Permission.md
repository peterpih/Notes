<h2>With this Error</h2>
<pre>
remote: Permission to railsnewbie257/curl.git denied to peterpih.
fatal: unable to access 'https://github.com/railsnewbie257/curl.git/': The requested URL returned error: 403
</pre>

<h2>Use SSH connection to git</h2>
<pre>
$ git remote rm curl    
$ git remote add curl git@github.com:railsnewbie257/curl.git   
</pre>
<pre>
Please make sure you have the correct access rights
and the repository exists.
</pre>
<h2>Need to generate new SSH key</h2>  

$ <b>cd &#126;/.ssh</b>    
$ <b>ssh-keygen</b>
<pre>
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/peterpih/.ssh/id_rsa): 
/Users/peterpih/.ssh/id_rsa already exists.
Overwrite (y/n)? <b>y</b>
Enter passphrase (empty for no passphrase): &lt;CR&gt;
Enter same passphrase again: &lt;CR&gt;
Your identification has been saved in <b>/Users/peterpih/.ssh/id_rsa</b>.
Your public key has been saved in <b>/Users/peterpih/.ssh/id_rsa.pub</b>.
The key fingerprint is:
SHA256:gdMXF...peterpih@MacBook-Pro.local
The key's randomart image is:
+---[RSA 2048]----+
|    ..  +=*o.    |
|. ..  .o.=+*     |
|*o.   o.oo+.+    |
|=*..   .*o*.     |
|E+B=.  oSO o     |
|++.=    . o      |
|..o              |
|.                |
|                 |
+----[SHA256]-----+
</pre>

$ <b>type /Users/peterpih/.ssh/id_rsa.pub</b>   

<em>Copy contents into Github account you are trying to write to</em>   
<em>In Guthub, under <b>Settings</b> | <b>Deploy keys</b> | <b>Add New Key</b></em>
<pre>
ssh-rsa AAAAB3NzaC1yc2EAAA...
</pre>

<h2>Test the new SSH Key</h2>   
$ <b>ssh -T git@github.com</b>
<pre>
Hi railsnewbie257! You've successfully authenticated, but GitHub does not provide shell access.
</pre>



