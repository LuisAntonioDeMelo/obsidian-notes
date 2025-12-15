
Stateless e StateFull

**Stateless** 
quando o cliente já sabe todas as informações necessárias para fazer o request, com a api, ou seja cada request feito pelo cliente deve toda as informações necessários para aquele metodo Http

**Statefull** 
 e quando um o cliente guarda os dados desse usuário no servidor 

Explain Http Methods 
Crud 
- Get  - fetch 
- Post - envida dados para o request
- Put - atualiza os dados
- Delete  - deleta

Http Status codes 
503 internal server // 500 server side error
200 ok 201 create  etc. 
400 not foud // cliente side error 
404 error

Uri - significa Uniforme Resource Identificador (Identificador uniforme de recursos)
urn - como um unico dado do recurso como isbn 
url - como endereço da web 

**Best practices in making URI for RESTful web services**

desenvolver com entendimento que 4 barras significam uma mais alta hierarquia
usar substantivos plurais para ramificações
utilizar hifens para múltiplas palavras
letras minúsculas 
evitar utilizar extensões de arquivos 

**Differences between REST and SOAP?**

Rest e uma arquitetura para desenvolver web services 
Soap - Simple Object Acess Protocol  : serve para trocar informações estruturadas por meio de apis
Enquanto rest tem padrões flexiveis, os padroes soap são muito mais rigido e sua implementação e seus "statefullness" siginificam que o cliente e servidor estão mais conectados 
adicionalmente enquanto rest permite transferência de dados em Json,XML e outros, o SOAP so permite XML
soap é uma versão mais restriviva do rest


**Differences between REST and AJAX?**

Ajax - Asynchronous Javascript and XML

É uma coleção de tecnologia que permitem aplicativos assíncronos da web 
usando  o objeto de solicitação Http XML integrado 

Rest Api é uma arquitetura pra lidar com as solicitações de request Http 
Ajax refere-se a uma coleção de tecnologias web para fazer solicitações 
web assíncronas, isso significa que uma API rest pode lidar com clientes Ajax 
por fazer restfull request, mas uma api nunca podera ser implementada por um ajax

**Tools to develop and test REST APIs**

as ferramentas são variadas, dependendo da linguagem, caso, frameworks 
como express para o nodejs, ou springboot para o java 

para teste existem ferramentas como o postman 

**What are real-world examples of Rest APIs ?"**

Quase todos faces da web, utilizam mais comum usadas para manipular data  etc 

Advantages and Cons 

Advantages >>
- Easy to learn 
- Wide range of data transfers 
- Statelessness
- Scalability 
Disadvantages >>
- Lack of built-in security 
- Need to be versioned for backwards compatibility 
- Consistency in URis dificult to maintain for complex projects 
-