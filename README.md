<div align="center">
<a href="https://www.fiap.com.br" target="_blank">
    <img src="https://on.fiap.com.br/theme/fiap/postech/pos-tech.png" height="100px" alt="FIAP" class="center"/>
</a>

[![Java11](https://img.shields.io/badge/devel-Java-brightgreen)](https://docs.oracle.com/en/java/javase/11)
[![SpringBoot](https://img.shields.io/badge/framework-SpringBoot-brightgreen)](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle)
[![Docker](https://img.shields.io/badge/container-Docker-brightgreen)](https://www.docker.com)
</div>


# TRABALHO DE CONCLUSÃO - FASE 4 # - ARQUITETURA, SERVERLESS e SPRING

## Sistema de Gerenciamento de Pedidos Integrado com Spring e Microsserviços.

----
Este sistema de gerenciamento de pedidos altamente eficiente, que explora profundamente
a arquitetura de microsserviços utilizando o ecossistema Spring.
Este sistema abrange desde a gestão de clientes e produtos até o processamento e entrega de pedidos,
enfatizando a autonomia dos serviços, comunicação eficaz, e persistência de dados isolada.

### Detalhamento dos microserviços:

#### Microsserviço de Gerenciamento de Clientes

- **Descrição Funcional:**
  Responsável por todas as operações relacionadas aos clientes, incluindo a criação, leitura, atualização e
  exclusão de registros de clientes

#### Microsserviço de Catálogo de Produtos

- **Descrição Funcional:**
  Responsável por gerenciar o catálogo de produtos, incluindo informações 
detalhadas dos produtos e o controle de estoque.

#### Microsserviço de Gestão de Pedidos

- **Descrição Funcional:**
  Responsável por centralizar o processamento de todos os pedidos, desde a 
criação até a conclusão. Isso inclui receber pedidos dos clientes, 
processar pagamentos , e coordenar com o microsserviço de logística de 
entrega para garantir a entrega eficiente dos produtos.

#### Microsserviço de Logística de Entrega

- **Descrição Funcional:**
  Responsável por cuidar de toda a logística relacionada à entrega de pedidos, 
- desde a atribuição de entregadores até o rastreamento das entregas.

### Links úteis
- [URL da API para se usar o POSTMAN](https://lively-moon-837353.postman.co/workspace/08fb73dc-c7f8-41fa-b4f9-772c5ffc1c6c/collection/16007703-cbf1378b-cabe-4771-af56-30d0f3c73888?utm_source=email&utm_medium=view_collection)


## Para executar o projeto , siga os passos abaixo:

1. **Download do projeto no GitHub:**  Primeiro, faça o download do projeto a partir do repositório no GitHub. Você pode
   clonar o repositório usando o seguinte comando:

   ```shell
   $ git clone https://github.com/Felipewiiu/MICROSSERVICES-TEC_CHALLENGE_MAIN.git
   ```
2. **Pré-requisitos:**  Antes de executar o projeto, certifique-se de ter instalado os seguintes componentes:
   ```shell  
   -   Maven (versão 3.x)
   -   Java 17
   -   PostgreSQL (versão 16.x)
    ```
3. **No diretório do projeto:**  Navegue até o diretório onde você clonou o projeto:
   ```shell
   cd MICROSSERVICES-TEC_CHALLENGE_MAIN
   ```
4. **No diretório do EUREKA-SERVER:**  Navegue até o diretório onde você clonou o microserviço:
   ```shell
   cd EUREKA-SERVER
   ```
5. **Compilando e empacotando com o Maven:**  Execute o seguinte comando para compilar o projeto e gerar o arquivo JAR:
   ```shell
   mvn clean package
   ```
6. **Executando a aplicação:**  Agora, inicie a aplicação com o seguinte comando:
   ```shell
   java -jar target/EurekaServer-1.0-SNAPSHOT.jar
   ```
   
7. **Retorne a Raiz do Sistema:**  Execute o seguinte comando:
   ```shell
   cd ..
   ```
8. **Para subir o API GATEWAY e os microserviços, repita dos passos 4,5 e 6** Fazendo os mesmos passos porém com os comandos abaixo:

8.1. Api Gateway

    cd API-GATEWAY
    mvn clean package
    java -jar target/ApiGateway-1.0-SNAPSHOT.jar
    cd ..

8.2. MS-CLIENT

    cd MS-CLIENT
    mvn clean package
    java -jar target/MS-CLIENTE-1.0-SNAPSHOT.jar
    cd ..

8.3. MS-LOGISTICA

    cd MS-LOGISTICA
    mvn clean package
    java -jar target/ms-logistica-1.0-SNAPSHOT.jar
    cd ..

8.4. MS-PEDIDOS

    cd ms-pedidos
    mvn clean package
    java -jar target/MS-ORDER-1.0-SNAPSHOT.jar
    cd ..

8.5. MS-PRODUCT_CATALOG

    cd MS-LOGISTICA
    mvn clean package
    java -jar target/MS-PRODUCT-MANAGEMENT-1.0-SNAPSHOT.jar
    cd ..

9. **Docker:** para subir os container Dokers basta seguir os comandos:

- Para buildar a imagem
````shell
make docker-build

````
- Para subir os containers
````shell
make docker-start
````
- Para encerrar os containers
````shell
make docker-stop
````

## Testes Unitários:

Testes Unitários:
Os testes unitários são responsáveis por validar o comportamento isolado de cada unidade do sistema, garantindo que cada
componente funcione conforme o esperado.

Para executar os testes unitários do projeto, siga os passos abaixo:

Compilar o projeto: Antes de rodar os testes, certifique-se de compilar o projeto com o comando:

```shell
mvn compile
 ```

Testes Unitários:
Os testes unitários garantem que cada unidade do código funcione corretamente de forma isolada.

- Para rodar os testes unitários, execute o comando:

```shell
make unit-test
 ```

## Testes Integrados e Inspeção de Código:

Testes de Integração:
Os testes de integração verificam a interação entre diferentes componentes do sistema.

- Para executar os testes de integração, utilize o comando:

```shell
make integration-test
 ```

## Testes de Integração no Controller, CI e BDD:

Testes de Sistema:
Esses testes garantem que o sistema como um todo esteja funcionando de maneira correta em um ambiente que simule o de
produção. O cucumber com bdd estao testando o fluxo d ponta a ponta.


- Para executar os testes de sistema, utilize o seguinte comando:
- OBS: Para executar os testes de sistemas é preciso que a API esteja rodando

```shell
make system-test
 ```

## Executando todos os testes

- Se você deseja executar todas as categorias de testes (unitários, de integração e de sistema), pode utilizar o
  seguinte comando:

```shell
make test 
```


### C) Participantes

- RM353873 - Kleuber Costa
- RM354111 - Felipe Oliveira
- RM354482 - Letícia Oliveira
- RM354525 - Marcello Caseiro
- RM355621 - Paulo Bof
  
  


