# ru_captcha

RUCaptcha is Python rucaptcha.com API implementation

Feature:
 
 -  Parallel token monitoring;
 -  Event driven development programming model support;
 -  You may switching to future or deffered implementation;

Usage example:

```php
  ru_captcha = RUCaptcha(apikey="***")
  value = ru_captcha.parse(path="tests/test_000.jpg", is_regsense=1)
  #
  print("{value!r}".format(value=value))
  #
  while not value.is_ready():
      time.sleep(0.1)
  #
  print("{value!r}".format(value=value))
  #
  print(value.get_value())
  #
  ru_captcha.dispose()
```
