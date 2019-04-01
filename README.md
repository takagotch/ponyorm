### ponyorm
---
https://ponyorm.com/

https://docs.ponyorm.org/firststeps.html

```py
select(c for c in Customer if sum(c.orders.total_price) > 1000)

Customer.select(lambda c: sum(c.orders.total_price) > 1000)

db = Database()

@db.on_connect(provider='sqlite')
def sqlite_case_sensitivity(db, connection):
  cursor = connection.cursor()
  cursor.execute('PRAGMA case_sensitive_like = OFF')

db.bind(**options)
db.generate_mapping(create_tables=True)

data = db.select("select * from Person where name = $x", {"x" : "Susan"})

data = db.select("select * from Person where name = $(x.lower()) and age > $(y + 2)")

x = 10
a = 20
b = 30
db.execute("SELECT * FROM Table1 WHERE column1 = $x and column2 = $(a + b)")

x = "John"
data = db.select("select * from Person where name = $x")

db.bind(provider='sqlite', filename=':memory:')

db.bind(provider='sqlite', filename=':memory:')
db.bind(provider='sqlite', filename='filename', create_db=True)
db.bind(provider='mysql', host='', user='', passwd='', db='')
db.bind(provider='oracle', user='', password='', dsn='')

db.generate_mapping(create_tables=True)

db = Database()

class MyEntity(db.Entity):
  attr1 = Required(str)
  
db.bind(provider='postgres', user='', password='', host='', database='')

db.bind(provider='sqlite', filename='database.sqlite', create_db=True)
db.bind(provider='sqlite', filename=':memory:')
```

```
```

```
```


