# Status

Retrieve the server’s current status.

## Example Usage

```java
// Java
// new Status(); // TODO: How to get status in Java
```
```python
# Python 
# (not implemented)
```
```javascript
// Javascript
// webdriver.io
driver.status();

// wd
await driver.status();
```
```ruby
# Ruby example
```
```php
# PHP example
```

## Description

Returns information about whether a remote end is in a state in which it can create new sessions and can additionally include arbitrary meta information that is specific to the implementation.

The readiness state is represented by the ready property of the body, which is false if an attempt to create a session at the current time would fail. However, the value true does not guarantee that a New Session command will succeed.

Implementations may optionally include additional meta information as part of the body, but the top-level properties ready and message are reserved and must not be overwritten.

## Client Docs

* [Java](http://seleniumhq.github.io/selenium/docs/api/java/index.html)
* [Python](http://selenium-python.readthedocs.io/api.html#selenium.webdriver.common.utils.is_url_connectable)
* [Javascript (WebdriverIO)](http://webdriver.io/api/protocol/status.html)
* [Javascript (WD)](https://github.com/admc/wd/blob/master/lib/commands.js#L44)
* [Ruby](http://www.rubydoc.info/gems/selenium-webdriver/Selenium/WebDriver/DriverExtensions/HasRemoteStatus#remote_status-instance_method)
* TODO: PHP

## Support

### Appium Server

|Platform|Driver|Platform Versions|Appium Version|Driver Version|
|--------|----------------|------|--------------|--------------|
|iOS|[XCUITest](/docs/en/drivers/ios-xcuitest.md)| 9.3+ | 1.6.0+ | All |
| |[UIAutomation](/docs/en/drivers/ios-xcuitest.md)| 8.0 to 9.3 | All | All |
|Android|[UiAutomator2](/docs/en/drivers/android-uiautomator2.md)| ? | 1.6.0+ | All|
| |[UiAutomator](/docs/en/drivers/android-uiautomator.md)| 4.2+ | All | All |
| |[Espresso](/docs/en/drivers/android-espresso.md)| TBD | TBD |TBD
|Windows|[Windows](/docs/en/drivers/windows.md)| 10+ | 1.6.0+ |All|
|Mac|[Mac](/docs/en/drivers/mac.md)|?| 1.6.4+ |All|

### Appium Clients 

|Language|Support|
|--------|-------|
|[Java](https://github.com/appium/java-client/releases/latest)|All|
|[Python](https://github.com/appium/python-client)|All|
|[Javascript (WebdriverIO)](http://webdriver.io/index.html)|All|
|[Javascript (WD)](https://github.com/admc/wd/releases)|All|
|[Ruby](https://github.com/appium/ruby_lib/releases/latest)|All|
|[PHP](https://github.com/appium/php-client/releases/latest)|All|

## HTTP API Specifications

### Endpoint

`GET /wd/hub/status`

### URL Parameters

None

### JSON Parameters

None

### Response

|Key|Type|Value|
|---|----|----|
|build.version|string|A generic release label (i.e. "2.0rc3")|
|build.revision|string|The revision of the local source control client from which the server was built|

## See Also

* [W3C Specification](https://www.w3.org/TR/webdriver/#status)
* [JSONWP Specification](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#status)