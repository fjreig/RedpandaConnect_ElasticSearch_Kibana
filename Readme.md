# Ejemplo de envio de datos entre Kafka y Elasticsearch + Kibana

### 0. Microservicios empleados

| Microservicio      | Descripcion |
| :----:             |    :----:   |
| Redpanda Server    | Servidor Kafka donde se guardan los datos        |
| Redpanda Console   | Plataforma web para monitorizar el servidor Kafka        |
| Redpanda Connect   | Servidor de connectores sink y source        |
| ElasticSearch      | BBDD donde se almacenan los datos para representarlos en Kibana        |
| Kibana             | Dashboards para la representacion de datos almacenados en Elasticsearch       |
| Distro             | Servidor Python que consulta el precio de instantaneo de varias criptomonedas y lo envia al servidor Kafka        |


### 1. Desplegar contenedores

```docker compose up -d```

### 2. Comprobamos el estado del cluster de Kafka

```docker exec -it redpanda rpk cluster info```

### 3. Comprobamos el estado de la BBDD

``` curl 'http://localhost:9200' ```

### 2. Cargar configuracion sink a Redpanda Connect

Accedemos a http://localhost:8080/connect-clusters/local-connect-cluster y añadimos un nuevo connector del tipo ElasticsearchSinkConnector
