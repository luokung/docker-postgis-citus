# postgis-citus
基于Postgres的Dockerfile，包含Postgis GIS扩展、Citus 集群扩展，可用于构建docker镜像。

MERGE FROM
[postgres](https://github.com/docker-library/postgres)
[mdillon/postgis](https://github.com/appropriate/docker-postgis)
[citusdata/citus](https://github.com/citusdata/docker)