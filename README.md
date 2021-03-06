# Plaid [![Build Status](https://travis-ci.org/plaid/plaid-ruby.svg?branch=release_v_1.0.0)](https://travis-ci.org/plaid/plaid-ruby) [![Gem Version](https://badge.fury.io/rb/plaid.svg)](http://badge.fury.io/rb/plaid)

Ruby bindings for the Plaid API

## Notes

This version is a beta version that contains failing tests for the new 'info' endpoint. While these have been tested individually on real accounts the tests here will fail with the test accounts supplied. These will be updated soon with test credentials.

Latest stable version: **1.3.0**

**Warning: If you have been using any version < 1 please switch to the correct branch (V0.1.6). Installing without specifying a version from RubyGems results in V1.1 build. **

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'plaid'
```

And install

    $ bundle

Or install it system wide as:

    $ gem install plaid

## Usage

Please read the great documentation at http://plaid.com/docs/ for more information.

Configure the gem with your client id, secret key, and the environment path you would like to use.

```ruby
Plaid.config do |p|
    p.client_id = 'Plaid provided client ID here'
    p.secret = 'Plaid provided secret key here'
    p.environment_location = 'URL for the development or production environment'
end
```

Authenticate a user to your desired level of api access (auth / connect).

```ruby
user = Plaid.add_user('auth','plaid_test','plaid_good','wells')
```

## Learn More

Learn about the full functionality of the library on our [Wiki](https://github.com/plaid/plaid-ruby/wiki)

## Contribute

We highly encourage helping out with the gem. Either adding more tests, building new helper classes, fixing bugs, or anything to increase overall quality.

Learn more about best practices, submitting a pull request, and rules for the build on our [Wiki](https://github.com/plaid/plaid-ruby/wiki/Contribute!)
