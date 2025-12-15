
### Perguntas sobre Apache Kafka

O Kafka foi criado para **resolver o problema** de pipeline de dados do **LinkedIn**. Ele foi desenvolvido para ser um **sistema de mensageria de alta performance** que consegue lidar com **diversos tipos de dados** e providenciar **dados limpos e estruturados** sobre **comportamento de usuários no site**, além de um **sistema de métricas** em **tempo real**. Inicialmente, o Kafka conseguia lidar **1,4 trilhões de mensagens por dia**. Após Fevereiro de 2020, ele processou **7 trilhões de mensagens** e **mais de 5 petabytes de dados** consumidos por dia, segundo a **Confluent**, empresa fundada pelos criadores de Apache Kafka e que mais contribui com a ferramenta.

1. **O que é um tópico em Kafka e como ele difere de uma fila tradicional?**

2. Um tópico em Apache Kafka é um canal lógico onde são publicados e armazenados eventos (mensagens) para serem consumidos por consumidores. Ele atua como uma espécie de "categoria" ou "nome de feed" para os dados, onde produtores escrevem eventos e consumidores leem esses eventos.
3. 
	**Persistência**: As mensagens em Kafka são persistidas em disco e mantidas por um tempo configurável
	
	**Particionamento**: Um tópico pode ser dividido em várias partições, permitindo escalabilidade horizontal. 
	
	**Paralelismo**: Kafka permite múltiplos padrões de consumo, incluindo grupos de consumidores para processamento paralelo; filas tradicionais são limitadas ao modelo ponto-a-ponto.
	
1. **Explique o conceito de partições em Kafka e como elas contribuem para a escalabilidade.**
2. 
3. **Como Kafka garante a entrega ordenada das mensagens dentro de uma partição?**
4. 
5. **O que é um consumidor em grupo (consumer group) e como ele funciona em Kafka?**
6. 
7. **Quais são as diferenças entre o modo de entrega "at least once" e "exactly once" em Kafka?**

- **_At-most-once_**: **No máximo uma** mensagem vai ser entregue, podendo haver perdas de dados;
- **_Exactly-once_**: **Exatamente uma** mensagem vai ser entregue, sem duplicações e perdas.

8. **Explique como funciona o armazenamento de logs segmentados (log segments) em Kafka.**

9. **Como Kafka lida com a retenção de mensagens e o que é o log compaction?**

10. **Descreva o papel do Zookeeper no ecossistema Kafka.**
	O **_Apache Zookeeper_** é um serviço centralizado para **manter informações de configuração**, **nomear** e providenciar **sincronização distribuída** em **grupo de serviços**.

1. **Quais são as principais diferenças entre Kafka e um sistema de mensageria tradicional como RabbitMQ?**

2. **Como configurar e gerenciar a replicação de dados entre clusters Kafka?**

3. **Quais são as práticas recomendadas para otimizar o desempenho de um cluster Kafka?**
16
. **Como implementar a segurança em Kafka, incluindo autenticação e criptografia?**

### Perguntas sobre RabbitMQ

1. **O que é uma exchange em RabbitMQ e quais são os tipos principais de exchanges?**

2. **Como funciona o binding entre uma fila e uma exchange em RabbitMQ?**

3. **Explique o conceito de mensagens persistentes e não persistentes em RabbitMQ.**

4. **Quais são as diferenças entre o modo de entrega "at most once" e "at least once" em RabbitMQ?**

5. **Como RabbitMQ lida com a escalabilidade e o balanceamento de carga entre consumidores?**

6. **O que são dead-letter exchanges (DLX) e como são utilizadas em RabbitMQ?**
### Como Funcionam as DLX em RabbitMQ

1. **Definição de uma DLX**: Uma DLX é apenas uma exchange normal configurada para receber mensagens que foram "morridas" (dead-lettered). Você pode configurar qualquer exchange como uma DLX.
    
2. **Configuração da Fila Original**: Para que uma fila utilize uma DLX, você precisa configurar a fila original para apontar para a exchange de dead-letter. Isso é feito através da configuração de argumentos da fila no momento da criação.
    
3. **Causas para Dead-Lettering**:
    
    - **Rejeição de Mensagem**: Quando uma mensagem é explicitamente rejeitada pelo consumidor (com a flag `requeue=false`).
    - **TTL Expirado**: Se a mensagem permanece na fila além do tempo-to-live (TTL) configurado.
    - **Limite de Redelivery**: Se a mensagem excede o número máximo de tentativas de redelivery.
    - **Erro de Roteamento**: Quando uma mensagem não pode ser roteada para nenhuma fila (se configurado para dead-lettering nesses casos).

### Configuração de DLX em RabbitMQ

7. **Descreva como a confirmação de mensagens (message acknowledgment) funciona em RabbitMQ.**

8. **Quais são as melhores práticas para configurar a alta disponibilidade em um cluster RabbitMQ?**

9. **Como configurar e utilizar plugins em RabbitMQ, como o plugin de gerenciamento?**

10. **Explique como implementar segurança em RabbitMQ, incluindo autenticação, autorização e criptografia.**

11. **Quais são os principais diferenciais entre RabbitMQ e Apache Kafka em termos de arquitetura e casos de uso?**

12. **Como funciona a política de TTL (Time-To-Live) para mensagens e filas em RabbitMQ?**

Essas perguntas podem ajudar a aprofundar o entendimento sobre as funcionalidades, arquiteturas e melhores práticas associadas a Apache Kafka e RabbitMQ.