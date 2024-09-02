# GerenciamentoDeBiblioteca

## 1. Classe ItemBiblioteca
classe que representa os itens da biblioteca. possui um único atributo:

### Atributos:
**titulo**: o título do item da biblioteca (no caso de livros, o título do livro; no caso de usuários, o nome do usuário).

Esta classe é usada como uma base para outras classes (Livro e Usuario), que herdam dela e estendem sua funcionalidade.

## 2. Classe Livro
A classe herda de ItemBiblioteca e representa um livro na biblioteca.

### Atributos:

titulo: herdado de ItemBiblioteca, representa o título do livro.
autor: o autor do livro.
isbn: o ISBN, um identificador único para o livro.

#### Função no Programa:

Representa os livros armazenados na biblioteca.

## 3. Classe Usuario
A classe Usuario herda de ItemBiblioteca e representa um usuário da biblioteca.

### Atributos:

titulo: herdado de ItemBiblioteca, representa o nome do usuário.
matricula: o número de matrícula do usuário, identificador único para cada usuário.
#### Função no Programa:

Representa os usuários da biblioteca, mantendo informações como nome e matrícula.

## 4. Classe Biblioteca
A classe Biblioteca é responsável por armazenar e gerenciar os livros e usuários.

### Atributos:

livros: lista que armazena todos os Livros adicionados à biblioteca.
usuarios: lista que armazena todos os Usuarios registrados na biblioteca.
**Métodos:**

adicionar_livro(self, livro): adiciona um Livro para a lista livros.
adicionar_usuario(self, usuario): adiciona um Usuario para a lista usuarios.
#### Função no Programa:

ser um banco de dados simples que armazena as informações sobre os livros e usuários da biblioteca.

## 5. Classe GerenciadorDePedidos
gerencia as solicitações de empréstimo pelos usuários.

### Atributos:

biblioteca: uma instância da classe Biblioteca, usada para acessar a lista de livros disponíveis.
pedidos: uma lista que armazena tuplas de pedidos no formato (usuario, livro), onde cada tupla representa um pedido de empréstimo.
**Métodos:**

solicitar_livro(self, usuario, livro): permite que um usuário solicite um livro. Verifica se o livro está disponível na biblioteca. Se estiver, adiciona o pedido à lista pedidos e retorna True; caso contrário, retorna False.
#### Função no Programa:

Gerencia os empréstimos, verificando a disponibilidade de livros e registrando as solicitações feitas pelos usuários.

## 6. Classe BibliotecaApp

Esta classe implementa a interface gráfica do usuário.

### Atributos:

root: a janela principal do aplicativo tkinter.
biblioteca: uma instância da classe Biblioteca, usada para acessar e modificar os dados de livros e usuários.
main_frame: um Frame principal que contém os botões para as diferentes opções do aplicativo.
**Métodos:**

__init__(self, root): inicializa a GUI, criando a janela principal e configurando os botões para diferentes ações:

Cadastrar Livro
Cadastrar Usuário
Visualizar Livros
Visualizar Usuários

cadastro_livro(self): exibe a tela de cadastro de livros, permitindo ao usuário inserir informações sobre um novo livro e salvá-lo na biblioteca.
cadastro_usuario(self): exibe a tela de cadastro de usuários, permitindo ao usuário inserir informações sobre um novo usuário e salvá-lo na biblioteca.
visualizar_livros(self): exibe uma lista de todos os livros cadastrados na biblioteca.
visualizar_usuarios(self): exibe uma lista de todos os usuários cadastrados na biblioteca.
voltar(self, frame): oculta o frame atual e exibe o frame principal (main_frame).

#### Função no Programa:

Fornece uma interface gráfica para o usuário interagir com o sistema da biblioteca, permitindo cadastrar livros, cadastrar usuários e visualizar ambos.

## 7. Inicialização do Aplicativo (if __name__ == "__main__":)
inicializa o aplicativo.
