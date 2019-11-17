# Vagrant

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

## Conclusao

Uma ferramente de curto aprendizado e com muito resultado para POC, Lab, estudos e documentacao de infraestrutura.