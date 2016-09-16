# REQUESTMETHOD.py

<script type="text/javascript" src="../js/general.js"></script>

### Dependency
---

* urllib
* urllib2
* json

### Constructor
---

```python
#
# desc : constructor
# param@getURL : e.g. 192.168.2.5/test/index.php
# param@getHeaderSetting : e.g. { "Authorization" : "abcdefg-hijk-lmnop-qrstuv-wxyz" }
# param@getData : e.g. { "method" : "post" }
# param@getMtd : one of ["GET", "POST", "PUT", "DELETE"]
#
def __init__(self, getURL, getHeaderSetting, getData, getMtd="GET")
```

### API
---


