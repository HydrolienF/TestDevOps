Lancer docker en ouvrant docker desktop.

` ` affiche les containers stopé.
`docker rm 0123456789acbdef` supprime le conteneur en argument.
DB_PASWORLD=pwd
`docker build -t hydrolien/dbpgsql .`
`docker run -p 6000:5432 --name dbpgsql --network app-network -v /home/hydrolien/cours/s10/devops/tp1/app/data/:/var/lib/postgresql/data  hydrolien/dbpgsql` lance la base de donnée. `hydrolien/dbpgsql`, le nom du docker doit être a la fin.

tout sur le même network avec `--network app-network`

`docker build -t hydrolien/javaapp .`
`docker run --name javaapp -p 8080:8080 --network app-network hydrolien/javaapp`

Inspecter le réseau interne :
`docker network inspect app-network`

`docker build -t hydrolien/httpserver .`
`docker run --name httpserver -p 8888:80 --network app-network hydrolien/httpserver`

Launch docker compose with `docker compose up`