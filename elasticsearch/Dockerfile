# Используем официальный образ Elasticsearch с указанной версией
ARG ELASTIC_VERSION
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELASTIC_VERSION}

# Переключаемся на root для выполнения команды
USER root

# Устанавливаем владельца файла конфигурации
RUN chown elasticsearch:elasticsearch /usr/share/elasticsearch/config/elasticsearch.yml

# Возвращаемся к пользователю elasticsearch
USER elasticsearch

# Экспортируем необходимые порты
EXPOSE 9200 9300
