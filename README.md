
Sistema para introduzir o conceito de mensageria  utilizando Spring Boot e Kafka.

## Tecnologias
 
- [Spring Boot](https://spring.io/projects/spring-boot)
- [Spring MVC](https://docs.spring.io/spring-framework/reference/web/webmvc.html)
- [Spring for Kafka](https://docs.spring.io/spring-kafka/reference/html/)
- [Kafka](https://kafka.apache.org)
- [Docker Compose](https://docs.docker.com/compose/)
- [Java 17]

## Como Executar

- Rodar o Kafka com o Docker Compose:
```
$ docker-compose up
```

- Adicionar /etc/hosts o hostname `kafka`.
- Clonar repositório git
- Construir o projeto:
```
$ ./mvnw clean package
```
- Executar a aplicação:
```
$ java -jar target/messaging-springboot-0.0.1-SNAPSHOT.jar
```

- Enviar um hello
```
$ http :8080/kafka/hello/Jardel

HTTP/1.1 200
Connection: keep-alive
Content-Length: 2
Content-Type: text/plain;charset=UTF-8
Date: Wed, 05 Jul 2023 16:21:05 GMT
Keep-Alive: timeout=60

OK
```

- Visualizar mensagem recebida no log:
```
Consumer Message: Olá, jardel 
```
