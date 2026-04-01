# Controle de Leitura - App Flutter

## Descrição

Aplicativo desenvolvido em Flutter para simular um controle de leitura. Ele permite que o usuário realize um cadastro simples, faça login (fictício) e visualize os últimos 5 livros lidos.

## Funcionalidades

- Cadastro de usuário com nome, e-mail e senha (validação básica)
- Login fictício utilizando os dados cadastrados e senha fixa `123456`
- Tela Home com mensagem de boas-vindas e lista dos últimos 5 livros
- Navegação entre telas com `Navigator`
- Impedimento de retorno à tela de login após o login bem-sucedido

## Telas

### 1. Cadastro
- Campos: Nome, E-mail, Senha
- Validação: todos os campos obrigatórios, e-mail com "@", senha com mínimo de 6 caracteres
- Ao cadastrar, o usuário é levado para a tela de login

### 2. Login
- Campos: E-mail, Senha
- Validação: e-mail obrigatório e com "@"
- Para login, a senha deve ser `123456` (simulação) e o e-mail deve coincidir com o cadastrado
- Sucesso navega para a Home

### 3. Home
- Saudação personalizada com o nome do usuário
- Lista dos últimos 5 livros lidos (título e autor)
- Botão de voltar do app bar removido para evitar retorno ao login

## Conceitos Utilizados

- **Flutter** e **Dart** – framework e linguagem
- **Widgets** – `StatelessWidget`, `StatefulWidget`, `Scaffold`, `Form`, `TextFormField`, `ListView`, `Card`, etc.
- **Gerenciamento de estado** – `setState` (embora utilizado apenas no cadastro/login, poderia ser expandido)
- **Navegação** – `Navigator.pushReplacement` para evitar pilha de telas desnecessária
- **Validação de formulários** – `Form` com `GlobalKey<FormState>` e `validator`
- **Modelagem de dados** – classe `Livro` para representar os livros
