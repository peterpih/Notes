[Upgrading to macOS Sierra will break your SSH keys and lock you out of your own servers](https://medium.freecodecamp.com/upgrading-to-macos-sierra-will-break-your-ssh-keys-and-lock-you-out-of-your-own-servers-f413ac96139a#.7gavw5z76)

###Step #1: delete your old key and create a new one
$ <b>ssh-keygen -l -f ~/.ssh/id_rsa.pub</b>
<pre>
<em>If the prompt responds with a string that starts with “2048 SHA256”   
you’re done and don’t need to take any further action.</em>
</pre>

<em>create a new key</em>  
$ <b>ssh-keygen -t rsa</b>

<pre>
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/freecodecamp/.ssh/id_rsa):
</pre>

<em>You can just press enter to save it in the default place. 
Note that this will overwrite your old (broken) key.</em>

<pre>
Enter passphrase (empty for no passphrase):
</pre>

<em>You can leave this blank or add a password for a little extra 
security (and a lot more typing).</em>

<em>set permissions</em>   
$ <b>sudo chmod 600 ~/.ssh/id_rsa</b>

<em>have a look</em>   
$ <b>cat ~/.ssh/id_rsa.pub</b>
