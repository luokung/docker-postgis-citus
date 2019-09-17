# postgis-citus
基于Postgres的Dockerfile，包含Postgis GIS扩展、Citus 集群扩展，可用于构建docker镜像。

MERGE FROM
[postgres](https://github.com/docker-library/postgres)
[mdillon/postgis](https://github.com/appropriate/docker-postgis)
[citusdata/citus](https://github.com/citusdata/docker)

## build Postgres10
```bash
cd 10/
docker build -t luokung/postgis-citus:10 .
```

## build Postgres10-alpine
```bash
cd 10/
docker build -t luokung/postgis-citus:10-alpine . -f Dockerfile-alpine
```

## build Postgres11
```bash
cd 11/
docker build -t luokung/postgis-citus:11 .
```

## build Postgres11-alpine
```bash
cd 11/
docker build -t luokung/postgis-citus:11-alpine . -f Dockerfile-alpine
```

# version view
select version();
> PostgreSQL 10.7 on x86_64-pc-linux-musl, compiled by gcc (Alpine 8.2.0) 8.2.0, 64-bit

select postgis_full_version();
> POSTGIS="2.5.2" [EXTENSION] PGSQL="100" GEOS="3.7.1-CAPI-1.11.1 27a5e771" PROJ="Rel. 5.2.0, September 15th, 2018" GDAL="GDAL 2.4.0, released 2018/12/14" LIBXML="2.9.9" LIBJSON="0.13.1" LIBPROTOBUF="1.3.0" TOPOLOGY RASTER

select citus_version();
> Citus 8.3.2 on x86_64-pc-linux-gnu, compiled by gcc (Alpine 8.3.0) 8.3.0, 64-bit
