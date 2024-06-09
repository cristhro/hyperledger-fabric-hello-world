### Configuración en el servidor de Google
1. Actualizar el sistema
```warp-runnable-command
sudo apt update && sudo apt upgrade -y
```
2. Instalación de Git 
```warp-runnable-command
sudo apt install git
git --version
```
3. COMPROBAR SI ESTÁ INSTALADO CURL 
```warp-runnable-command
curl --version 
```
4. INSTALAR DOCKER
```warp-runnable-command
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo docker run hello-world
```
5. Configuración de docker para ser ejecutado por usuario local
```warp-runnable-command
sudo groupadd docker
sudo usermod -aG docker $USER
logout
```
6. Instalar go
```warp-runnable-command
sudo apt install golang-go
go version
```
7. Instalar NPM
```warp-runnable-command
sudo apt install npm
npm --version
```
8. Instalar Docker compose
```warp-runnable-command
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
```
9. DESCARGA REPOSITORIO Y BINARIOS \(Fabric\)
```warp-runnable-command
curl -sSL https://bit.ly/2ysbOFE | bash -s -- 2.3.2 1.5.2
cd fabric-samples
ls bin
```
10. ARRANCAR PRIMER EJEMPLO
    1. Se genera las dos universidades
```warp-runnable-command
cd fabric-samples/test-network

./network.sh down

export COMPOSE_PROJECT_NAME=net

./network.sh up
```
11. COMPROBAR DOCKERS
    1. Lista los contenedores generados 
```warp-runnable-command
docker ps -a
```
12. CREAR CANAL DE COMUNICACIÓN
    1. Instalacion de Vim
    2. Modificar channelID
```warp-runnable-command

vi scripts/createChannel.sh

./network.sh createChannel

sudo docker ps -a
```

