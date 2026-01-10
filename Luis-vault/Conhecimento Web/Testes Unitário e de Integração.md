Testes unitários e de integração são dois tipos fundamentais de testes de software, cada um com objetivos e características distintas. A seguir, explicarei cada tipo e fornecerei exemplos em Java para ilustrar como eles podem ser implementados.

### Testes Unitários

Os testes unitários focam na verificação de unidades individuais de código, como métodos ou classes, de forma isolada. O objetivo é garantir que cada unidade funcione conforme o esperado.

#### Exemplo de Teste Unitário

Suponha que temos uma classe `Calculator` com métodos para adicionar e subtrair números.

##### Classe a Ser Testada

java

Copiar código

`public class Calculator {     public int add(int a, int b) {         return a + b;     }      public int subtract(int a, int b) {         return a - b;     } }`

##### Classe de Teste Unitário

Usando JUnit 5, aqui está um exemplo de teste unitário para a classe `Calculator`:

java

Copiar código

`import static org.junit.jupiter.api.Assertions.assertEquals; import org.junit.jupiter.api.Test;  public class CalculatorTest {      private final Calculator calculator = new Calculator();      @Test     public void testAdd() {         assertEquals(5, calculator.add(2, 3));         assertEquals(0, calculator.add(-1, 1));     }      @Test     public void testSubtract() {         assertEquals(1, calculator.subtract(3, 2));         assertEquals(-2, calculator.subtract(-1, 1));     } }`

### Testes de Integração

Os testes de integração verificam a interação entre múltiplos componentes ou sistemas, como a interação entre classes, módulos ou serviços externos (por exemplo, banco de dados, APIs).

#### Exemplo de Teste de Integração

Suponha que temos um serviço `UserService` que interage com um repositório de banco de dados `UserRepository`.

##### Classe de Serviço

java

Copiar código

`public class UserService {     private final UserRepository userRepository;      public UserService(UserRepository userRepository) {         this.userRepository = userRepository;     }      public User getUserById(int id) {         return userRepository.findById(id).orElse(null);     }      public void saveUser(User user) {         userRepository.save(user);     } }`

##### Interface do Repositório

java

Copiar código

`import java.util.Optional;  public interface UserRepository {     Optional<User> findById(int id);     void save(User user); }`

##### Classe de Entidade

java

Copiar código

`public class User {     private int id;     private String name;      // construtores, getters e setters }`

##### Configuração de Teste de Integração com Spring Boot

Usando Spring Boot e JUnit 5 para configurar um teste de integração:

###### Dependências no `pom.xml`

xml

Copiar código

`<dependency>     <groupId>org.springframework.boot</groupId>     <artifactId>spring-boot-starter-data-jpa</artifactId> </dependency> <dependency>     <groupId>org.springframework.boot</groupId>     <artifactId>spring-boot-starter-test</artifactId>     <scope>test</scope> </dependency> <dependency>     <groupId>com.h2database</groupId>     <artifactId>h2</artifactId>     <scope>test</scope> </dependency>`

###### Configuração do Repositório

java

Copiar código

`import org.springframework.data.jpa.repository.JpaRepository;  public interface UserRepository extends JpaRepository<User, Integer> { }`

###### Classe de Teste de Integração

java

Copiar código

`import org.junit.jupiter.api.Test; import org.springframework.beans.factory.annotation.Autowired; import org.springframework.boot.test.autoconfigure.orm.jpa.DataJpaTest; import org.springframework.boot.test.context.SpringBootTest; import org.springframework.test.context.junit.jupiter.SpringExtension;  import static org.junit.jupiter.api.Assertions.assertEquals; import static org.junit.jupiter.api.Assertions.assertNotNull;  @SpringBootTest public class UserServiceIntegrationTest {      @Autowired     private UserService userService;      @Autowired     private UserRepository userRepository;      @Test     public void testSaveAndGetUser() {         User user = new User();         user.setName("John Doe");         userService.saveUser(user);          User retrievedUser = userService.getUserById(user.getId());         assertNotNull(retrievedUser);         assertEquals("John Doe", retrievedUser.getName());     } }`

### Explicação

1. **Teste Unitário**:
    
    - O foco está em métodos individuais (`add` e `subtract`).
    - Não há dependências externas, e o teste é rápido e isolado.
2. **Teste de Integração**:
    
    - O foco está na interação entre `UserService` e `UserRepository`.
    - Usa um banco de dados em memória (H2) para simular a persistência real.
    - Verifica se as operações de salvar e recuperar um usuário funcionam corretamente em conjunto.

### Considerações Finais

- **Testes Unitários**:
    
    - Rápidos e isolados.
    - Usam mocks para substituir dependências externas.
    - Verificam a funcionalidade de métodos individuais.
- **Testes de Integração**:
    
    - Podem ser mais lentos devido à inicialização de contextos e interação com componentes externos.
    - Testam a interação entre vários componentes.
    - Verificam se o sistema funciona como um todo.

Ambos os tipos de testes são essenciais para uma cobertura de teste robusta. Os testes unitários garantem que cada unidade de código funcione corretamente, enquanto os testes de integração garantem que as unidades funcionem corretamente quando combinadas.

O Mockito é uma das bibliotecas mais populares para a criação de testes unitários em Java. Ele oferece várias anotações que simplificam a criação e a configuração de objetos simulados (mocks). A seguir, descrevo as principais anotações do Mockito e como utilizá-las.

### 1. @Mock

A anotação `@Mock` é usada para criar mocks de classes e interfaces. Esses mocks podem ser configurados para simular comportamentos específicos durante os testes.

java

Copiar código

``` java
import static org.mockito.Mockito.*; import org.mockito.Mock; import org.junit.jupiter.api.BeforeEach; import org.junit.jupiter.api.Test; import org.mockito.MockitoAnnotations;  

public class ExampleTest {     

@Mock     
private MyService myService;      

@BeforeEach     
public void setUp() {        
	MockitoAnnotations.initMocks(this);     
}     
@Test    
public void testSomething() {
	when(myService.someMethod()).thenReturn("Mocked Value");          
	String result = myService.someMethod();         
	assertEquals("Mocked Value", result);     
	} 
}`
````

### 2. @InjectMocks

A anotação `@InjectMocks` é usada para criar e injetar mocks nos campos de uma classe que está sendo testada. O Mockito tenta injetar os mocks utilizando construtores, métodos setters ou diretamente nos campos.

java

Copiar código

`import static org.mockito.Mockito.*; import org.mockito.InjectMocks; import org.mockito.Mock; import org.junit.jupiter.api.BeforeEach; import org.junit.jupiter.api.Test; import org.mockito.MockitoAnnotations;  public class ExampleTest {      @Mock     private MyService myService;      @InjectMocks     private MyController myController;      @BeforeEach     public void setUp() {         MockitoAnnotations.initMocks(this);     }      @Test     public void testSomething() {         when(myService.someMethod()).thenReturn("Mocked Value");          String result = myController.callServiceMethod();         assertEquals("Mocked Value", result);     } }`

### 3. @Spy

A anotação `@Spy` é usada para criar espiões (spies) de objetos reais. Ao contrário dos mocks, os espiões chamam os métodos reais do objeto a menos que sejam explicitamente simulados.

java

Copiar código

`import static org.mockito.Mockito.*; import org.mockito.Spy; import org.junit.jupiter.api.BeforeEach; import org.junit.jupiter.api.Test; import org.mockito.MockitoAnnotations;  public class ExampleTest {      @Spy     private MyService myService = new MyService();      @BeforeEach     public void setUp() {         MockitoAnnotations.initMocks(this);     }      @Test     public void testSomething() {         doReturn("Spied Value").when(myService).someMethod();          String result = myService.someMethod();         assertEquals("Spied Value", result);     } }`

### 4. @Captor

A anotação `@Captor` é usada para criar instâncias de `ArgumentCaptor`, que são úteis para capturar e verificar os argumentos passados para métodos simulados.

java

Copiar código

`import static org.mockito.Mockito.*; import org.mockito.Captor; import org.mockito.Mock; import org.junit.jupiter.api.BeforeEach; import org.junit.jupiter.api.Test; import org.mockito.ArgumentCaptor; import org.mockito.MockitoAnnotations;  public class ExampleTest {      @Mock     private MyService myService;      @Captor     private ArgumentCaptor<String> captor;      @BeforeEach     public void setUp() {         MockitoAnnotations.initMocks(this);     }      @Test     public void testSomething() {         myService.process("Hello");          verify(myService).process(captor.capture());         assertEquals("Hello", captor.getValue());     } }`

### 5. @RunWith(MockitoJUnitRunner.class)

A anotação `@RunWith(MockitoJUnitRunner.class)` é usada com o JUnit 4 para inicializar automaticamente os mocks anotados com `@Mock`, `@Spy`, `@InjectMocks` e `@Captor`.

java

Copiar código

`import static org.mockito.Mockito.*; import org.junit.Test; import org.junit.runner.RunWith; import org.mockito.InjectMocks; import org.mockito.Mock; import org.mockito.junit.MockitoJUnitRunner;  @RunWith(MockitoJUnitRunner.class) public class ExampleTest {      @Mock     private MyService myService;      @InjectMocks     private MyController myController;      @Test     public void testSomething() {         when(myService.someMethod()).thenReturn("Mocked Value");          String result = myController.callServiceMethod();         assertEquals("Mocked Value", result);     } }`

### 6. MockitoExtension

Para JUnit 5, você pode usar `MockitoExtension` para habilitar a injeção de mocks. Isso é feito com a anotação `@ExtendWith(MockitoExtension.class)`.

java

Copiar código

`import static org.mockito.Mockito.*; import org.junit.jupiter.api.Test; import org.junit.jupiter.api.extension.ExtendWith; import org.mockito.InjectMocks; import org.mockito.Mock; import org.mockito.junit.jupiter.MockitoExtension;  @ExtendWith(MockitoExtension.class) public class ExampleTest {      @Mock     private MyService myService;      @InjectMocks     private MyController myController;      @Test     public void testSomething() {         when(myService.someMethod()).thenReturn("Mocked Value");          String result = myController.callServiceMethod();         assertEquals("Mocked Value", result);     } }`

### Considerações Finais

- **@Mock**: Cria um mock de uma classe ou interface.
- **@InjectMocks**: Cria uma instância da classe e injeta os mocks criados com `@Mock` ou `@Spy`.
- **@Spy**: Cria um espião de um objeto real, permitindo chamar métodos reais a menos que sejam simulados.
- **@Captor**: Cria um `ArgumentCaptor` para capturar argumentos de métodos simulados.
- **@RunWith(MockitoJUnitRunner.class)**: Utilizado no JUnit 4 para inicializar mocks.
- **@ExtendWith(MockitoExtension.class)**: Utilizado no JUnit 5 para inicializar mocks.

Essas anotações ajudam a simplificar e tornar mais legível a configuração e o uso de mocks em seus testes unitários com Mockito.


os testes unitarios 

//arrange - crio meus mocks
//act - chamos as funcionalidade e funções
//assert  - faço as verificações 

argument captor
para assegurar os dados que estão passando 

o argument captor, ele captura o argumento dentro de um paramentro
dentro de um metodo, ele utiliza o generics para verificar o objeto que eu
estou passando 

exemplo eu quero testar se eu to persistindo com os dados 
entao 