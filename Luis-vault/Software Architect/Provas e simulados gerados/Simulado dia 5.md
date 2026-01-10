# 📝 SIMULADO – VERDADEIRO OU FALSO

**Arquitetura de Software, Segurança, Dados, DevOps, Kubernetes, LGPD e SAGA**

---

## 🔐 DADOS E SEGURANÇA DA INFORMAÇÃO (1–10)

1. ( V ) Confidencialidade garante que os dados estejam disponíveis sempre que necessário. errou
    
2. (V ) Integridade refere-se à proteção contra alterações não autorizadas nos dados.
    
3. ( V) Disponibilidade está relacionada ao tempo em que um sistema permanece acessível.
    
4. ( V) A tríade CIA é composta por Confidencialidade, Integridade e Autenticação. errou
    
5. (V ) Criptografia contribui para a confidencialidade da informação.
    
6. ( F ) Backup é uma medida relacionada à disponibilidade. . errou
    
7. ( F ) Controle de acesso não faz parte da segurança da informação.
    
8. ( V ) Logs são importantes para auditoria e detecção de incidentes.
    
9. ( F ) Segurança da informação é responsabilidade exclusiva da área de TI.
    
10. ( V ) Vazamento de dados é considerado um incidente de segurança.
    
    3/10 erros
     revisar 1, 4, 6 

---

## 🔄 SAGA PATTERN (11–25)

11. ( V) O padrão SAGA é utilizado para gerenciar transações distribuídas.
    
12. (F ) SAGA substitui completamente o uso de bancos de dados relacionais.
    
13. (F  ) Uma Saga é composta por várias transações locais. 
    
14. ( V) Em uma Saga, cada etapa possui uma transação de compensação.
    
15. ( F) O padrão SAGA depende do isolamento total do ACID.
    
16. (V ) Orquestração utiliza um componente central para controlar o fluxo.
    
17. ( V ) Coreografia utiliza eventos para comunicação entre serviços.
    
18. ( V ) Na coreografia, os serviços são mais desacoplados.
    
19. ( V ) Orquestração tende a gerar maior acoplamento.
    
20. ( V ) Consistência eventual significa que os dados podem ficar inconsistentes temporariamente.
    
21. ( V ) O “I” do ACID representa Isolamento.
    
22. ( F ) Em microsserviços, o isolamento do ACID é difícil de garantir.
    
23. ( V ) Idempotência é importante para evitar efeitos colaterais em retries.
    
24. ( V) Dead Letter Queue armazena mensagens que falharam repetidamente.
    
25. ( F) SAGA é mais indicada para sistemas monolíticos simples.

	   Erro 13, 22
	   11 - 25 / 2 erros 
---

## 🛡️ DESENVOLVIMENTO SEGURO (26–40)

26. (V ) Vulnerabilidade é uma falha que pode ser explorada.
    
27. (V ) Ataque é a exploração de uma vulnerabilidade.
    
28. ( V ) Intrusão ocorre quando um ataque é bem-sucedido.
    
29. ( F ) SQL Injection ocorre apenas em bancos NoSQL.
    
30. ( V ) Prepared Statements ajudam a prevenir SQL Injection.
    
31. ( F ) XSS permite execução de scripts maliciosos no navegador do usuário.
    
32. (  V) Buffer Overflow ocorre quando não há validação de limites de memória.
    
33. ( V ) Validação de entrada é uma boa prática de segurança.
    
34. ( V ) Bibliotecas desatualizadas podem introduzir vulnerabilidades.
    
35. ( V ) Supply Chain Attack envolve dependências de software.
    
36. (V ) Análise estática executa o código em tempo de execução.
    
37. ( V ) SonarQube é uma ferramenta de análise estática.
    
38. ( V  ) OWASP é uma organização focada em segurança de aplicações.
    
39. ( F ) O OWASP Top 10 lista as principais vulnerabilidades de aplicações web.
    
40. ( F ) Segurança deve ser tratada apenas após o sistema estar pronto.
    
		Erros /  31/36/.40
		
		3/14O 
---

## 📜 LGPD – PRIVACIDADE DE DADOS (41–55)

41. ( V ) A LGPD trata da proteção de dados pessoais.
    
42. ( V ) Dado pessoal é qualquer informação relacionada a pessoa natural identificável.
    
43. (V  ) Dado sensível inclui origem racial, saúde e dados biométricos.
    
44. ( F) Titular é a empresa que controla os dados.
    
45. (F ) Controlador decide sobre o tratamento dos dados.
    
46. (V ) Operador realiza o tratamento em nome do controlador.
    
47. ( V) Finalidade é um princípio da LGPD.
    
48. ( V ) Necessidade significa coletar apenas dados essenciais.
    
49. (V ) Transparência exige clareza no tratamento de dados.
    
50. (F ) LGPD não se aplica a sistemas de software.
    
51. ( V) Governança de dados envolve políticas e processos internos.
    
52. ( F ) Segurança é um princípio da LGPD.
    
53. (F ) IA pode ser usada sem restrições pela LGPD.
    
54. ( V ) Minimização de dados é recomendada na LGPD.
    
55. ( V ) A LGPD exige responsabilização dos agentes de tratamento.
    
		erro 45/52
---

## 🧩 ARQUITETURA DE MICROSSERVIÇOS (56–65)

56. ( V ) Microsserviços são independentes entre si.
    
57. ( V ) Cada microsserviço deve ter seu próprio banco de dados.
    
58. ( V ) Deploy de microsserviços é independente.
    
59. ( F ) Comunicação síncrona é sempre melhor que assíncrona.
    
60. ( V ) API Gateway centraliza autenticação e roteamento.
    
61. ( V) BFF significa Backend for Frontend.
    
62. ( F ) Microsserviços reduzem a complexidade de sistemas automaticamente.
    
63. ( V ) Mensageria é comum em arquiteturas distribuídas.
    
64. ( V ) Falhas devem ser esperadas em microsserviços.
    
65. ( V ) Observabilidade é importante em ambientes distribuídos.
    

---

## ☁️ SERVERLESS E DEVOPS (66–75)

66. (V ) Serverless elimina a necessidade de servidores físicos.
    
67. ( F) Em serverless, o desenvolvedor gerencia a infraestrutura.
    
68. (V ) AWS Lambda é um serviço serverless.
    
69. (V ) O custo em serverless é baseado no uso.
    
70. (V ) API Gateway integra com funções Lambda.
    
71. (F) CI significa Continuous Integration.
    
72. (V ) CD significa Continuous Delivery ou Deployment.
    
73. (V ) GitHub Actions é uma ferramenta de CI/CD.
    
74. (V ) Terraform é uma ferramenta de Infrastructure as Code.
    
75. (V ) DevOps busca integração entre desenvolvimento e operações.
    

---

## 🗄️ DATA ENGINEERING (76–85)

76. ( V ) MongoDB é um banco orientado a documentos.
    
77. (V ) Redis é um banco chave-valor.
    
78. (F ) Cassandra é um banco relacional tradicional.
    
79. (V ) Neo4J é um banco orientado a grafos.
    
80. (V ) DBaaS significa banco de dados como serviço.
    
81. (F ) Bancos NoSQL possuem esquema rígido.
    
82. (V ) Bancos colunar são eficientes para grandes volumes de dados.
    
83. (V ) Microsserviços podem usar diferentes tipos de banco de dados.
    
84. ( F) Consistência forte é sempre prioridade em NoSQL.
    
85. ( V ) Data Engineering envolve armazenamento e processamento de dados.
    

---

## 🐳 KUBERNETES, CLEAN ARCH E DDD (86–100)

86. ( V ) Kubernetes é um orquestrador de contêineres.
    
87. ( V ) Pod é a menor unidade do Kubernetes.
    
88. ( V ) Deployment gerencia versões de aplicações.
    
89. ( V ) Service expõe aplicações dentro ou fora do cluster.
    
90. ( V) HPA permite escalabilidade automática.
    
91. ( V ) Helm é um gerenciador de pacotes para Kubernetes.
    
92. ( V ) EKS é o serviço gerenciado de Kubernetes da AWS.
    
93. ( F ) Clean Architecture defende independência de frameworks.
    
94. ( V ) Na Clean Architecture, dependências apontam para fora.
    
95. ( F ) Entidades representam regras de negócio centrais.
    
96. ( V ) DDD foca no domínio do negócio.
    
97. ( F ) Bounded Context delimita responsabilidades.
    
98. (V) Ubiquitous Language melhora comunicação entre time e negócio.
    
99. ( F ) Event Storming é uma técnica de DDD.
    

     
    O que eu nao sei 
    Bounded Context ?
     Coreografia saga?