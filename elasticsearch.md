# Elasticsearch cheatsheets

## Curl commands

GET to retrieve all indices
```sh
curl -X GET "http://localhost:9200/_cat/indices"
```

GET to retrive the mappings of an index
```sh
curl -X GET "http://localhost:9200/[index_name]/_mappings"
```
