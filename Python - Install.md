$ <b>brew install python3</b>
<pre>
<b>==> Installing dependencies for python3: sqlite, openssl, xz
==> Installing python3 dependency: sqlite
==> Downloading https://homebrew.bintray.com/bottles/sqlite-3.19.2.sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring sqlite-3.19.2.sierra.bottle.tar.gz
==> Using the sandbox
==> Caveats</b>
Homebrew has detected an existing SQLite history file that was created
with the editline library. The current version of this formula is
built with Readline. To back up and convert your history file so that
it can be used with Readline, run:

  sed -i~ 's/\\040/ /g' ~/.sqlite_history

before using the `sqlite` command-line tool again. Otherwise, your
history will be lost.

This formula is keg-only, which means it was not symlinked into /usr/local,
because macOS provides an older sqlite3.

If you need to have this software first in your PATH run:
  echo 'export PATH="/usr/local/opt/sqlite/bin:$PATH"' >> ~/.bash_profile

For compilers to find this software you may need to set:
    LDFLAGS:  -L/usr/local/opt/sqlite/lib
    CPPFLAGS: -I/usr/local/opt/sqlite/include
For pkg-config to find this software you may need to set:
    PKG_CONFIG_PATH: /usr/local/opt/sqlite/lib/pkgconfig

==> <b>Summary</b>
🍺  /usr/local/Cellar/sqlite/3.19.2: 12 files, 2.9MB
==> <b>Installing python3 dependency:</b> openssl
==> <b>Downloading https://homebrew.bintray.com/bottles/openssl-1.0.2l.sierra.bottle.tar.gz
######################################################################## 100.0%</b>
==> <b>Pouring openssl-1.0.2l.sierra.bottle.tar.gz</b>
==> <b>Caveats</b>
A CA file has been bootstrapped using certificates from the SystemRoots
keychain. To add additional certificates (e.g. the certificates added in
the System keychain), place .pem files in
  /usr/local/etc/openssl/certs

and run
  /usr/local/opt/openssl/bin/c_rehash

This formula is keg-only, which means it was not symlinked into /usr/local,
because Apple has deprecated use of OpenSSL in favor of its own TLS and crypto libraries.

If you need to have this software first in your PATH run:
  echo 'export PATH="/usr/local/opt/openssl/bin:$PATH"' >> ~/.bash_profile

For compilers to find this software you may need to set:
    LDFLAGS:  -L/usr/local/opt/openssl/lib
    CPPFLAGS: -I/usr/local/opt/openssl/include
For pkg-config to find this software you may need to set:
    PKG_CONFIG_PATH: /usr/local/opt/openssl/lib/pkgconfig

==> <b>Summary</b>
🍺  /usr/local/Cellar/openssl/1.0.2l: 1,709 files, 12.2MB
==> <b>Installing python3 dependency:</b> xz
==> Downloading https://homebrew.bintray.com/bottles/xz-5.2.3.sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring xz-5.2.3.sierra.bottle.tar.gz
🍺  /usr/local/Cellar/xz/5.2.3: 92 files, 1.4MB
==> Installing python3 
==> <b>Downloading https://homebrew.bintray.com/bottles/python3-3.6.1.sierra.bottle.1.tar.gz
######################################################################## 100.0%</b>
==> <b>Pouring python3-3.6.1.sierra.bottle.1.tar.gz</b>
==> <b>/usr/local/Cellar/python3/3.6.1/bin/python3 -s setup.py --no-user-cfg install --force --verbose --install-scripts=/usr/local/Cellar/python3/3.6.1/bin --install-lib=/usr/local/lib/py</b>
==> <b>/usr/local/Cellar/python3/3.6.1/bin/python3 -s setup.py --no-user-cfg install --force --verbose --install-scripts=/usr/local/Cellar/python3/3.6.1/bin --install-lib=/usr/local/lib/py</b>
==> <b>/usr/local/Cellar/python3/3.6.1/bin/python3 -s setup.py --no-user-cfg install --force --verbose --install-scripts=/usr/local/Cellar/python3/3.6.1/bin --install-lib=/usr/local/lib/py</b>
==> <b>Caveats</b>
Pip, setuptools, and wheel have been installed. To update them
  pip3 install --upgrade pip setuptools wheel

You can install Python packages with
  pip3 install <package>

They will install into the site-package directory
  /usr/local/lib/python3.6/site-packages

See: http://docs.brew.sh/Homebrew-and-Python.html
==> <b>Summary</b>
🍺  /usr/local/Cellar/python3/3.6.1: 3,600 files, 55.8MB
</pre>
