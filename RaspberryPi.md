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

#Commands

####Shutdown
<pre>
<b>sudo shutdown -s</b> <em>now</em>
</pre>

####Reboot
<pre>
<b>sudo shutdown -r</b> <em>now</em>
</pre>

####Service
<pre>
<b>service --status-all</b>            # <em>gives a list of services</em>
<b>service</b> <em>service-name</em>      # <em>gives further options for the command</em>
</pre>

#VNC on RPi3
https://www.realvnc.com/docs/raspberry-pi.html

[RealVNC downloads](https://www.realvnc.com/download/vnc/?utm_medium=email&utm_campaign=license-emails&utm_source=free-trial-license&utm_content=download)

<em>download the VNC package</em>   
curl -L -o VNC.tar.gz https://www.realvnc.com/download/binary/latest/debian/arm/ 
<pre>
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--     0
100 12.0M  100 12.0M    0     0   612k      0  0:00:20  0:00:20 --:--:--  661k
</pre>

<em>get the package name</em>   
tar xvf VNC.tar.gz
<pre>
VNC-Server-5.3.2-Linux-ARM.deb
VNC-Viewer-5.3.2-Linux-ARM.deb
</pre>

<em>install package</em>
sudo dpkg -i VNC-Server-5.3.2-Linux-ARM.deb
<pre>
(Reading database ... 119726 files and directories currently installed.)
Preparing to unpack VNC-Server-5.3.2-Linux-ARM.deb ...
Unpacking realvnc-vnc-server (5.3.2.19179) ...
Setting up realvnc-vnc-server (5.3.2.19179) ...
Updating /etc/pam.d/vncserver
Updating /etc/pam.conf... done
Looking for font path... not found.
Generating private key... done
Installed systemd unit for VNC Server in Service Mode daemon
Start or stop the service with:
  systemctl (start|stop) vncserver-x11-serviced.service
Mark or unmark the service to be started at boot time with:
  systemctl (enable|disable) vncserver-x11-serviced.service

Installed systemd unit for VNC Server in Virtual Mode daemon
Start or stop the service with:
  systemctl (start|stop) vncserver-virtuald.service
Mark or unmark the service to be started at boot time with:
  systemctl (enable|disable) vncserver-virtuald.service


(gconftool-2:4503): GConf-WARNING **: Client failed to connect to the D-BUS daemon:
Unable to autolaunch a dbus-daemon without a $DISPLAY for X11
gconfd-2: no process found
Processing triggers for gconf2 (3.2.6-3) ...
Processing triggers for hicolor-icon-theme (0.13-1) ...
Processing triggers for man-db (2.7.0.2-5) ...
Processing triggers for shared-mime-info (1.3-1) ...
Processing triggers for gnome-menus (3.13.3-6) ...
Processing triggers for desktop-file-utils (0.22-1) ...
Processing triggers for mime-support (3.58) ...
</pre>


