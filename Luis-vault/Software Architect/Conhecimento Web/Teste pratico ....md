TESTE TÉCNICO

Desafio Técnico para Desenvolvedor Full Stack (Java e Angular) -
Nível Pleno

Objetivo:
docker pull postgres
template de pagina utilizado como referencia

https://codepen.io/knyttneve/pen/ZEbQepZ
docker volume create pgdata

docker run -d --name postgres -p 5432:5432 -e POSTGRES_PASSWORD=vaga-data1 -v pgdata:/var/lib/postgresql/data postgres

docker start postgres

version: '3' services: db: image: postgres restart: always volumes: - pgdata:/var/lib/postgresql/data environment: POSTGRES_PASSWORD: sua-senha ports: - 5432:5432 volumes: pgdata:

docker-compose up

fluxo>
authenticar > feito 
rotas para usuario e admin 
cadastro de vagas : admin  fiz

fluxo ao logar como candidato ele ira ver um dashboard com vagas para se candidatar

 notificar vagas para o admin do candidato
 
 

Desenvolver uma aplicação web que facilite o processo de recrutamento
interno para os colaboradores da empresa. A aplicação deve permitir aos
usuários pesquisar e candidatar-se a vagas internas, passando por filtros
de requisitos específicos.

Requisitos Funcionais:

● Autenticação e Autorização:
Implementar um sistema de autenticação seguro para os usuários.  done>>>


● Cadastro de Vagas:
Permitir que os administradores cadastrem novas vagas
incluindo informações como título, descrição e requisitos.
Possibilitar a atualização e exclusão de vagas. >>> done

● Candidatura a Vagas:  >>> done
implementar um sistema de candidatura às vagas,
onde os usuários podem expressar interesse em uma posição específica.

Enviar notificações aos responsáveis pela vaga e ao candidato.

cadastrar vaga >  
listar vagas
editar vagas

criar swagger doc - not 
criar compose projeto -afet
criar avaliação de candidatos 
criar testes unitarios 

 ● Painel do Candidato (Bônus): >>
  fazendo
Criar um painel para os candidatos acompanharem o status de suas
candidaturas e receberem feedbacks.

● Avaliação de Candidatos (Bônus):  >>
fazer
Se possível, implementar um sistema de avaliação de candidatos pelos
responsáveis pela vaga, incluindo filtros de requisitos ou tempo de
empresa.
Escopo:

Desenvolver os módulos de frontend e backend de forma separada.

O desenvolvimento do backend deve ser feito em Java 8+.

O desenvolvimento do frontend deve ser feito em Angular.
Preferencialmente utilizar Spring Boot 2.0+ com toda sua stack para o
desenvolvimento do backend.

É aceitável utilizar algumas respostas estáticas em determinadas porções
da aplicação.

Não é necessário submeter uma aplicação que cumpra cada um dos
requisitos descritos, mas o que for submetido deve funcionar.
Utilizar um banco de dados relacional PostgreSQL.
O que será avaliado:

- O código será avaliado seguindo os seguintes critérios:

manutenabilidade, clareza e limpeza de código; resultado funcional;
entre outros fatores.
- Não esqueça de documentar o processo necessário para rodar a

aplicação.
- Diferenciais:
 - Adaptar a página para dispositivos móveis (torná-la responsiva).
- Liberação da aplicação utilizando Docker.
- Utilização de boas práticas de UX na solução.
 - Boa documentação de código e de serviços.
 - testes
