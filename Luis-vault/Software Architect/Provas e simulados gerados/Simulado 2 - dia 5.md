# 📝 SIMULADO AVANÇADO – 50 QUESTÕES

**Arquitetura de Software, Segurança, Dados e Microsserviços**

---

## 🔐 SEGURANÇA DA INFORMAÇÃO & LGPD (1–10)

**1.** Em um sistema crítico, a indisponibilidade temporária causada por um ataque de ransomware afeta diretamente qual princípio da segurança da informação?  
a) Confidencialidade  
b) Integridade  
c) Autenticidade  
d) Disponibilidade  (x) d
e) Não repúdio

---

**2.** Uma política de controle de acesso baseada no menor privilégio tem como principal objetivo:  
a) Aumentar desempenho do sistema  
b) Reduzir complexidade do código  
c) Minimizar impacto de acessos indevidos  (x ) c
d) Garantir disponibilidade contínua  
e) Substituir mecanismos de autenticação

---

**3.** Segundo a LGPD, quem decide a finalidade e os meios do tratamento de dados pessoais é:  
a) O operador  ( x ) a
b) O encarregado (DPO)  
c) O titular  
d) O controlador  
e) A autoridade nacional

---

**4.** A coleta excessiva de dados pessoais, além do necessário para a finalidade pretendida, viola principalmente qual princípio da LGPD?  
a) Finalidade  
b) Transparência (X)  
c) Segurança  
d) Necessidade  
e) Responsabilização

---

**5.** O uso de criptografia inadequada ou inexistente para proteger dados sensíveis é classificado no OWASP Top 10 (2021) como:  
a) Insecure Design  
b) Injection  
c) Cryptographic Failures  
d) Security Misconfiguration  
e) Software Integrity Failures (x)

---

**6.** Um ataque XSS persistente ocorre quando:  
a) Scripts são executados no servidor  (x)
b) Código malicioso é armazenado e entregue a vários usuários  
c) O atacante manipula cabeçalhos HTTP  
d) O ataque depende de engenharia social  
e) O script é executado apenas uma vez

---

**7.** Qual prática é MAIS eficaz para mitigar SQL Injection?  
a) Validação no front-end  
b) Escape manual de strings  
c) Prepared Statements / Query parametrizada  (x)
d) Firewall de rede  
e) Hash de senhas

---

**8.** No contexto da LGPD aplicada a IA, a principal preocupação relacionada à tomada de decisão automatizada é:  
a) Performance do algoritmo  
b) Custo computacional  
c) Transparência e explicabilidade  (x)
d) Escalabilidade do modelo  
e) Uso de containers

---

**9.** Qual alternativa representa corretamente a relação entre backup e segurança da informação?  
a) Backup está ligado apenas à confidencialidade  
b) Backup não possui relação com segurança  
c) Backup contribui para disponibilidade e continuidade  (x)
d) Backup substitui criptografia  
e) Backup garante integridade lógica

---

**10.** Logs e monitoramento são fundamentais principalmente para atender a qual objetivo de segurança?  
a) Prevenção de ataques  
b) Detecção e resposta a incidentes  (x)
c) Criptografia de dados  
d) Autorização de usuários  
e) Controle de acesso físico

---

## 🔄 SAGA, CONSISTÊNCIA E MICROSSERVIÇOS (11–20)

**11.** O padrão SAGA é mais adequado quando:  
a) Há necessidade de isolamento ACID global  
b) Existe um único banco de dados central  
c) As transações envolvem múltiplos serviços independentes  (x)
d) O sistema é monolítico  
e) Não há necessidade de rollback

---

**12.** Na abordagem de coreografia em SAGA, o fluxo é controlado principalmente por:  
a) Um orquestrador central  
b) Um banco de dados transacional  
c) Chamadas síncronas encadeadas  
d) Eventos e reações dos serviços  (x)
e) O cliente final

---

**13.** A principal vantagem da coreografia sobre a orquestração é:  
a) Menor complexidade conceitual   (x )
b) Menor acoplamento entre serviços  
c) Maior controle central  
d) Facilidade de debug  
e) Garantia de consistência forte

---

**14.** A ausência do “I” (Isolamento) do ACID em microsserviços leva, normalmente, à adoção de:  
a) Locks distribuídos  (x)
b) Consistência eventual  
c) Transações globais  
d) Two-Phase Commit  
e) Escalabilidade vertical

---

**15.** Idempotência é essencial em arquiteturas distribuídas porque:  
a) Garante maior performance  
b) Evita execução duplicada de efeitos colaterais  (x) 
c) Substitui autenticação  
d) Elimina falhas de rede  
e) Simplifica modelagem de domínio

---

**16.** Uma Dead Letter Queue é utilizada principalmente para:  
a) Armazenar mensagens com alta prioridade  
b) Persistir logs de auditoria  
c) Tratar mensagens que falharam repetidamente  (x)
d) Balancear carga  
e) Substituir retries

---

**17.** Em microsserviços, falhas devem ser:  
a) Eliminadas por design  
b) Tratadas como exceção rara  
c) Esperadas e tratadas explicitamente  (x)
d) Ignoradas pelo sistema  
e) Centralizadas em um único serviço

---

**18.** O uso de mensageria em microsserviços favorece principalmente:  
a) Consistência forte  
b) Baixo acoplamento e resiliência  (x)
c) Comunicação síncrona  
d) Simplificação de transações ACID  
e) Eliminação de latência

---

**19.** O padrão API Gateway é mais indicado para:  
a) Persistência de dados  
b) Orquestração de negócios  
c) Centralizar preocupações transversais  (x)
d) Substituir microsserviços  
e) Executar regras de domínio

---

**20.** BFF (Backend for Frontend) existe principalmente para:  
a) Reduzir custo de infraestrutura  
b) Criar um backend genérico  
c) Adaptar APIs às necessidades de cada frontend  (x)
d) Centralizar regras de negócio  
e) Substituir o API Gateway

---

## 🧱 CLEAN ARCHITECTURE, DDD, DEVOPS E K8S (21–50)

**21.** Na Clean Architecture, a regra de dependência afirma que:  
a) Dependências apontam para frameworks  
b) Dependências apontam para fora  
c) Dependências apontam para dentro  
d) Dependências são bidirecionais  
e) Não há regra definida

---

**22.** As entidades, na Clean Architecture, representam:  
a) DTOs de banco  
b) Controllers  
c) Regras de negócio centrais  
d) Infraestrutura  
e) APIs externas

---

**23.** Bounded Context, no DDD, serve para:  
a) Definir limites técnicos  
b) Separar times por tecnologia  
c) Delimitar onde um modelo de domínio é válido  
d) Centralizar regras de negócio  
e) Substituir microsserviços

---

**24.** Event Storming é utilizado principalmente para:  
a) Testes de carga  
b) Deploy de aplicações  
c) Descobrir e entender o domínio  
d) Monitoramento de eventos técnicos  
e) Criação de APIs REST

---

**25.** Um dos principais objetivos do DDD é:  
a) Reduzir custo de infraestrutura  
b) Focar no domínio e na linguagem do negócio  
c) Substituir padrões arquiteturais  
d) Eliminar testes  
e) Criar sistemas monolíticos

---

**26.** Em Kubernetes, um Pod é:  
a) Um cluster  
b) Um nó  
c) A menor unidade de execução  
d) Um serviço externo  
e) Um volume persistente

---

**27.** Um Deployment no Kubernetes é responsável por:  
a) Expor aplicações  
b) Gerenciar versões e réplicas  
c) Armazenar dados  
d) Configurar rede  
e) Monitorar logs

---

**28.** HPA (Horizontal Pod Autoscaler) baseia-se geralmente em:  
a) Número fixo de pods  
b) Uso de CPU/métricas  
c) ConfigMap  
d) Versão da aplicação  
e) Nome do serviço

---

**29.** Helm é melhor descrito como:  
a) Um runtime de containers  
b) Um sistema de CI/CD  
c) Um gerenciador de pacotes para Kubernetes  
d) Um serviço de cloud  
e) Um banco de dados

---

**30.** EKS é:  
a) Um serviço de containers da Azure  
b) Um orquestrador proprietário  
c) Kubernetes gerenciado pela AWS  
d) Um cluster on-premises  
e) Um serviço serverless

---

**31.** Serverless caracteriza-se principalmente por:  
a) Ausência total de servidores  
b) Infraestrutura gerenciada pelo provedor  
c) Execução síncrona obrigatória  
d) Alto acoplamento  
e) Uso exclusivo de containers

---

**32.** Em serverless, o custo normalmente está associado a:  
a) Número de servidores  
b) Capacidade reservada  
c) Tempo e número de execuções  
d) Número de desenvolvedores  
e) Tipo de banco

---

**33.** CI/CD tem como objetivo principal:  
a) Eliminar bugs  
b) Automatizar integração e entrega  
c) Substituir testes  
d) Aumentar acoplamento  
e) Centralizar deploy manual

---

**34.** Terraform é usado para:  
a) Criar containers  
b) Gerenciar código-fonte  
c) Definir infraestrutura como código  
d) Executar pipelines  
e) Monitorar aplicações

---

**35.** MongoDB é classificado como:  
a) Relacional  
b) Colunar  
c) Documento  
d) Grafo  
e) Chave-valor

---

**36.** Redis é mais adequado para:  
a) Relatórios analíticos complexos  
b) Grafos sociais  
c) Cache e dados chave-valor  
d) Dados altamente relacionais  
e) Transações ACID complexas

---

**37.** Cassandra é otimizado para:  
a) Baixa latência com joins  
b) Escalabilidade horizontal e grandes volumes  
c) Transações financeiras  
d) Relacionamentos complexos  
e) Pequenos conjuntos de dados

---

**38.** Neo4J é especialmente indicado quando o foco é:  
a) Alta taxa de escrita simples  
b) Cache distribuído  
c) Relacionamentos entre dados  
d) Dados semi-estruturados  
e) Logs

---

**39.** Polyglot Persistence significa:  
a) Um único banco para tudo  
b) Uso de múltiplos bancos conforme o contexto  
c) Replicação síncrona  
d) Consistência forte global  
e) Eliminação de NoSQL

---

**40.** Observabilidade envolve principalmente:  
a) Logs, métricas e traces  
b) Apenas logs  
c) Apenas monitoramento de CPU  
d) Auditoria financeira  
e) Testes unitários

---

**41.** Testes de integração verificam:  
a) Funções isoladas  
b) Interfaces entre componentes  
c) Apenas performance  
d) Regras de negócio puras  
e) Estilo de código

---

**42.** TDD segue qual sequência?  
a) Green → Red → Refactor  
b) Red → Green → Refactor  
c) Refactor → Red → Green  
d) Build → Test → Deploy  
e) Code → Test → Fix

---

**43.** BDD foca principalmente em:  
a) Performance  
b) Infraestrutura  
c) Comportamento esperado do sistema  
d) Código-fonte  
e) Deploy

---

**44.** Testes não funcionais avaliam:  
a) Regras de negócio  
b) APIs REST  
c) Performance, segurança, usabilidade  
d) Controllers  
e) Entidades

---

**45.** A principal vantagem de microsserviços é:  
a) Menor número de serviços  
b) Simplicidade total  
c) Deploy independente e escalabilidade  
d) Menor necessidade de testes  
e) Uso obrigatório de cloud

---

**46.** A principal desvantagem de microsserviços é:  
a) Escalabilidade  
b) Complexidade operacional  
c) Resiliência  
d) Independência  
e) Modularidade

---

**47.** Comunicação síncrona excessiva em microsserviços tende a:  
a) Aumentar resiliência  
b) Reduzir latência  
c) Aumentar acoplamento  
d) Melhorar tolerância a falhas  
e) Simplificar transações

---

**48.** Qual prática é mais alinhada à arquitetura resiliente?  
a) Locks distribuídos  
b) Retry sem limite  
c) Circuit Breaker  
d) Transações globais  
e) Acoplamento forte

---

**49.** O princípio do menor privilégio significa:  
a) Menos usuários no sistema  
b) Acesso máximo por padrão  
c) Cada componente com permissões mínimas necessárias  
d) Eliminar autenticação  
e) Substituir autorização

---

**50.** Em sistemas distribuídos modernos, consistência forte é geralmente:  
a) Sempre obrigatória  
b) Sempre inviável  
c) Substituída por consistência eventual  
d) Garantida por SAGA  
e) Obtida com API Gateway