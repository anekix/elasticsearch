<b> Index a document

```python
 curl -XPUT 'http://localhost:9200/twitter/tweet/1' -d '{
    "user" : "kimchy",
    "post_date" : "2009-11-15T14:12:12",
    "message" : "trying out Elasticsearch"
}'
```
<b> Get a document by id
```python
curl -XGET 'localhost:9200/customer/external/1?pretty'
{
  "_index" : "customer",
  "_type" : "external",
  "_id" : "1",
  "_version" : 1,
  "found" : true,
  "_source" : { "name": "John Doe" }
}
```
<b>Get only specific fields from search results</b>
```python
curl -XGET 'http://localhost:9200/twitter/tweet/1?fields=title,content'
```
<b>Get only the source field in search results , exclude extra fields </b>
```python
curl -XGET 'http://localhost:9200/twitter/tweet/1/_source'
```
