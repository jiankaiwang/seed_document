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

### API
---

* SELECT operation
  1. getConds{} : defined where SQL conditions
  2. getParams [] : selected column names, empty : means all
  3. asdict : returned row as dictionary data type

```python
def select(self, getConds, getParams, asdict=False)
```

* UPDATE operation
  1. getParams : {}, set sql parameters	
  2. getConds : {}, where sql conditions

```python
def update(self, getParams, getConds)
```

* INSERT operation
  1. getParams : {}, value sql parameters	

```python
def insert(self, getParams)
```

* DELETE operation
  1. getConds : {}, where sql conditions

```python
def delete(self, getConds)
```

### Example
---






