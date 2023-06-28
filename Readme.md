# Ejemplo de envio de datos entre Kafka y Elasticsearch + Kibana

### 0. Microservicios empleados

| Microservicio      | Descripcion |
| :----:             |    :----:   |
| Redpanda Server    | Title       |
| Redpanda Console   | Text        |
| Redpanda Connect   | Text        |
| ElasticSearch      | Text        |
| Kibana             | Text        |
| Distro             | Text        |


### 1. Desplegar contenedores

```docker compose up -d```

### 2. Cargar configuracion sink a Redpanda Connect
