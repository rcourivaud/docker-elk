ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu

COPY ltr-es5.6.3.zip /usr/share/elasticsearch/

RUN echo "script.max_size_in_bytes: 10000000" >> config/elasticsearch.yml \
    && elasticsearch-plugin install file:///usr/share/elasticsearch/ltr-es5.6.3.zip --batch
