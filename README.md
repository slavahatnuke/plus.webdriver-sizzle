plus.webdriver-sizzle
==============
Its based on [webdriver-sizzle](https://www.npmjs.com/package/webdriver-sizzle) and fixes issues related to the latest `selenium-webdriver` updates issues.  
Locate a [selenium-webdriver](https://npmjs.org/package/selenium-webdriver) element by sizzle CSS3 selector.

```javascript
var selenium = require('selenium-webdriver');
var sizzle = require('webdriver-sizzle');
var driver = new seleniumWebdriver.Builder().forBrowser('chrome').build();
var $ = sizzle(driver);
    

// Find the first element with class btn and click it
$('.btn').click().then(function() {
  console.log('ok')
});

// Count the paragraphs
$.all('p').then(function (elements) {
  console.log(elements.count);
});

```