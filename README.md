# Swot :apple:

[![Build Status](https://api.travis-ci.org/leereilly/swot.png)](https://travis-ci.org/leereilly/swot) [![Gem Version](https://badge.fury.io/rb/swot.svg)](http://badge.fury.io/rb/swot)

Ruby gem for accessing swot dataset – see https://github.com/leereilly/swot for a description.

### Installation

Swot is a Ruby gem, so you'll need a little Ruby-fu to get it working. Simply

`gem install swot`

Or add this to your `Gemfile` before doing a `bundle install`:

`gem 'swot'`

### Usage

#### Verify Email Addresses

```ruby
Swot::is_academic? 'lreilly@stanford.edu'           # true
Swot::is_academic? 'lreilly@strath.ac.uk'           # true
Swot::is_academic? 'lreilly@soft-eng.strath.ac.uk'  # true
Swot::is_academic? 'pedro@ugr.es'                   # true
Swot::is_academic? 'lee@uottawa.ca'                 # true
Swot::is_academic? 'lee@leerilly.net'               # false
```

#### Verify Domain Names

```ruby
Swot::is_academic? 'harvard.edu'              # true
Swot::is_academic? 'www.harvard.edu'          # true
Swot::is_academic? 'http://www.harvard.edu'   # true
Swot::is_academic? 'http://www.github.com'    # false
Swot::is_academic? 'http://www.rangers.co.uk' # false
```

#### Find School Names

```ruby
Swot::school_name 'lreilly@cs.strath.ac.uk'
# => "University of Strathclyde"

Swot::school_name 'http://www.stanford.edu'
# => "Stanford University"
```

### Contributing to Swot

Code contributions and ports to different languages are welcome!

**Thanks** to the following people for their contributions:
@blutack, @captn3m0, @chrishunt, @johndbritton, @johnotander, @pborreli, @rcurtis, @vikhyat.

**Special thanks** to @weppos for the [public_suffix](https://github.com/weppos/publicsuffix-ruby) gem :metal:
