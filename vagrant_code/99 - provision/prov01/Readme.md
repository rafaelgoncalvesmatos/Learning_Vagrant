# Welcome to Vagrant ;) !

Uso de provision, neste exemplo iremo subir uma maquina ja realizando um docker pull de uma imagem.

Referencias:
https://www.vagrantup.com/docs/provisioning/docker.html

## Acesso

Para acessar container provisionado pelo vagrant é simples:
````
vagrant docker-exec -t default -- bash
````

Ou dessa forma:
````
vagrant docker-exec -it -- /bin/sh
#
````

Notasse que ele ja esta no container utilizando o zsh

## Comandos de status

Continua sendo o mesmo:

````
vagrant status
Current machine states:

default                   running (docker)
````

No terminal podemos digitar o docker ps para visualizar informacoes do container:
````
XPSPMAC-025023:prov01 u001956$ docker ps -a
 CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
ffb423eec680        redis               "docker-entrypoint.s…"   6 minutes ago       Up 6 minutes        6379/tcp            prov01_default_1574109115
````


