# Feed Store Test
Easiest way to test the backend implementation is to use docker.

## Docker
See [docker-compose.yaml](./docker-compose.yaml) for the docker setup used for backend testing.

Execute the following commands in this directory, where [docker-compose.yaml](./docker-compose.yaml) is stored.

Start Backend:
`docker-compose up -d`

Stop Backend:
`docker-compose down`

Access Webserver:
http://localhost:48000/

Access PhpMyAdmin:
http://localhost:48080/
(Used for manual DB inspection)

MySQL data is stored in the subdirectories:
* `/test/dbdata`
* `/test/dblog`

If you want to have a clean start, delete all contents of those two folders, except for the `.gitkeep` files.


## Automated Tests

TODO
