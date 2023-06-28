# Ejemplo de envio de datos entre Kafka y Elasticsearch + Kibana

### 0. Microservicios empleados

| Microservicio      | Descripcion |
| :----:             |    :----:   |
| Redpanda Server    | Servidor Kafka donde se guardan los datos        |
| Redpanda Console   | Plataforma web para monitorizar el servidor Kafka        |
| Redpanda Connect   | Servidor de connectores sink y source        |
| ElasticSearch      | BBDD donde se almacenan los datos para representarlos en Kibana        |
| Kibana             | Dashboards        |
| Distro             | Servidor Python que consulta el precio de instantaneo de varias criptomonedas y lo envia al servidor Kafka        |


### 1. Desplegar contenedores

```docker compose up -d```

### 2. Cargar configuracion sink a Redpanda Connect
