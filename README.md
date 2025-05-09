# datajs

A library to make working with JSON files simpler

# Hot to use

All you have to do is specify a JSON file, along with the database name and collection

```py

import datajs

js = datajs.JS_file("data.json")
js.database = "data"
js.collection = "collect"

```

# Note 

The JSON file must be in the same project file. If it is in another file, the path must be specified

# How to fetch data

The library contains a function called find that enables you to add a specific condition from which to retrieve data

```py

json_data = js.find({"age": 15}, "one")

```

# How to add data

The library contains a function called insert that enables you to add the data you want

```py

js.insert({"name": "ahmed", "age": 17})

```

# How to update data

The library contains a function called update that allows you to add a condition to retrieve old data and change it

```py

js.update({"age": 15}, {"name": "yassen"}, "all")

```
# How to delete data

The library contains a function called delete that enables you to add a condition to delete the data you want

```py

js.delete({"age": 15}, "all")

```

# Note

In all the functions mentioned except for the insert function, there is something called option with two options. The first is "one", which means that the function works on the first data in the database, and the other is "all", which means that the function works on all the data according to the condition that you added

# How to delete database

The library has a function called delete_database that allows you to delete the database you want

```py

js.delete_database("database_name")

```

# How to delete collection

The library has a function called delete_collection that allows you to delete the collection you want

```py

js.delete_collection("collection_name")

```

# How to get databases

The library has a function called get_database which allows you to find out your databases

```py

databases = js.get_database()

```

# How to get collection

The library has a function called get_collection which allows you to find out your collections

```py

collections = js.get_collection()

```
