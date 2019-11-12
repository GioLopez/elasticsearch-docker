
# Insert data on Elastic and search

## Inserting data

```
curl -X POST -H "Content-Type:application/json" "http://localhost:9200/producto/deportes?pretty" -d\
'{
	"codigo": "EVENT000000001",
	"nombre": "Junior Tu Papá",
	"descripcion": "Junior se enfrentará a Tolima",
	"url_imagen": "http://juniorfc.com",
	"ciudad": "Barranquilla",
	"precio": 100000,
	"fecha_espectaculo": "2019-10-28T12:40:44.881Z",
	"fecha_llegada": "2019-10-27T20:40:44.881Z",
	"fecha_salida": "2019-10-28T20:40:44.881Z"
}'
```


```
curl -X POST -H "Content-Type:application/json" "http://localhost:9200/producto/deportes?pretty" -d\
'{
	"codigo": "EVENT000000002",
	"nombre": "Rey de copas",
	"descripcion": "Nacional se enfrentará al Cucuta",
	"url_imagen": "http://nacional.com",
	"ciudad": "Medellin",
	"precio": 90000,
	"fecha_espectaculo": "2019-10-28T12:40:44.881Z",
	"fecha_llegada": "2019-10-27T20:40:44.881Z",
	"fecha_salida": "2019-10-28T20:40:44.881Z"
}'
```
## Search

```
curl -H "Content-Type:application/json" "http://localhost:9200/producto/deportes_search?q=nombre:Rey"
```


```
curl -H "Content-Type:application/json" "http://localhost:9200/producto/deportes/_search?q=nombre:junior&pretty"
```

```
curl -H "Content-Type:application/json" "http://localhost:9200/producto/deportes/_search?q=codigo:*001&pretty"
```

# Reference

- [Instal Elastic with docker](https://www.elastic.co/guide/en/elastic-stack-get-started/current/get-started-docker.html#get-started-docker-tls)
- [Search with Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/search-search.html)
