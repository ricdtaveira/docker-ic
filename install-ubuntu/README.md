### Instalação do Docker no Ubuntu

#### 1) Remover instalação anterior e atualizar

    $ sudo apt-get remove docker docker-engine docker.io

#### 2) Atualizar o indice de pacotes 

    $ sudo apt-get update

#### 3) Instalar os pacotes para permitir o apt usar um repositório usando o HTTPS:

       $ sudo apt-get install \        
              apt-transport-https \        
              ca-certificates \        
              curl \        
              software-properties-common

#### 4) Adicionar a chave GPG oficial do Docker:

        $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -    OK


#### 5) Verificar se chave correta foi instalada:

        $ sudo apt-key fingerprint 0EBFCD88      pub rsa4096 2017-02-22 [SCEA]            9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88      uid [ unknown] Docker Release (CE deb) <docker@docker.com>      sub rsa4096 2017-02-22 [S]

#### 6) Adicionar o repositorio apt do Docker usando o canal stable:

       $ sudo add-apt-repository \        
              "deb [arch=amd64] https://download.docker.com/linux/ubuntu \        
              $(lsb_release -cs) \        
              stable"

#### 7) Atualizar o indice do pacote apt assim, é incluído o repositório que foi adicionado:

       $ sudo apt-get update

#### 8) Instalar a ultima versão do Docker CE:

       $ sudo apt-get install docker-ce


#### 9) Verificar se a instalação funciona chamando o container hello-world:

       $ sudo docker container run hello-world




