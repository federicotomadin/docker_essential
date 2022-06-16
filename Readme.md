                           ***********  DOCKER  **********

**_Download docker desktop_**
https://www.docker.com/products/docker-desktop/

_**Docker Hub**_
https://hub.docker.com/

_**Documentation**_
https://docs.docker.com/

Download image

```sh
docker pull
```

Docker run tambien hace un pull si no tenés la imagen descargada

```sh
docker run
```

Listar las imagenes locales

```sh
docker images | head
```

Contenedores corriendo ahora

```sh
docker ps
```

Historial de contenedores que corrieron

```sh
docker ps -a
```

## LOGS

_-f: logs tiempo real_

```sh
docker logs <name_container>
docker logs -f <name_container>
```

## EXEC

Ejecuta un comando dentro del contenedor que esta corriendo

_i: interactivo
t: terminal
sh: shell_

```sh
docker exec
docker exec it sh
```

## START and STOP

```sh
docker start <conteiner_id>
docker sotp <conteiner_id>
```

## BUILD and RUN

_t: tag_

```sh
docker build -t <name_image>
```

_d: ditach_ -> significa que corre en background

```sh
docker run -d nginx
```

_p: port
d: ditach_

```sh
docker run -dp 3000:3000 <name_image>
```

## DOCKER HUB

```sh
docker login
```
