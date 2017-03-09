###[What I learned migrating a Rails app to Elixir/Phoenix](https://medium.com/@stueccles/what-i-learned-migrating-a-rails-app-to-elixir-phoenix-f707436749aa#.tb614ty2x)

###[Code School](https://www.codeschool.com/courses/mixing-it-up-with-elixir)  
###[Elixir School.com](http://elixirschool.com)  
###[Elixir OKC](https://elixir.school)

###[Installation](http://elixir-lang.org/install.html)
<pre>
<b>brew update</b>

<b>brew install elixir</b>
==> Installing dependencies for elixir: openssl, libpng, libtiff, wxmac, erlang
==> Installing elixir dependency: openssl
==> Downloading https://homebrew.bintray.com/bottles/openssl-1.0.2j.el_capitan.bottle.tar.gz
######################################################################## 100.0%
==> Pouring openssl-1.0.2j.el_capitan.bottle.tar.gz
==> Using the sandbox
==> Caveats
A CA file has been bootstrapped using certificates from the system
keychain. To add additional certificates, place .pem files in
  /usr/local/etc/openssl/certs

and run
  /usr/local/opt/openssl/bin/c_rehash

This formula is keg-only, which means it was not symlinked into /usr/local.

Apple has deprecated use of OpenSSL in favor of its own TLS and crypto libraries

Generally there are no consequences of this for you. If you build your
own software and it requires this formula, you'll need to add to your
build variables:

    LDFLAGS:  -L/usr/local/opt/openssl/lib
    CPPFLAGS: -I/usr/local/opt/openssl/include
    PKG_CONFIG_PATH: /usr/local/opt/openssl/lib/pkgconfig

==> Summary
🍺  /usr/local/Cellar/openssl/1.0.2j: 1,695 files, 12M
==> Installing elixir dependency: libpng
==> Downloading https://homebrew.bintray.com/bottles/libpng-1.6.25.el_capitan.bottle.tar.gz
######################################################################## 100.0%
==> Pouring libpng-1.6.25.el_capitan.bottle.tar.gz
🍺  /usr/local/Cellar/libpng/1.6.25: 25 files, 1.2M
==> Installing elixir dependency: libtiff
==> Downloading https://homebrew.bintray.com/bottles/libtiff-4.0.6_2.el_capitan.bottle.tar.gz
######################################################################## 100.0%
==> Pouring libtiff-4.0.6_2.el_capitan.bottle.tar.gz
🍺  /usr/local/Cellar/libtiff/4.0.6_2: 261 files, 3.4M
==> Installing elixir dependency: wxmac
==> Downloading https://homebrew.bintray.com/bottles/wxmac-3.0.2_3.el_capitan.bottle.tar.gz
######################################################################## 100.0%
==> Pouring wxmac-3.0.2_3.el_capitan.bottle.tar.gz
🍺  /usr/local/Cellar/wxmac/3.0.2_3: 809 files, 23.6M
==> Installing elixir dependency: erlang
==> Downloading https://homebrew.bintray.com/bottles/erlang-19.1.el_capitan.bottle.tar.gz
######################################################################## 100.0%
==> Pouring erlang-19.1.el_capitan.bottle.tar.gz
==> Caveats
Man pages can be found in:
  /usr/local/opt/erlang/lib/erlang/man

Access them with `erl -man`, or add this directory to MANPATH.
==> Summary
🍺  /usr/local/Cellar/erlang/19.1: 7,297 files, 279.8M
==> Installing elixir
==> Downloading https://homebrew.bintray.com/bottles/elixir-1.3.3.el_capitan.bottle.tar.gz
######################################################################## 100.0%
==> Pouring elixir-1.3.3.el_capitan.bottle.tar.gz
🍺  /usr/local/Cellar/elixir/1.3.3: 383 files, 5M

<b>elixir -v</b>
Erlang/OTP 19 [erts-8.1] [source] [64-bit] [smp:8:8] [async-threads:10] [hipe] [kernel-poll:false] [dtrace]

Elixir 1.3.3

</pre>

#Introduction  
http://elixir-lang.org/getting-started/introduction.html
