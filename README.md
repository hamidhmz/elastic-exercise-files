# Structure:
* In elastic instead of table we have *index*
* Instead of rows we have *documents*
* Instead of columns we have *Fields*
* We have : `Index > Type > Document > Field`
* For each Index we have just One Type and for each type we have multiple Documents and for each Documents we have multiples Fields
* In elastic instead of saying inserting data it would called indexing

# INDEX:
* Indexes have just 3 sections:
  
   * aliases: 
   * mappings: model of data
   * settings: 


# Commands:
```
(PUT/POST/GET/DELETE) /{index}/{type}/{id}/({filed})
{
    "field1": "value1",
    "field2": "value2",
    ...
}
```

## GET: 
### Examples:

1. get all a data specific by one id and also you can filter it by name
```
GET /{index}/{type}/{id}/({filed})
```

2. search inside index or type
```
GET /{index}/{type}/_search
```
or
```
GET /{index}/_search
```
it would return object inside this object all of data is inside hits.hits by array

2. get data by `term`
```
GET /{index}/({type}/)_search
{
    "query" : {
        "term":{
            "{key}":"{value}"
        }
    }
}
```

3. get data by `match_all`
```
GET /{index}/({type}/)_search
{
    "query" : {
        "match_all":{}
    }
}
```

## PUT:
* For `updating you can create` document with this command and update 
* For each time you would update one document in background elastic would remove and create your document again

1. create or update index or document or type
```
PUT /{index}/{type}/{id}
{
    "field1": "value1",
    "field2": "value2",
    ...
}
```

## POST:
* For `update and for create` would be used 


## DELETE:
* For `delete` would be used 
* You can delete documents
* You can delete types
* You can delete indices