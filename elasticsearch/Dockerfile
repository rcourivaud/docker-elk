# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:5.6.3

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu

COPY ltr-es5.6.3.zip /usr/share/elasticsearch/

RUN echo "script.max_size_in_bytes: 10000000" >> config/elasticsearch.yml \
    && elasticsearch-plugin install file:///usr/share/elasticsearch/ltr-es5.6.3.zip --batch
