Bom os bancos de dados são componentes vitais no desenvolvimento de software 
eles estão em praticamente quase todos os sistemas de software, algumas exceções
sistemas embarcados, ou que gerenciam a própria memoria 

desempenham um papel fundamental no gerenciamento e armazenamento de dados
de estoques, sistemas bancários assim como comercio eletrônico e etc..

na arquitetura de software e uma área muito importante pois gera muito impacto e influencia muito na solução proposta.


# Os tipos de Bancos de Dados 

SQL - Relacionais 
Existem diversas maneiras de trabalhar com bancos relacionais, 
os Sistemas são conhecidos como Sistemas de Gerenciamento de Banco de Dados Relacionais (SGBDR) - ou Relational Database Management Systems (RDBMS) 

São os mais difundidos e utilizados no mercado desde os anos 70, como Oracle, Mysql, SqlServer, Postgres entre outros.  uma característica principal e utilizar o SQL a linguagem de consulta, Structured Query Language) para consulta e definição do dados

NoSql - Não relacionais 
Ja nos bancos relacionais, pode ser entendido como qualquer banco de dados que não siga o modelo relacional fornecido pelos SGBDR. Esta categoria de bancos de dados é também conhecida como banco de dados NoSQL (Not only SQL) se tornou comum para definir outros tipos de bancos de dados, como exemplo os que utilizam vetores, documentos, chave e valor 

### Os tipo são 

-  Bancos de dados de documentos
	Também chamados de  SGBD orientados a documentos, são caracterizadas por sua organização de dados sem esquemas.
	Não precisam estar em uma mesma estrutura uniforme ou seja registros podem ter atributos diferentes
	Documentos em geral são armazenados em objetos JSON. Normalmente possuem linguagens de consulta e podem ser escalados horizontalmente para acomodar grandes volumes de dados.
	Dentre eles, destaca-se o Mongo-db que é constantemente classificado como o banco de dados NoSql mais popular

- Bancos de dados Colunares
	Diferentemente dos bancos relacionais, que armazenam dados em linhas, os bancos de dados colunares armazenam dados em colunas. isso permite uma recuperação mais eficiente de dados em consultas analíticas, pois apenas as colunas relevantes precisam ser acessadas.
	Esses bancos de dados são especialmente úteis para análise de grandes volumes de dados.
	Exemplo : Apache Cassandra, Hbase e Google Bigtable.

- Bancos de dados de chave e valor
	Esses bancos de dados armazenam dados como pares de chave e valor, onde uma chave é associada a um valor Eles são altamente escaláveis e oferecem tempos de resposta rápidos para operações de escrita e leitura. Os valores podem ser estruturados ou não, dependendo do banco de dados. são utilizados para armazenar caches, sessões de usuário e dados de configuração Exemplo populares incluem, Redis, Riak e Amazon dynamodb 

- Bancos de dados orientados a grafos
	Esses bancos de dados são projetados para armazenar e consultar relacionamentos complexos entre entidades. Eles usam uma estrutura de grafo composta por nós (entidades), arestas ( relacionamentos ) e propriedades ( atributos ). Os bancos de dados de gráfico são ideias para análise de rede, recomendações personalizadas e detecção de padrões. Exemplos incluem Neo4J, Amazon Neptune e JanusGraph
 
-  Bancos de dados de séries temporais
	Esses bancos de dados são otimizados para armazenar e consultar dados que evoluem com o tempo, como dados de sensores, registros de eventos e métricas de desempenho. Eles oferecem recursos específicos para armazenamento eficiente de dados cronológicos e suporte a consultas temporais. Exemplos populares incluem InfluxDB, TimescaleDB e Prometheus.
	
	
	
	Além  desses,  há  também  bancos  de  dados  in-memory,  bancos  de  dados espaciais para dados geográficos, bancos de dados de texto completospara pesquisa textual e muitos outros tipos especializados. 
	
	diferenças  entre  bancos  de  dados  relacionais  e  não  relacionais  são significativas  e  abrangem  diversos  aspectos.  Aqui  estão  algumas  das  principais diferenças:Modelo de dadosBancos de dados relacionaisseguem o modelo relacional, em que os dados são  organizados  em  tabelas  com  linhas  e  colunas.  As  relações  entre  tabelas  são
	


---

## Diferenças entre Bancos de Dados Relacionais e Não Relacionais

As diferenças entre bancos de dados relacionais e não relacionais são significativas e abrangem diversos aspectos. A seguir, estão algumas das principais diferenças:

---

### 1. **Modelo de Dados**

**Bancos de dados relacionais**

- Seguem o modelo relacional.    
- Os dados são organizados em **tabelas** com **linhas e colunas**.
- As relações entre tabelas são estabelecidas por:
    - **Chaves primárias**
    - **Chaves estrangeiras**

**Bancos de dados não relacionais**

- Adotam diferentes modelos de dados, como:
    - Documento
    - Chave-valor
    - Armazenamento em colunas
    - Grafos
        
- Permitem estruturação mais flexível dos dados.
- Facilitam a representação direta de objetos e estruturas complexas.
    

---

### 2. **Desempenho**

**Bancos de dados relacionais**

- São otimizados para fornecer transações **ACID**:    
    - Atomicidade
    - Consistência
    - Isolamento
    - Durabilidade
        
- Adequados para aplicações que exigem:
    - Transações seguras
    - Consistência rígida dos dados
        

**Bancos de dados não relacionais**
- Projetados para:
    - Alta escalabilidade
    - Alto desempenho em leitura e gravação
- Geralmente priorizam:
    - Velocidade
    - Capacidade de escalar horizontalmente
- Distribuem dados em vários servidores.

---
### 3. **Esquema**

**Bancos de dados relacionais**
- Possuem **esquema rígido e pré-definido**.
- A estrutura das tabelas e relacionamentos precisa ser definida **antes** do armazenamento dos dados.

**Bancos de dados não relacionais**

- Possuem:
    - Esquema flexível
    - Ou até mesmo inexistente
- Permitem inserção de dados sem restrições estruturais rígidas.
- Facilitam adaptações rápidas no modelo de dados.
    

---

### 4. **Escalabilidade**

**Bancos de dados relacionais**

- Tradicionalmente utilizam **escalabilidade vertical**, ou seja:\    
    - Aumento de recursos em um único servidor para melhorar desempenho.        

**Bancos de dados não relacionais**

- Projetados para **escalabilidade horizontal**, permitindo:
    - Distribuição de dados entre vários servidores.



Exemplo 
sql
```select * from tabela tb1 
 ``inner join tabela 2 tb2 on tb2.id = tb1.id 
```

nosql 
mql
````
db.customers.find({ gender: "female", age: { $lt: 25 } });
````


Escabilidade 
Vertical x Horizotal

Vertical scaling  = aumento de custo - scale up |  aumentar  a capacidade da maquina
Horizontal scaling =  scale out |  aumentar mais maquinas 