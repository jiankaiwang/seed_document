# py2psql.py

<script type="text/javascript" src="../js/general.js"></script>

### Dependency
---

* psycopg2 (PostgreSQL + Python)

### Constructor
---

* constructed parameter:
  1. host : URL or IP
  2. port : postgresql server port
  3. db : database name as a string
  4. tb : table name as a string
  5. user : login user as a string
  6. pwd : the password as a string

```python
# constructor
def __init__(self, getHost, getPort, getDB, getTB, getUser, getPwd)
```

