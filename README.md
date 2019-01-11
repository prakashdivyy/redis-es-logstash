# redis-es-logstash

Logstash docker container that using Redis as input and Elasticsearch as output

## Getting Started
These instructions will cover usage information and for the docker container

### Prerequisities

In order to run this container you'll need docker installed.

* [Windows](https://docs.docker.com/windows/started)
* [OS X](https://docs.docker.com/mac/started/)
* [Linux](https://docs.docker.com/linux/started/)

### Steps

#### Build container

```shell
docker build . -t=redis-es-logstash
```

#### Run container

```shell
docker run --rm -it --env REDIS_HOST --env REDIS_DATA_TYPE --env REDIS_KEY --env REDIS_PORT --env ELASTICSEARCH_URL redis-es-logstash:latest
```

#### Environment Variables

* `REDIS_HOST` - Redis Hostname
* `REDIS_DATA_TYPE` - Redis data type for input ([more](https://www.elastic.co/guide/en/logstash/current/plugins-inputs-redis.html#plugins-inputs-redis-data_type))
* `REDIS_KEY` - Redis Key
* `REDIS_PORT` - Redis Port
* `ELASTICSEARCH_URL` - Elasticsearch url