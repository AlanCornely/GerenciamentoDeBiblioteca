# BibliotecaApp

Um sistema simples de gerenciamento de biblioteca com interface gráfica desenvolvido em Python utilizando o `tkinter`.

## Descrição do Projeto

Este programa simula o funcionamento básico de uma biblioteca, permitindo ao usuário cadastrar novos livros e usuários, visualizar os itens cadastrados, e gerenciar pedidos de empréstimos de livros. A interface gráfica foi criada com `tkinter` para proporcionar uma experiência de usuário intuitiva e interativa.

## Funcionalidades

### 1. Cadastro de Livros

Permite ao usuário adicionar novos livros ao sistema da biblioteca.

- **Como Funciona:**
  - Clique no botão **"Cadastrar Livro"**.
  - Insira as informações do livro: título, autor e ISBN.
  - Clique em **"Salvar"** para adicionar o livro ao sistema.
  - Clique em **"Voltar"** para retornar à tela principal.

- **Propósito:**
  - Adicionar novos livros ao sistema para que possam ser gerenciados e emprestados.

### 2. Cadastro de Usuários

Permite adicionar novos usuários ao sistema da biblioteca.

- **Como Funciona:**
  - Clique no botão **"Cadastrar Usuário"**.
  - Insira as informações do usuário: nome e matrícula.
  - Clique em **"Salvar"** para adicionar o usuário ao sistema.
  - Clique em **"Voltar"** para retornar à tela principal.

- **Propósito:**
  - Adicionar novos usuários ao sistema para que possam solicitar empréstimos de livros.

### 3. Visualização de Livros

Permite visualizar todos os livros cadastrados na biblioteca.

- **Como Funciona:**
  - Clique no botão **"Visualizar Livros"**.
  - Veja a lista de livros com suas informações (título, autor e ISBN).
  - Clique em **"Voltar"** para retornar à tela principal.

- **Propósito:**
  - Permitir ao usuário visualizar os livros disponíveis na biblioteca.

### 4. Visualização de Usuários

Permite visualizar todos os usuários cadastrados na biblioteca.

- **Como Funciona:**
  - Clique no botão **"Visualizar Usuários"**.
  - Veja a lista de usuários com suas informações (nome e matrícula).
  - Clique em **"Voltar"** para retornar à tela principal.

- **Propósito:**
  - Permitir ao usuário visualizar todos os usuários registrados no sistema da biblioteca.

### 5. Navegação entre Telas

Permite a navegação entre diferentes telas (ou frames) para realizar diversas ações.

- **Como Funciona:**
  - Use os botões de navegação para transitar entre diferentes funcionalidades.
  - O botão **"Voltar"** está disponível em todas as telas de ação para retornar à tela principal.

- **Propósito:**
  - Proporcionar uma experiência de navegação fluida e intuitiva.

### 6. Inicialização do Aplicativo

O programa é executado e inicia a interface gráfica, preparando o ambiente para o usuário.

- **Como Funciona:**
  - O código é executado na seção `if __name__ == "__main__":`.
  - Cria a janela principal e inicializa o aplicativo `BibliotecaApp`.
  - Mantém a janela aberta para interações do usuário através do loop principal `root.mainloop()`.

- **Propósito:**
  - Inicializar o aplicativo e preparar o ambiente para interação do usuário.

## Como Executar

1. Certifique-se de ter o Python instalado em seu ambiente.
2. Clone este repositório em sua máquina local.
3. Execute o arquivo principal do programa (por exemplo, `biblioteca_app.py`).

```bash
python biblioteca_app.py
