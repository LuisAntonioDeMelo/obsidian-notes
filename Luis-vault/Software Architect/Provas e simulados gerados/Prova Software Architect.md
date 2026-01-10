# 📘 PROVA FINAL – ARQUITETURA DE SOFTWARE E SISTEMAS DISTRIBUÍDOS

**Duração:** 3h  
**Modalidade:** individual  
**Pontuação total:** 100 pontos

---

## 🔹 PARTE I – FUNDAMENTOS DE ARQUITETURA (20 pontos)

**Questão 1 – DDD e Arquitetura (10 pts)**  
Explique como o **Domain-Driven Design** contribui para a definição de **microsserviços coesos**.  
Em sua resposta, aborde obrigatoriamente:

-
-// Minha resposta 
	 Linguagem ubíqua, a linguagem assertiva que comunica sem ambiguidades, de forma coesa como será o comportamento do software  

// resposta correta 
    A linguagem ubíqua é a base para um projeto baseado em DDD, ela é a base para conseguirmos construir nossos **modelos de domínio — estratégico e tático**. Além disso, a linguagem ubíqua não é uma linguagem universal, ela é unica por **contexto delimitados ou por sub-domínios** (assunto para o próximo post) ou departamentos da empresa. Ela cria um vocabulário coeso e que faça sentido tanto para especialistas de domínio quanto para desenvolvedores.
    
     Exemplos 
       criarPedido()
       autorizarPagamento()
       cancelarPedido()
       estornarPagamento()
       realizarVenda()  
     Exemplo de Dominio
       PedidoCriado
       PagamentoAutorizado
       PagamentoEstornado
       PedidoConfirmado
    
- Bounded Context
    
- Event Storming
    
- Impactos na escalabilidade e manutenção
    

---

**Questão 2 – Clean Architecture (10 pts)**  
Descreva a estrutura de uma aplicação baseada em **Clean Architecture**, indicando:

- Camadas
    
- Regra da dependência
    
- Benefícios para testabilidade e evolução do sistema  
    Explique por que essa abordagem é especialmente adequada para microsserviços.
    

---

## 🔹 PARTE II – CONTEINERIZAÇÃO, KUBERNETES E DEVOPS (20 pontos)

**Questão 3 – Docker e Kubernetes (10 pts)**  
Explique o papel de cada um dos elementos abaixo dentro de um cluster Kubernetes:

- Pod
    
- Service
    
- ConfigMap
    
- Deployment
    
- HPA
    

Indique **um cenário real** onde o uso de cada componente é essencial.

---

**Questão 4 – CI/CD e IaC (10 pts)**  
Explique como **CI/CD aliado ao Terraform** contribui para:

- Redução de erros humanos
    
- Padronização de ambientes
    
- Segurança e rastreabilidade
    

Inclua no mínimo **um exemplo prático** usando GitHub Actions.

---

## 🔹 PARTE III – MICROSSERVIÇOS, DADOS E DISTRIBUIÇÃO (20 pontos)

**Questão 5 – Comunicação entre Microsserviços (10 pts)**  
Compare:

- Comunicação síncrona vs assíncrona
    
- API Gateway vs BFF
    

Indique vantagens, desvantagens e impactos em performance e escalabilidade.

---

**Questão 6 – Bancos de Dados e Microsserviços (10 pts)**  
Explique por que **cada microsserviço deve possuir seu próprio banco de dados**.  
Cite ao menos **3 tipos de bancos diferentes** (relacional, documento, chave-valor, grafo) e indique um caso de uso para cada.

---

## 🔹 PARTE IV – CONSISTÊNCIA, SEGURANÇA E LGPD (30 pontos)

**Questão 7 – Padrão SAGA (10 pts)**  
Explique:

- O problema das transações distribuídas
    
- A ausência do “I” do ACID
    
- Diferença entre **orquestração** e **coreografia**
    
- Quando utilizar cada abordagem
    

---

**Questão 8 – Desenvolvimento Seguro (10 pts)**  
Explique **três vulnerabilidades do OWASP Top 10**, descrevendo:

- Como ocorrem
    
- Impactos no sistema
    
- Estratégias de mitigação
    

---

**Questão 9 – LGPD aplicada ao software (10 pts)**  
Explique como a **LGPD influencia diretamente**:

- Arquitetura da solução
    
- Modelagem de dados
    
- Segurança
    
- Uso de IA
    

Inclua os princípios da LGPD aplicáveis ao desenvolvimento de software.

---

## 🔹 PARTE V – QUESTÃO PRÁTICA (10 pontos)

**Questão 10 – Análise Arquitetural**  
Dado um sistema de e-commerce distribuído:

- Proponha uma arquitetura de alto nível
    
- Indique tecnologias
    
- Explique como garantir escalabilidade, segurança e conformidade com a LGPD