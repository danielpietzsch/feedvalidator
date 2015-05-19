= FeedValidator [![Build Status](https://travis-ci.org/edgar/feedvalidator.png?branch=master)](https://travis-ci.org/edgar/feedvalidator) [![Gem Version](https://badge.fury.io/rb/feedvalidator.svg)](http://badge.fury.io/rb/feedvalidator)

FeedValidator is an interface to the {W3C Feed Validation online service}[http://validator.w3.org/feed/],
based on its SOAP 1.2 support.

It helps to find errors in RSS or ATOM feeds.

FeedValidator add a new assertion (<code>assert_valid_feed</code>) which you can use in Rails applications.
This assertion implements a cache to improve the performance of the tests and to not abuse of the
{W3C Feed Validation online service}[http://validator.w3.org/feed/]


== Examples

* For use FeedValidator just do this:

    ```ruby
    require 'feed_validator'

    v = W3C::FeedValidator.new()
    v.validate_url('http://www.w3.org/QA/news.rss')
    puts v.to_s unless v.valid?
    ```

* In Rails you can use it in your functional tests, just modify your /test/test_helper.rb adding this line:

    ```ruby
    require 'feed_validator/assertions'
    ```

  And now you can use in your functional test, in this way:

    ```ruby
    def test_bar_valid_feed
      get :bar
      assert_valid_feed
    end
    ```

  Or use the class-level method to quickly create validation tests for a bunch of actions at once:

    ```ruby
    assert_valid_feed :bar, :foo
    ```

== Download

The latest version of FeedValidator can be found at

* http://github.com/edgar/feedvalidator

Documentation can be found at

* http://feedvalidator.rubyforge.org


== Installation

You can install FeedValidator as a gem:

  ```ruby
  gem install feedvalidator
  ```

Or you can install it from the tarball or zip packages on the download page
and then extract it to your lib directory as you would with any other
Ruby library.


== License

FeedValidator is released under the MIT license.
