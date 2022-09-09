ARG ELASTIC_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELASTIC_VERSION}

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
RUN echo ${MINIO_ACCESS_KEY} | bin/elasticsearch-keystore add --stdin --force s3.client.default.access_key
RUN echo ${MINIO_SECRET_KEY} | bin/elasticsearch-keystore add --stdin --force s3.client.default.secret_key