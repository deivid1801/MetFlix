# Projeto Integrador - Modelo
*(Coloque aqui o nome do seu projeto.)*

Um modelo para o desenvolvimento do Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari.
*(Coloque aqui uma breve descrição do seu projeto.)*

**IMPORTANTE**: [**Cadastre seu projeto nesse link**](https://docs.google.com/spreadsheets/d/1KXuMJ9TK7GPyahR_BfLwfn4ec7vX7DgiHx42vFc4E7g/edit?usp=sharing).

Professor: [Marco André Mendes](github.com/marcoandre)

Equipe:
- [Aluno1](github.com/aluno1)
- [Aluno2](github.com/aluno2)

Links do projeto:
(*Coloque aqui os links para a documentação do projeto e os repositórios e plubicação do backend e frontend.*)
-   [Documentação (esse documento)](github.com/marcoandre/pi-modelo)
-   Backend: [Repositório](github.com/marcoandre/pi-backend) e [Publicação](https://pi-backend.herokuapp.com/)
-   Frontend: [Repositório](github.com/marcoandre/pi-frontend) e [Publicação](https://pi-frontend.herokuapp.com/)

**Como usar esse modelo para o Projeto Integrador**

*(Essa parte pode ser apagada depois.)*

1. Faça um fork desse repositório para a sua conta do GitHub.
2. Clone o repositório para o seu computador.
3. Abra o arquivo README.md no seu editor de texto favorito (recomendamos o [Visual Studio Code](https://code.visualstudio.com/)).
4. Tenha instaladas as seguintes extensões:
   - [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
   - [TODO Highlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight)
5. Edite o arquivo README.md com as informações do seu projeto.

# 1. Desenvolvimento
*(Escolha um dos modelos de sistemas para desenvolver o projeto. Apague as informações desnecessárias depois.)*
-   As equipes serão avaliadas por cada etapa da documentação e entregas realizadas.
-   Cada equipe deverá escolher um sistema para o desenvolvimento das atividades, a partir dos modelos apresentados.

**1.1 Modelos de Sistemas**

**Nessa parte a equipe deve escolher um dos modelos de sistemas para desenvolver o projeto. Ao escolher, escreva uma breve descrição do sistema e o motivo da escolha e pode apagar os outros modelos.**

**1.1.2 Empréstimo**

**Gerenciamento de uma biblioteca**

Uma ONG, chamada Sala Arco Íris, ajuda crianças de baixa renda em sua educação básica. Atualmente, recebeu uma doação de mais de 1000 livros e está montando a sua biblioteca. Eles querem emprestar os livros para as crianças e os pais das crianças. Apesar de
terem um computador e as estantes necessárias à disposição nessa nova biblioteca, não possuem verba suficiente para um leitor de impressão digital ou para produção
de carteirinhas para todas as crianças. Para isso, eles precisam de um sistema que gerencie todo o acervo, empréstimos, livros disponíveis, etc. mas que isso ocorra de maneira simples e sem necessidade de novos gastos. Também é importante que haja relatórios, permitindo o controle dos empréstimos e dos livros disponíveis no acervo.

2. Situação‑Problema

Introdução

A MetFlix é uma empresa fictícia de aluguel de filmes e séries fundada há 5 anos pelo empreendedor Paulo Cardoso. Atualmente, MetFlix conta com uma loja física localizada em São Paulo, além de um pequeno portal online que registra apenas catálogos, mas não executa processos de locação. A equipe é composta por:

Proprietário/Gestor: Paulo Cardoso

Atendentes: 3 funcionários responsáveis pelo atendimento ao cliente e processos de aluguel/retorno

Equipe de Estoque: 2 funcionários responsáveis pela organização dos acervos e manutenção dos discos físicos

Suporte Técnico: terceirizado para manutenção básica de hardware e da página de catálogo

Situação‑problema

Gerenciamento Manual de Inventário: todo o controle de disponibilidade de filmes e séries é feito em planilhas do Excel e anotações em papéis. Isso gera divergências frequentes entre o estoque físico e o que consta disponível.

Processo de Locação Fragmentado:

O atendente verifica manualmente a identidade do cliente e sua elegibilidade (nenhuma pendência de devolução)

Consulta a planilha para confirmar se o título está disponível fisicamente

Abre uma ficha de locação em papel, registra data de retirada e previsão de devolução (3 dias por padrão)

Controle de Pagamentos e Multas:

Pagamentos de aluguel e eventuais multas (R$ 5,00 ao dia de atraso) são lançados manualmente no caixa.

Boletos gerados de forma externa quando o cliente atrasa mais de 7 dias.

Experiência do Cliente:

Não há histórico de aluguéis integrado; atendentes dependem de memória ou das fichas de papel.

Promoções para membros Premium não são aplicadas automaticamente.

Relatórios Gerenciais:

Relatórios mensais de locação, faturamento e itens mais alugados são extraídos manualmente das planilhas, consumindo muito tempo.

Conclusão

A MetFlix enfrenta atrasos, retrabalho e falhas de comunicação entre inventário, caixa e atendimento, resultando em baixo nível de satisfação do cliente e perda de receita por multas não cobradas. Um sistema integrado de gerenciamento de locações, estoque e pagamentos pode automatizar processos, minimizar erros e prover indicadores em tempo real para melhor tomada de decisão.

3. Descrição da Proposta

O software proposto para a MetFlix será uma plataforma web responsiva com foco em gerenciamento completo de aluguel de mídias, desde o cadastro de clientes e títulos até o controle de devoluções e emissão de relatórios.

Foco de Ação: automatizar o ciclo de locação (consulta de catálogos, registro de empréstimos, controle de devolução e cobranças).

Níveis de Usuário:

Administrador: configura catálogo, planos de assinatura, e acessa relatórios estratégicos;

Atendente: registra aluguéis, devoluções e pagamentos;

Cliente (usuário externo): visualiza catálogo online, faz reservas e consulta histórico de locações.

- Funcionalidades Principais:

Cadastro e autenticação de clientes e funcionários

Registro e acompanhamento de débitos e multas

Disponibilidade de reservas online para membros registrados

Geração automática de boletos e recibos

Painéis de indicadores (disponibilidade de estoque, itens mais locados, multas pendentes)

Com esta solução, MetFlix terá processos padronizados, menor tempo de atendimento e melhores insights para ações de marketing e expansão.

4. Modelagem de Dados

Entidades Principais:

Cliente (Customer): id, nome, CPF, e-mail, telefone, plano (Básico/Premium), data de cadastro

Funcionario (Staff): id, nome, login, senha, nível (Atendente/Administrador)

Mídia (MediaItem): id, título, tipo (Filme/Série), gênero, ano, classificação indicativa, status (Disponível/Alugado/Reservado)

Gênero (Genre): id, descrição

Locação (RentalTransaction): id, cliente_id, data_retirada, data_prevista_devolucao, data_devolucao, status (Em Aberto/Concluído)

Pagamento (Payment): id, transacao_id, valor_aluguel, valor_multa, data_pagamento, método (Dinheiro/Cartão/Online)

Reserva (Reservation): id, cliente_id, midia_id, data_reserva, status (Ativa/Cancelada)

Relacionamentos:

Um Cliente pode gerar múltiplas Locações e Reservas.

Cada Locação gera um ou mais Pagamentos (aluguel + eventual multa).

Uma Mídia possui um Gênero e pode estar associada a várias Locações e Reservas.

(Diagrama Entidade-Relacionamento desenvolvido na próxima fase.)

4. Regras de Negócio

RN01 – Elegibilidade para Locação: Cliente só pode alugar se não possuir locações em aberto ou multas pendentes.

RN02 – Período de Locação: Prazo padrão de 3 dias corridos, não prorrogável após 1 dia de atraso.

RN03 – Limite de Itens: Plano Básico: até 3 itens simultâneos; Plano Premium: até 5 itens.

RN04 – Multa por Atraso: R$ 5,00 por dia de atraso a partir do quarto dia.

RN05 – Reserva de Mídias: Apenas clientes com plano Premium podem reservar títulos indisponíveis.

RN06 – Desconto Premium: Clientes Premium recebem 10% de desconto no valor de aluguel.

RN07 – Geração de Boleto: Boleto gerado automaticamente se multa acumulada ultrapassar R$ 50,00.

RN08 – Visualização de Relatórios: Apenas Administradores têm acesso completo a relatórios financeiros e de uso.

5. Requisitos Funcionais

Entradas

R.F. 01 – Cadastro de Cliente: Permite registrar novo cliente; dados necessários: nome, CPF, e-mail, plano; usuários: Atendente, Administrador.

R.F. 02 – Cadastro de Mídia: Permite inserir novo título; dados necessários: título, tipo, gênero, ano; usuários: Administrador.

R.F. 03 – Registro de Locação: Captura dados de aluguel; dados necessários: cliente_id, midia_id, data_retirada; usuários: Atendente.

Processos

R.F. 04 – Autenticação de Usuário: Verifica login/senha e define nível de acesso; dados necessários: login, senha; usuários: todos.

R.F. 05 – Cálculo de Multa: Calcula valor de multa conforme dias de atraso; dados necessários: data_prevista, data_devolucao; usuários: sistema.

R.F. 06 – Geração de Boletos: Emite boleto eletrônico para pagamento de multa; dados necessários: cliente_id, valor; usuários: sistema.

Saídas

R.F. 07 – Relatório de Locação: Exibe lista de aluguéis por período; dados necessários: cliente, título, datas; usuários: Administrador.

R.F. 08 – Painel de Estoque: Mostra disponibilidade de mídias; dados necessários: título, status; usuários: Atendente, Administrador.

R.F. 09 – Histórico de Cliente: Lista todas as transações e pagamentos de um cliente; dados necessários: id_cliente; usuários: Atendente, Cliente.

6. Requisitos Não Funcionais

R.N.F. 01 – Interface Web Responsiva: Compatível com desktop e dispositivos móveis.

R.N.F. 02 – Desempenho: Suportar até 50 usuários simultâneos sem degradação.

R.N.F. 03 – Segurança: Autenticação com senha criptografada; roles e permissões.

R.N.F. 04 – Disponibilidade: Disponível 99,9% do tempo, exceto em manutenção agendada.

R.N.F. 05 – Escalabilidade: Arquitetura em camadas para fácil expansão (microserviços ou módulos).

R.N.F. 06 – Conformidade: Atendimento à LGPD para tratamento de dados de clientes.

R.N.F. 07 – Portabilidade: Deploy em servidores Linux e containers Docker.

R.N.F. 08 – Manutenibilidade: Código documentado e testes automatizados.

7. Diagrama de Caso de Uso

Atores

Cliente: Browsing e reserva de títulos, consulta histórico.

Atendente: Realiza locação, devolução e pagamento.

Administrador: Gera relatórios, cadastra mídias e gerencia usuários.

Casos de Uso Principais

Autenticar Usuário (incluído por todos)

Registrar Cliente

Cadastrar Mídia

Buscar Catálogo

Realizar Locação

Registrar Devolução

Calcular Multa (extensão de Devolução)

Gerar Boleto (extensão de Calcular Multa)

Gerar Relatórios

