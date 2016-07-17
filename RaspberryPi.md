###Soldering

<pre>
From: http://www.electro-tech-online.com/threads/dull-coulored-solder-joints.127272/
----
This is my favorite basic soldering video: <a href="http://www.youtube.com/watch?v=I_NU2ruzyc4">How and why to solder correctly</a>


----
In this video, the correct method is shown but for most field repairs, as long as the terminal is 
clean and the solder wets well, tinning just the wire should be sufficient. In a production setting, 
wire and terminals are often tinned by fluxing and dipping in a solder pot.

http://m.youtube.com/watch?desktop_uri=/watch?v=Ql6Vkw5wswU&v=Ql6Vkw5wswU&gl=US#/watch?v=Ql6Vkw5wswU

This shows more wire tinning using a heat sink to prevent wicking under the insulation and insulation 
melting/retracting.  On stranded wires with minimal twist, twist the end a little tighter before 
tinning to prevent the strands from splaying.

http://m.youtube.com/#/watch?v=xpiyB7ZM3vg
</pre>

###[Unboxing Raspberry Pi](https://www.youtube.com/watch?v=-6OGuhLtKbU)
###Connecting Raspberry Pi
[Raspberry Pi Remote Connections – Without A Network!](https://pihw.wordpress.com/guides/direct-network-connection/)

###[Updating Raspbian](https://www.youtube.com/watch?v=-6OGuhLtKbU&t=15m52s)
<pre>
sudo apt-get update
sudo apt_get upgrade
</pre>

To add VNC
<pre>
sudo apt-get install tightvncserver
</pre>


###[Use-ssh-to-talk-with-your-Raspberry-Pi](http://www.instructables.com/id/Use-ssh-to-talk-with-your-Raspberry-Pi/)
On a Mac
<pre>
<b>ssh pi@</b><em>ip-address</em>
</pre>
You can find the <em>ip-address</em> by typing **ifconfig** on the RPI CLI.

###[how-to-tell-which-services-run-at-startup-on-raspberry-pi-raspbian](http://superuser.com/questions/852610/how-to-tell-which-services-run-at-startup-on-raspberry-pi-raspbian)

####Shutdown
<pre>
<b>sudo shutdown -s</b> <em>now</em>
</pre>

####Reboot
<pre>
<b>sudo shutdown -r</b> <em>now</em>
</pre>
