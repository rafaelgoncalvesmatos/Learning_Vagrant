# Vagrant

Este repositorio vem para auxiliar na documentacao dos estudos referente a está solução da Hashicorp para provisionamento de recursos.

Muito fácil para construção de ambiente de POC.

## Indice

1. Basico
    * [basico1](./vagrant_code/01-Basico/basico1/Readme.md)
    * [basico2](./vagrant_code/01-Basico/basico2/Readme.md)
    * [basico3](./vagrant_code/01-Basico/basico3/Readme.md)

2. Intermediario
    * [intermediario1](./vagrant_code/02-Intermediario/inter1/Readme.md)
    * [intermediario2](./vagrant_code/02-Intermediario/inter2/Readme.md)
    * [intermediario3](./vagrant_code/02-Intermediario/inter3/Readme.md)
    * [intermediario4](./vagrant_code/02-Intermediario/inter4/Readme.md)
    * [intermediario5](./vagrant_code/02-Intermediario/inter5/Readme.md)

3. Avancado
    * [avancado1](./vagrant_code/03-Avancado/avanc1/Readme.md)
    * [avancado2](./vagrant_code/03-Avancado/avanc2/Readme.md)
    
4. Plugins
5. Truques
6. Provision

## Ajuda

Segue alguns links uteis.

Para achar a box que mais agrada:

> https://app.vagrantup.com/boxes/search

## Iniciando maquina

Para inicio de uma instancia segue exemplo.

Criar o arquivo com **Vagrantfile** que contem as configuracoes da nossa VM, neste caso ele ira definir que a box utilizada sera o centos 7:
```
$ vagrant init -m centos/7
```

O parametro -m e de minimal, nao contera os comentarios padroes.


Enfim, para iniciar a maquina apenas entre no diretorio de onde esta o arquivo **Vagrantfile** e levante a maquina virtual.
```
$ vagrant up
```

![](.images/img1.png)

## Acesso a maquina

Para acesso com este comando: 
```
$ vagrant ssh
```

Uma maquina especifica:
``` 
$ vagrant ssh elastic01
```

ou 
```
$ vagrant ssh a44
```

## Desligando maquina

Para desligamento apenas digite no mesmo diretorio:
```
$ vagrant halt
```

Para desligar uma maquina especifica obtenha o ID:
```
$ vagrant global-status
id       name    provider   state    directory                                                                   
-----------------------------------------------------------------------------------------------------------------
a44814a  default virtualbox running /home/rafa/Devops/github/Vagrant_exemplos/vagrant_code/01 - Simples/basico2 
 
The above shows information about all known Vagrant environments
on this machine. This data is cached and may not be completely
up-to-date (use "vagrant global-status --prune" to prune invalid
entries). To interact with any of the machines, you can go to that
directory and run Vagrant, or you can use the ID directly with
Vagrant commands from any directory. For example:
"vagrant destroy 1a2b3c4d"
```

Executando:

```
$ vagrant halt a44
```

## Destruindo

Para destruicao execute:
```
$ vagrant destroy 
```

Ou uma maquina especifica:
```
$ vagrant destroy a444
```

Para nao perguntar se vc tem certeza de remover execute com parametro **-f**:
```
$ vagrant destroy -f 
```

## Conclusao

Uma ferramente de curto aprendizado e com muito resultado para POC, Lab, estudos e documentacao de infraestrutura.
