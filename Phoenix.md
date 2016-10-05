#[Installation](http://www.phoenixframework.org/docs/installation)

<pre>
~/phoenix(setup*) 752 >mix local.hex
Are you sure you want to install archive "https://repo.hex.pm/installs/1.3.0/hex-0.13.2.ez"? [Yn] Y
* creating /Users/peterpih/.mix/archives/hex-0.13.2
</pre>

<pre>

I had already installed

brew install elixir

brew install node

brew install postgres

</pre>

#Create Application

<pre>
<b>mix phoenix.new</b> <em>hello_phoenix</em>
* creating hello_phoenix/config/config.exs
* creating hello_phoenix/config/dev.exs
...
* creating hello_phoenix/web/views/layout_view.ex
* creating hello_phoenix/web/views/page_view.ex

Fetch and install dependencies? [Yn] <b>Y</b>
* running mix deps.get
* running npm install && node node_modules/brunch/bin/brunch build

We are all set! Run your Phoenix application:

    $ cd hello_phoenix
    $ mix phoenix.server

You can also run your app inside IEx (Interactive Elixir) as:

    $ iex -S mix phoenix.server

Before moving on, configure your database in config/dev.exs and run:

    $ mix ecto.create
    
</pre>


