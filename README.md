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
PUT(POST/GET/DELETE) /{index}/{type}/{id}/({filed})
{
    "field1": "value1",
    "field2": "value2",
    ...
}
```


## PUT:
* For `updating you can create` document with this command and update 
* For each time you would update one document in background elastic would remove and create your document again

## POST:
* For `update and for create` would be used 


## DELETE:
* For `delete` would be used 
* You can delete documents
* You can delete types
* You can delete indices