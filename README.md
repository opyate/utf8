
```
>>> import requests, sys
>>> resp = requests.get("https://raw.githubusercontent.com/opyate/utf8/master/test.json")
>>> resp.encoding
'utf-8'
>>> resp.content                 # yuck
'{"umbrella":"\xe2\x98\x82"}\n'
>>> print resp.content           # better...
{"umbrella":"☂"}

>>> # ... why?
... 
>>> sys.getdefaultencoding()
'ascii'
>>> sys.stdout.encoding
'UTF-8'
>>> 
```
