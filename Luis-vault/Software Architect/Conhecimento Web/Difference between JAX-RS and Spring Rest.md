## JAX-RS

JAX-RS is a [specification](http://download.oracle.com/otn-pub/jcp/jaxrs-2_0-fr-eval-spec/jsr339-jaxrs-2.0-final-spec.pdf) for implementing REST web services in Java, currently defined by the [JSR-370](https://jcp.org/en/jsr/detail?id=370). It is part of the [Java EE technologies](https://stackoverflow.com/a/37083274/1426227), currently defined by the [JSR 366](https://www.jcp.org/en/jsr/detail?id=366).

[Jersey](https://jersey.java.net/) (shipped with GlassFish and Payara) is the JAX-RS reference implementation, however there are other implementations such as [RESTEasy](http://resteasy.jboss.org/) (shipped with JBoss EAP and WildFly) and [Apache CXF](https://cxf.apache.org/) (shipped with TomEE and WebSphere).

## Spring Framework

The [Spring Framework](http://projects.spring.io/spring-framework/) is a [full framework](http://docs.spring.io/spring/docs/current/spring-framework-reference/html/overview.html) that allows you to create Java enterprise applications. The REST capabilities are provided by the [Spring MVC](https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html) module (same module that provides _model-view-controller_ capabilities). It is not a JAX-RS implementation and can be seen as a Spring alternative to the JAX-RS standard.

The Spring ecosystem also provides a [wide range of projects](https://spring.io/projects) for creating enterprise applications, covering persistence, security, integration with social networks, batch processing, etc.

## Examples

Consider the following resource controller using the JAX-RS API:

```java
@Path("/greetings")
public class JaxRsController {

    @GET
    @Path("/{name}")
    @Produces(MediaType.TEXT_PLAIN)
    public Response greeting(@PathParam("name") String name) {

        String greeting = "Hello " + name;
        return Response.ok(greeting).build();
    }
}
```

The equivalent implementation using the Spring MVC API would be:

```java
@RestController
@RequestMapping("/greetings")
public class SpringRestController {

    @RequestMapping(method = RequestMethod.GET,
                    value = "/{name}", 
                    produces = MediaType.TEXT_PLAIN_VALUE)
    public ResponseEntity<?> greeting(@PathVariable String name) {

        String greeting = "Hello " + name;
        return new ResponseEntity<>(greeting, HttpStatus.OK);
    }
}
```

## Using Spring Boot and Jersey

Spring Boot provides the [`spring-boot-starter-jersey`](http://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-developing-web-applications.html#boot-features-jersey) module that allows you to use the JAX-RS programming model for the REST endpoints instead of Spring MVC. It works quite well with Jersey 2.x.