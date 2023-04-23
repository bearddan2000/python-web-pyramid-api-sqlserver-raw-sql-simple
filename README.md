# python-web-pyramid-api-sqlserver-raw-sql-simple

## Description
Simple web app that serves an api
for a pyramid project.

Uses sqlalchemy raw sql to query a table `dog`.

Remotely tested with *testify*.

## Tech stack
- python
  - pyramid
  - sqlalchemy
  - testify
  - requests
- mssql

## Docker stack
- python:latest
- mcr.microsoft.com/mssql/server:2017-CU17-ubuntu

## To run
`sudo ./install.sh -u`
- Get all dogs: http://localhost/dog
  - Schema id, breed, and color
- CRUD opperations
  - Create: curl -i -X PUT localhost/dog/<id>
  - Read: http://localhost/dog/<id>
  - Update: curl -i -X POST localhost/dog/<id>/<breed>/<color>
  - Delete: curl -i -X DELETE localhost/dog/<id>

## To stop (optional)
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
- [Pyramid setup](https://docs.pylonsproject.org/projects/pyramid/en/latest/index.html)
- [Sqlalchemy setup](https://docs.pylonsproject.org/projects/pyramid-cookbook/en/latest/database/sqlalchemy.html)
- [Json setup](https://docs.pylonsproject.org/projects/pyramid/en/latest/narr/renderers.html)