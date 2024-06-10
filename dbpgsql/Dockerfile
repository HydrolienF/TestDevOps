FROM postgres:14.1-alpine

# copy files required for the app to init tables
COPY *.sql /docker-entrypoint-initdb.d/

ENV POSTGRES_DB=db \
    POSTGRES_USER=hydrolien \
    POSTGRES_PASSWORD=pwd