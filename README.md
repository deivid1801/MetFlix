# Projeto Integrador - Modelo
# MetFlix


Um modelo para o desenvolvimento do Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari.

O projeto MetFlix tem como objetivo o desenvolvimento de uma plataforma web para automatizar o processo de locação de filmes e séries de uma locadora.A proposta é criar um sistema completo que permita o gerenciamento do acervo de mídias, cadastro de clientes, controle de empréstimos e devoluções, aplicação de multas por atraso e geração de relatórios estratégicos. 

Professor: [Marco André Mendes](github.com/marcoandre)

Equipe:
- [Deivid Leonardo Mendes da Silva](https://github.com/deivid1801)
- [Brayan Pedroso de Mattos](https://github.com/brayanpedroso)

Links do projeto:
-   [Documentação (esse documento)](github.com/marcoandre/pi-modelo)
-   Backend: [Repositório](github.com/marcoandre/pi-backend) e [Publicação](https://pi-backend.herokuapp.com/)
-   Frontend: [Repositório](github.com/marcoandre/pi-frontend) e [Publicação](https://pi-frontend.herokuapp.com/)



# 1. Desenvolvimento

# **1.1 Modelos de Sistemas**

# **1.1.2 Empréstimo**

O projeto MetFlix foi baseado no modelo de sistema de Empréstimo, pois a proposta consiste em desenvolver uma plataforma de locação de mídias (filmes e séries), cujo funcionamento é semelhante ao de uma biblioteca: o cliente realiza um empréstimo (locação), com data prevista para devolução, podendo sofrer penalidades em caso de atraso.

# 2. Situação‑Problema

A MetFlix é uma locadora de filmes e séries que enfrenta dificuldades operacionais devido à falta de um sistema informatizado. Atualmente, todo o controle de estoque, locações, pagamentos e multas é feito manualmente, por meio de planilhas e anotações em papel. Isso gera erros frequentes, atrasos no atendimento, perda de dados importantes e retrabalho para os funcionários.

Além disso, não há histórico integrado de clientes, as promoções não são aplicadas automaticamente e os relatórios gerenciais são imprecisos e demorados. Esses problemas afetam diretamente a eficiência da equipe e a experiência do cliente.

Um sistema de gerenciamento digital é essencial para automatizar os processos, melhorar o controle do acervo e das locações, garantir a aplicação correta de regras e promoções, e oferecer relatórios confiáveis em tempo real.


# 3. Descrição da Proposta

Será desenvolvido um sistema web responsivo para a MetFlix, com foco na automação de todo o processo de locação de mídias: desde o cadastro de clientes e títulos até devoluções, cobranças e geração de relatórios.

O sistema contará com três tipos de usuários:

- Administrador: gerencia o catálogo, planos de assinatura e acessa relatórios.

- Atendente: realiza locações, devoluções e registra pagamentos.

- Cliente: acessa o catálogo online, faz reservas e consulta seu histórico.

As funcionalidades principais incluem:

- Cadastro e login de clientes e funcionários

- Controle de estoque e locações

- Cálculo de multas e geração automática de boletos

- Reservas online para membros

- Painéis de indicadores com dados em tempo real

- A plataforma vai padronizar os processos da empresa, reduzir o tempo de atendimento e oferecer dados estratégicos para apoiar o crescimento da MetFlix.

# 4. Modelagem de Dados



# 4. Regras de Negócio

RN01. Cadastro único de CPF e e-mail
Cada cliente deve ter um CPF e e-mail únicos no sistema.

Cada funcionário deve ter um e-mail único.

RN02. Tipos de usuário
Existem três tipos de usuários:

Administrador: acesso total ao sistema.

Atendente: apenas operações de atendimento (locações, devoluções, pagamentos).

Cliente: apenas consultas, reservas e histórico próprio.

RN03. Planos de assinatura
Um cliente deve estar vinculado a um plano (ex.: BASICO, PADRAO, PREMIUM) que pode restringir:

Quantidade de mídias simultâneas

Tipo de mídia (ex.: DIGITAL só para planos avançados)
(Essas restrições devem ser definidas nas regras internas do sistema, com base nas políticas da empresa.)

RN04. Controle de estoque
A quantidade de uma mídia disponível deve ser reduzida ao realizar uma locação e aumentada ao registrar a devolução.

Não é permitido locar uma mídia com quantidade igual a zero.

RN05. Devolução e cálculo de multa
Caso a data de devolução seja posterior à data prevista, deve ser calculada uma multa por dia de atraso.

O valor da multa deve ser armazenado na tabela Locacao_Midia.

RN06. Pagamento obrigatório para finalização
Uma locação só será considerada fechada após o registro do pagamento (aluguel e, se houver, multa).

RN07. Reservas
Apenas clientes ativos e logados podem fazer reservas.

O sistema deve permitir uma reserva por título por cliente enquanto o status estiver como pendente.

Reservas vencidas ou não convertidas em locações dentro de um prazo definido (ex.: 24h) devem ser automaticamente canceladas.

RN08. Inativação lógica
Clientes, mídias, e funcionários não devem ser excluídos fisicamente do banco, mas marcados como ativo = 0.

RN09. Histórico de locações e reservas
O cliente pode acessar apenas seu próprio histórico.

O atendente pode acessar o histórico de qualquer cliente.

RN10. Acesso por perfil
Cada funcionalidade do sistema deve ser acessível apenas pelos perfis autorizados:

Administrador: tudo

Atendente: locação, devolução, pagamento, consulta

Cliente: consulta, reserva, histórico pessoal

RN11. Geração de relatórios
Os relatórios devem ser gerados apenas por administradores.

Devem conter dados como: quantidade de locações por período, mídias mais locadas, faturamento mensal, etc.

# 5. Requisitos Funcionais

RF01. Cadastro de Usuários
O sistema deve permitir o cadastro de clientes com nome, CPF, e-mail, telefone, plano, e data de cadastro.

O sistema deve permitir o cadastro de funcionários, com nome, e-mail e cargo.

O sistema deve permitir o cadastro de contas de acesso (usuários) para clientes e funcionários.

RF02. Autenticação e Acesso
O sistema deve permitir que os usuários realizem login com autenticação por senha.

O sistema deve permitir o acesso conforme o tipo de usuário: Administrador, Atendente ou Cliente.

RF03. Gerenciamento de Mídias
O administrador deve poder cadastrar, editar, ativar/desativar mídias, com informações como título, tipo, gênero, ano, classificação e quantidade.

O sistema deve permitir o controle de estoque de mídias com base nas locações e devoluções.

RF04. Gerenciamento de Gêneros
O administrador deve poder cadastrar e editar gêneros de mídia.

RF05. Locação de Mídias
O atendente deve poder registrar uma nova locação com o cliente, mídias, e data prevista de devolução.

O sistema deve permitir o registro de devoluções, atualizando o status da locação e o estoque.

RF06. Cálculo e Registro de Multas
O sistema deve calcular multas por atraso com base na data de devolução e registrar o valor em Locacao_Midia.

RF07. Pagamento
O atendente deve poder registrar pagamentos de aluguel e multas, com método e data.

RF08. Reservas Online
O cliente deve poder consultar o catálogo e reservar mídias online, se disponíveis.

O atendente ou sistema deve poder converter reservas em locações ou cancelá-las.

RF09. Consulta de Histórico
O cliente deve poder consultar seu histórico de locações e reservas no sistema.

O atendente deve poder consultar o histórico de qualquer cliente.

RF10. Gerenciamento de Planos
O administrador deve poder gerenciar os tipos de plano de assinatura disponíveis.

RF11. Painéis e Relatórios
O administrador deve poder acessar painéis com dados em tempo real sobre:

Mídias mais alugadas

Locações por período

Clientes ativos/inativos

Receitas e inadimplência

O sistema deve gerar relatórios gerenciais, exportáveis em PDF/Excel.

RF12. Controle de Acesso
O sistema deve restringir o acesso às funcionalidades de acordo com o tipo de usuário.

# 6. Requisitos Não Funcionais

R.N.F. 01 – Interface Web Responsiva: Compatível com desktop e dispositivos móveis.

R.N.F. 02 – Desempenho: Suportar até 50 usuários simultâneos sem degradação.

R.N.F. 03 – Segurança: Autenticação com senha criptografada; roles e permissões.

R.N.F. 04 – Disponibilidade: Disponível 99,9% do tempo, exceto em manutenção agendada.

R.N.F. 05 – Escalabilidade: Arquitetura em camadas para fácil expansão (microserviços ou módulos).

R.N.F. 06 – Conformidade: Atendimento à LGPD para tratamento de dados de clientes.

R.N.F. 07 – Portabilidade: Deploy em servidores Linux e containers Docker.

R.N.F. 08 – Manutenibilidade: Código documentado e testes automatizados.
