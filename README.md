A base library for [Hoptoad](http://www.hoptoadapp.com/) error reporting.

Toadhopper can be used to report plain old Ruby exceptions, or to build a framework-specific gem such as [toadhopper-sinatra](http://github.com/toolmantim/toadhopper-sinatra).

    begin
      raise "Kaboom!"
    rescue  => e
      require 'toadhopper'
      ToadHopper("YOURAPIKEY").post!(e)
    end

You can install it via rubygems:

    gem install toadhopper

## Development

Install Bundler 0.9.x, then:

    % git clone git://github.com/toolmantim/toadhopper.git
    % cd toadhopper
    % bundle install
    % bundle exec rake test

If you set a `HOPTOAD_API_KEY` environment variable it'll test actually posting to the Hoptoad API. For example:

    % bundle exec rake test HOPTOAD_API_KEY=abc123

To generate the docs:

    % bundle exec yardoc

## Contributors

* [Tim Lucas](http://github.com/toolmantim)
* [Samuel Tesla](http://github.com/stesla)
* [atmos](http://github.com/atmos)
* [indirect](http://github.com/indirect)
