# Pytholenium

[![Build Status](https://travis-ci.org/ArgiesDario/pytholenium.svg?branch=master)](https://travis-ci.org/ArgiesDario/pytholenium)
![GitHub](https://img.shields.io/github/license/ArgiesDario/pytholenium.svg)
[![Coverage Status](https://coveralls.io/repos/github/ArgiesDario/pytholenium/badge.svg?branch=master)](https://coveralls.io/github/ArgiesDario/pytholenium?branch=master)

pytholenium is a simple but powerful python-selenium selector that allows you to combine selenium with attribute selections, combining multiple "wait/get/do" actions in a single line

## Getting Started

To install pytholenium using pip just do: ```pip install pytholenium```


## Easy usage example

Having the following html:

```html
<button name="my_button" some_attribute="atenas">Click me</button>
<button name="my_button" some_attribute="hares">Click me</button> <!-- You want to click this one -->
<button name="other_button" some_attribute="hares">Click me</button>
```

Attempting to wait for element to be displayed, then selecting all name="my_button", from that subset selecting some_attribute="hares", finally clicking the element, could be mulitple lines of code.

Using pytholenium you can wait, get, do action, in a single line mixing selections types:

```python
from pytholenium import pytholenium as pl
pl.wait_do (driver=driver, params={"name": "my_button", "some_attribute": "hares"}, action="click")
```

## Documentation

You can find more examples and details in our [Documentation](https://github.com/ArgiesDario/pytholenium/blob/master/DOCUMENTATION.md)


## License

This project is licensed under the GNU License - see the [LICENSE](https://github.com/ArgiesDario/pytholenium/blob/master/LICENSE) file for details
