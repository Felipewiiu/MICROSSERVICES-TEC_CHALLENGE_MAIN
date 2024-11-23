<div align="center">
<a href="https://www.fiap.com.br" target="_blank">
    <img src="https://on.fiap.com.br/theme/fiap/postech/pos-tech.png" height="100px" alt="FIAP" class="center"/>
</a>

[![Java11](https://img.shields.io/badge/devel-Java-brightgreen)](https://docs.oracle.com/en/java/javase/11)
[![SpringBoot](https://img.shields.io/badge/framework-SpringBoot-brightgreen)](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle)
</div>

# MICROSSERVICE-TECCHALLENGE

## Apresentação:


## Para executar o projeto , siga os passos abaixo:

1. **Download do projeto no GitHub:**  Primeiro, faça o download do projeto a partir do repositório no GitHub. Você pode
   clonar o repositório usando o seguinte comando:

   ```shell
    git clone --recurse-submodule https://github.com/Felipewiiu/MICROSSERVICES-TEC_CHALLENGE_MAIN.git
   ```
4. **Pré-requisitos:**  Antes de executar o projeto, certifique-se de ter instalado os seguintes componentes:
   ```text  
   -   Maven (versão 3.x)
   -   Java 17
   -   PostgreSQL (versão 16.x)
   -   Makefile
    ```
5. **No diretório do projeto:**  Navegue até o diretório onde você clonou o projeto:
   ```shell
   cd MICROSSERVICES-TEC_CHALLENGE_MAIN
   ```
9. **Docker:** para subir os container Dokers basta seguir os comandos:

- Crie as váriáveis de ambiente (.env) :

```text
USER_POSTGRES=root
PASSWORD_POSTGRES=root
```
- com o comando a baixo adicione essas variáveis:
```shell
    docker-compose -f docker-compose.yaml config
```

- Para buildar as imagem, vá para o diretório de cada MICROSSERVICE e digite o comando abaixo PARA CRIAR AS IMAGENS DOCKER:
````shell
make docker-build

````
- Para subir os containers, vá para a raíz do projeto principal e digite:
````shell
make docker-start
````
- Para encerrar os containers
````shell
make docker-stop
````


