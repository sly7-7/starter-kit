starter-kit
===========

A starter kit for Ember

Your Ember.js project is almost ready! Here's how to get started:

- Start writing your app in js/app.js.

- Describe your application HTML in index.html.

- During development, you can link to js/libs/ember-*.js to get the
  unminified version of Ember.js.

- Add CSS to css/style.css

Tests
=====

This starter kit comes with an integration test sample, written for QUnit runner. 

You can run the tests by opening the `index.html?tests` page in your browser.

The test is located in the `tests/tests.js` file.

```javascript

// in order to see the app running inside the QUnit runner
App.rootElement = '#ember-testing';

// Common test setup
App.setupForTesting();
App.injectTestHelpers();

// common QUnit module declaration
module("Integration tests", {
  setup: function() {
    // before each test, ensure the application is ready to run.
    Ember.run(App, App.advanceReadiness);
  },

  teardown: function() {
    // reset the application state between each test
    App.reset();
  }
});

// QUnit test case
test("/", function() {
  // async helper telling the application to go to the '/' route
  visit("/");

  // helper waiting the application is idle before running the callback
  andThen(function() {
    equal(find("h2").text(), "Welcome to Ember.js", "Application header is rendered");
    equal(find("li").length, 3, "There are three items in the list");
  });
});

```

For more information about ember-testing package see [ember-testing](http://emberjs.com/guides/testing/integration/)

For more information about the QUnit testing framework, see [QUnit](http://qunitjs.com/)

Contact
====

www.emberjs.com
