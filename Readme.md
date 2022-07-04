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
docker exec -it <imageId> sh
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

# INSTALL DOCKER EN WSL 2

## Uninstall previous versions

```sh
sudo apt-get remove docker docker-engine docker.io containerd runc
```

```sh
sudo apt-get update
```

## Install Docker Engine

```sh
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```

```sh
sudo mkdir -p /etc/apt/keyrings
```

```sh
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg
```

```sh
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```sh
sudo apt-get update
```

```sh
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

```sh
sudo service docker start
```

## Correct settings in Docker Desktop

![image.png](/.attachments/image-bc4aa844-02e6-4946-8789-9d2ade5e5b73.png)
