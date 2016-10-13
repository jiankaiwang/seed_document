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
#
# desc : constructor
# param@getTB : can be null when only using execsql()
#
def __init__(self, getHost, getPort, getDB, getTB, getUser, getPwd):
```

### API
---

* SELECT operation
  1. param@getConds : {}, defined where SQL conditions
  2. param@getParams : [], selected column names, empty : means all
  3. param@asdict : boolean, returned row as dictionary
  4. data as [] type
  5. also support status object, use status()

```python
def select(self, getConds, getParams, asdict=False):
```

* UPDATE operation
  1. param@getParams : {}, set sql parameters  
  2. param@getConds : {}, where sql conditions
  3. retn : 0 : failure, 1 : success
  4. note : also support status object, use status()

```python
def update(self, getParams, getConds)
```

* INSERT operation
  1. param@getParams : {}, value sql parameters    
  2. retn : 0 : failure, 1 : success
  3. note : also support status object, use status()

```python
def insert(self, getParams)
```

* DELETE operation
  1. param@getConds : {}, where sql conditions
  2. retn : 0 : failure, 1 : success
  3. note : also support status object, use status()

```python
def delete(self, getConds)
```

* Custom SQL operation
  1. param@getSQL : parameter-based complex sql command，
     e.g. "select * from public.user where name = %(name)s;"
  2. param@hasRetValue : are there returned values ?
  3. param@getParams : {}
     e.g. {'name' : "test114"}
  4. param@asdict : only works when param@hasRetValue is true, returned value as dictionary data type
  5. retn : return executing status

```python
def execsql(self, getSQL, hasRetValue, getParams, asdict=True)
```

* Get Table schema
  1. param@getTable : get desired table schema
  2. retn : status object
  3. note : when param@getTable == None, **self.__tb** must exist at the beginning of object creation

```python
def getTableSchema(self, getTable=None)
```

### Example
---

```python
# link to postgresql database
p2l = py2psql("127.0.0.1","5432","ckan_default","public.user","ckan_default","ckan")

# get table schema
p2l = py2psql("127.0.0.1","5432","ckan_default","public.user","ckan_default","ckan")
p2l.getTableSchema()  # default table
p2l2 = py2psql("127.0.0.1","5432","ckan_default","","ckan_default","ckan")
p2l2.getTableSchema("public.user")  # desired table
p2l.status()

# query data and select column name, email, 123 (not existing)
data = p2l.select({where},[columns])
data = p2l.select({"name":"test114"},["name","email","123"])
data = p2l.select({"name":"test114"},[])

# query data and select column name, email, 123 (not existing) and also returned as dictionary
data = p2l.select({where},[columns],asdict=True)
data = p2l.select({"name":"test114"},["name","email","123"],asdict=True)
data = p2l.select({"name":"test114"},[],asdict=True)

# update data
p2l.update({set},{where})
p2l.update({"email":"test@tw"},{"name":"test114"})

# insert data
p2l.insert({ data })
p2l.insert({ "id" : "acbdhcbdh-abchdbch", "name":"123","email":"123@tw" })

# delete data
p2l.delete({where})
p2l.delete({"name":"test1", "email":"test1@tw"})

# execsql data
# create object without assign table
p2l.execsql("sql command", is there returned value, {parameter : value})
p2l.execsql("select * from public.user where name = %(name)s;", True, {'name' : "test114"}, True)
p2l.status()
```




