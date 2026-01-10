# ✅ Correção organizada – Questões que você errou

## 1) Questão 1

**Enunciado:** “Confidencialidade garante que os dados estejam disponíveis sempre que necessário.”  
❌ **Sua marcação:** V  
✅ **Correto:** **F**

**Por quê:**

- **Confidencialidade** = impedir acesso/divulgação a quem não tem permissão.
    
- Quem garante acesso quando necessário é **Disponibilidade**.
    

**Macete:**

> Confidencialidade = “segredo”; Disponibilidade = “sempre acessível”.

---

## 2) Questão 4

**Enunciado:** “A tríade CIA é composta por Confidencialidade, Integridade e Autenticação.”  
❌ **Sua marcação:** V  
✅ **Correto:** **F**

**Por quê:**  
A tríade **CIA** é:

- **C**onfidencialidade
    
- **I**ntegridade
    
- **A**vailability (**Disponibilidade**)  
    Autenticação é importante, mas **não** é o “A” da tríade.
    

**Macete:**

> CIA = Confidencialidade + Integridade + Disponibilidade.

---

## 3) Questão 6

**Enunciado:** “Backup é uma medida relacionada à disponibilidade.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**Por quê:**  
Backup ajuda a recuperar dados/sistemas após falhas (ransomware, erro humano, pane), reduzindo downtime → isso é **Disponibilidade**.

**Macete:**

> Backup = recuperação = disponibilidade.

---

## 4) Questão 13

**Enunciado:** “Uma Saga é composta por várias transações locais.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**Por quê:**  
Saga = sequência de **transações locais** (cada serviço faz sua parte).  
Se algo falhar, executa **compensações** para “desfazer” etapas anteriores.

**Macete:**

> Saga = várias transações locais + compensações.

---

## 5) Questão 22

**Enunciado:** “Em microsserviços, o isolamento do ACID é difícil de garantir.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**Por quê:**  
Em microsserviços, cada serviço tem seu próprio banco/estado. Não existe “transação única” com isolamento forte atravessando vários serviços como num monólito. Por isso usa-se:

- consistência eventual
    
- SAGA
    
- idempotência e retries
    

**Macete:**

> ACID forte “de ponta a ponta” é difícil em microsserviços.

---

## 6) Questão 31

**Enunciado:** “XSS permite execução de scripts maliciosos no navegador do usuário.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**Por quê:**  
XSS (Cross-Site Scripting) permite injetar script (geralmente JS) que roda **no navegador da vítima**, podendo roubar sessão, redirecionar, alterar conteúdo etc.

**Macete:**

> XSS = script executa no browser do usuário.

---

## 7) Questão 36

**Enunciado:** “Análise estática executa o código em tempo de execução.”  
❌ **Sua marcação:** V  
✅ **Correto:** **F**

**Por quê:**

- **Análise estática**: inspeciona código **sem executar** (SAST, SonarQube).
    
- Quem executa e observa comportamento é **análise dinâmica** (DAST).
    

**Macete:**

> Estática = sem rodar; Dinâmica = rodando.

---

## 8) Questão 45 (LGPD – Controlador)

**Enunciado:** “Controlador decide sobre o tratamento dos dados.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**Por quê:**

- **Controlador**: decide **finalidade**, meios e regras do tratamento.
    
- **Operador**: executa o tratamento **em nome do controlador**.
    

**Macete:**

> Controlador decide; Operador executa.

---

## 9) Questão 52 (LGPD – Princípio)

**Enunciado:** “Segurança é um princípio da LGPD.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**Por quê:**  
A LGPD prevê o princípio da **Segurança**: adotar medidas técnicas e administrativas para proteger dados contra acessos não autorizados e incidentes.

**Macete:**

> LGPD: segurança é obrigação/princípio.

---

## 10) Questão 66 (Serverless)

**Enunciado:** “Serverless elimina a necessidade de servidores físicos.”  
❌ **Sua marcação:** V  
✅ **Correto:** **F**

**Por quê:**  
Servidores existem, mas ficam sob responsabilidade do provedor (AWS/Azure/GCP). O “serverless” significa:

- você não gerencia servidor
    
- você gerencia apenas função/serviço
    

**Macete:**

> Serverless ≠ sem servidor; é “sem gerenciar servidor”.

---

## 11) Questão 71 (CI)

**Enunciado:** “CI significa Continuous Integration.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**Por quê:**  
CI = integrar código frequentemente + testes automáticos + detectar problemas cedo.

**Macete:**

> CI = integração contínua.

---

## 12) Questão 93 (Clean Architecture)

**Enunciado:** “Clean Architecture defende independência de frameworks.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**Por quê:**  
Framework é detalhe. O domínio e os casos de uso não devem depender de Spring/Hibernate/etc.

**Macete:**

> Framework é detalhe, domínio é núcleo.

---

## 13) Questão 94 (Direção das dependências)

**Enunciado:** “Na Clean Architecture, dependências apontam para fora.”  
❌ **Sua marcação:** V  
✅ **Correto:** **F**

**Por quê:**  
Regra de ouro: dependências apontam **para dentro** (para o domínio).

**Macete:**

> Setas sempre para o centro (domínio).

---

## 14) Questão 95 (Entidades)

**Enunciado:** “Entidades representam regras de negócio centrais.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**Por quê:**  
Entities modelam regras essenciais do negócio (core). Não são “só tabelas” ou DTO.

**Macete:**

> Entidade = regra de negócio + identidade.

---

## 15) Questão 97 (Bounded Context)

**Enunciado:** “Bounded Context delimita responsabilidades.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**O que é Bounded Context (bem direto):**  
É um “limite” onde um modelo de domínio e seus termos têm significado consistente. Evita “um mesmo termo significar coisas diferentes”.

**Exemplo rápido:**  
“Pedido” em **Vendas** ≠ “Pedido” em **Logística** → contextos separados.

**Macete:**

> Bounded Context = limite de significado + responsabilidade.

---

## 16) Questão 99 (Event Storming)

**Enunciado:** “Event Storming é uma técnica de DDD.”  
❌ **Sua marcação:** F  
✅ **Correto:** **V**

**Por quê:**  
Técnica colaborativa para descobrir processos do domínio por meio de **eventos de negócio**.

**Macete:**

> Event Storming = mapear o domínio por eventos.

---

## 17) Questão 100 (DDD + Clean)

**Enunciado:** “DDD e Clean Architecture são incompatíveis.”  
❌ **Sua marcação:** V  
✅ **Correto:** **F**

**Por quê:**  
Elas se complementam. DDD modela o domínio; Clean organiza as camadas e dependências.

**Macete:**

> DDD + Clean = combinação comum e forte.