# Especificações do Projeto: Forest

## 1. Integrantes

Caetano de Medeiros Santana - RGA: 202219070244


## 2. Visão Geral do Software

O "Forest" é um aplicativo para auxiliar os usuários a manterem a concentração durante a realização de atividades como estudos e trabalho. A funcionalidade principal consiste em o usuário definir um temporizador para uma sessão de foco, ao concluir o tempo estabelecido ele é recompensado com uma árvore virtual que é plantada em sua "floresta pessoal", servindo como um incentivo visual para a manutenção da produtividade.

## 3. Papéis e Permissões de Usuários

O sistema foi desenhado com um único papel principal:

    Usuário Registrado: Usuário principal. 

    Suas permissões incluem:
        - Realizar o cadastro e o login no sistema.
        - Gerenciar seu perfil, alterando seus dados.
        - Iniciar sessões de foco com tempos customizados.
        - Acompanhar seu progresso através da visualização de sua floresta.
        - Encerrar a sessão no aplicativo (logout).

## 4. Requisitos Funcionais

 ###  Usuários Permitidos:

O aplicativo permite o cadastro de múltiplos usuários, mas cada usuário só tem acesso aos seus próprios dados e à sua própria floresta.

### O que cada usuário pode fazer:

- Cadastro: Criar uma nova conta com nome, e-mail, senha e foto.

- Login: Acessar o sistema com e-mail e senha.

- Definir Sessão de Foco: Inserir um valor numérico (minutos) para iniciar o temporizador.

- Acompanhar Sessão: Visualizar um cronômetro regressivo durante uma sessão ativa.

- Visualizar Progresso: Acessar uma tela que exibe as árvores ganhas.

### Entradas Necessárias:

- Cadastro: Nome (texto), E-mail (texto), Senha (texto) e Foto (imagem).

- Login: E-mail (texto) e Senha (texto).

- Sessão de Foco: Tempo em minutos (número inteiro).

### Processamento Realizado pelo App:

O sistema valida todos os dados de entrada nos formulários de cadastro e login para garantir que estão completos e nos formatos corretos.

Durante o cadastro, a senha fornecida pelo usuário é processada por um algoritmo de hashing antes de ser salva no banco de dados.

Um cronômetro regressivo é iniciado. O sistema monitora se o app permanece em primeiro plano. Caso o usuário saia do app, a sessão é invalidada.
Ao completar uma sessão com sucesso, uma nova entidade "árvore" é criada e salva no banco de dados, sendo permanentemente associada ao ID do usuário que estava logado.

### Relatórios e Saídas:

- Feedback Visual Imediato: A tela de foco exibe o tempo restante no cronômetro.

- Feedback Sonoro: O sistema emite um som ao final de cada sessão de estudo ou quando uma sessão de estudo é cancelada.

- Notificações: Ao término bem-sucedido de uma sessão, uma notificação do sistema é disparada para informar o usuário sobre sua conquista e a nova árvore.

- Relatório de Progresso: A tela da "floresta" funciona como o principal relatório visual do aplicativo, exibindo a coleção de árvores do usuário e o histórico de sessões de estudo.
