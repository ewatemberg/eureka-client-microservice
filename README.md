# Echo Microservice
Como parte de la creación de nuestro servicio necesitamos una clase Java que contenga la funcionalidad necesaria. Crearemos la clase EchoService.java que estará anotada con @SpringBootApplication.
Puesto que queremos que nuestro servicio se registre en nuestro previamente creado servicio Eureka debemos anotarlo con @EnableDiscoveryClient tal y como se muestra a continuación.

```
package com.example.microservices.eurekaclient.eurekaclientmicroservice;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.client.discovery.EnableDiscoveryClient;

@EnableDiscoveryClient
@SpringBootApplication
public class EurekaClientMicroserviceApplication {

    public static void main(String[] args) {
        SpringApplication.run(EurekaClientMicroserviceApplication.class, args);
    }

}
```

Todos los microservicios que forman parte del sistema que estamos creando deben tener su configuración centralizada en un repositorio de Github (en nuestro ejemplo: [Repo](https://github.com/ewatemberg/spring-cloud-configuration-repository)). Para ello añadimos un nuevo archivo llamado echo-service.yml, en el cual añadiremos el puerto en el que queremos ejecutar el servicio (en nuestro caso 8091).

![alt text](https://raw.githubusercontent.com/ewatemberg/eureka-client-microservice/master/doc/img/repo.jpg)


![alt text](https://raw.githubusercontent.com/ewatemberg/spring-cloud-configuration-server-example/master/doc/img/java-microservices-with-netflix-oss-spring.jpg)

### Related
* [Spring Cloud Config](https://github.com/ewatemberg/spring-cloud-configuration-server-example)
* [Repositorio Configuración Centralizada](https://github.com/ewatemberg/spring-cloud-configuration-repository)
* [Servicio de Registro y Descubrimiento basado en Eureka](https://github.com/ewatemberg/eureka-discovery-server)
* [Servicio Gateway mediante Zuul](https://github.com/ewatemberg/zuul-gateway-server)

###### Fuente:
[Miguel Doctor Yuste](https://medium.com/@migueldoctor/spring-cloud-series-spring-cloud-config-server-con-github-paso-a-paso-135d2b4aaf4c)