# Fluxo De Execução

## 1. Inicialização do Programa

- **Arquivo Principal:** Quando o programa é executado, ele começa pela seguinte linha:

  ```python
  if __name__ == "__main__":
      root = tk.Tk()
      app = BibliotecaApp(root)
      root.mainloop()
  ```
### O que Acontece:
* tk.Tk() cria uma instância da janela principal da aplicação (chamada de root).
* A classe BibliotecaApp é inicializada com root como argumento, o que configura a interface gráfica e todas as funcionalidades do aplicativo.
* O método root.mainloop() inicia o loop principal do tkinter, mantendo a janela aberta para interação do usuário.

## Instanciação da Classe BibliotecaApp

```python
app = BibliotecaApp(root)
```

### O que Acontece:

* O construtor __init__ da classe BibliotecaApp é executado:
  * Cria o frame principal (self.main_frame) para a interface gráfica.
  * Adiciona botões ao frame principal para cada funcionalidade: "Cadastrar Livro", "Cadastrar Usuário", "Visualizar Livros" e "Visualizar Usuários".
  * Associa cada botão a um método específico (command) para tratar a ação correspondente, como self.cadastro_livro para o botão "Cadastrar Livro".

## Ação do Usuário: Cadastro de Livros
**Botão Clicado:** "Cadastrar Livro"

**Método Chamado:** 
```python
BibliotecaApp.cadastro_livro()
```

### O que Acontece:

* Esconde o frame principal (self.main_frame.pack_forget()).
* Cria um novo frame (cadastro_livro_frame) para a tela de cadastro de livros.
* Adiciona campos de entrada (Entry) para o título, autor e ISBN do livro.
* Adiciona dois botões: "Salvar" e "Voltar":
#### "Salvar":
  * Associado ao método salvar_livro, que:
  * Recupera os dados inseridos.
  * Cria um objeto Livro com os dados.
  * Adiciona o objeto Livro à lista de livros na instância da Biblioteca.
  * Retorna ao frame principal.
#### "Voltar":
* Associado ao método BibliotecaApp.voltar(), que:
* Oculta o frame atual (cadastro_livro_frame.pack_forget()) e exibe o frame principal (self.main_frame.pack()).

## Ação do Usuário: Cadastro de Usuários
**Botão Clicado:** "Cadastrar Usuário"

**Método Chamado:** 
```python
BibliotecaApp.cadastro_usuario()
```
### O que Acontece:

* Esconde o frame principal (self.main_frame.pack_forget()).
* Cria um novo frame (cadastro_usuario_frame) para a tela de cadastro de usuários.
* Adiciona campos de entrada (Entry) para o nome e a matrícula do usuário.
* Adiciona dois botões: "Salvar" e "Voltar":
#### "Salvar":
* Associado ao método salvar_usuario, que:
* Recupera os dados inseridos.
* Cria um objeto Usuario com os dados.
* Adiciona o objeto Usuario à lista de usuários na instância da Biblioteca.
* Retorna ao frame principal.
#### "Voltar":
* Associado ao método BibliotecaApp.voltar(), que:
* Oculta o frame atual (cadastro_usuario_frame.pack_forget()) e exibe o frame principal (self.main_frame.pack()).

## Ação do Usuário: Visualização de Livros
**Botão Clicado:** "Visualizar Livros"

**Método Chamado:** 
```python
BibliotecaApp.visualizar_livros()
```
### O que Acontece:

* Esconde o frame principal (self.main_frame.pack_forget()).
* Cria um novo frame (visualizar_livros_frame) para exibir a lista de livros cadastrados.
* Itera sobre a lista de livros na instância da Biblioteca:
* Para cada Livro, cria um Label com suas informações (título, autor, ISBN).
#### Adiciona o botão "Voltar":
* Associado ao método BibliotecaApp.voltar(), que:
* Oculta o frame atual (visualizar_livros_frame.pack_forget()) e exibe o frame principal (self.main_frame.pack()).

## Ação do Usuário: Visualização de Usuários
**Botão Clicado:** "Visualizar Usuários"

**Método Chamado:** 
```python
BibliotecaApp.visualizar_usuarios()
```
#### O que Acontece:

* Esconde o frame principal (self.main_frame.pack_forget()).
*Cria um novo frame (visualizar_usuarios_frame) para exibir a lista de usuários cadastrados.
*Itera sobre a lista de usuários na instância da Biblioteca:
 *Para cada Usuario, cria um Label com suas informações (nome, matrícula).
#### Adiciona o botão "Voltar":
* Associado ao método BibliotecaApp.voltar(), que:
* Oculta o frame atual (visualizar_usuarios_frame.pack_forget()) e exibe o frame principal (self.main_frame.pack()).
## Voltar à Tela Principal
**Botão Clicado:** "Voltar" em qualquer tela (Cadastro de Livros, Cadastro de Usuários, Visualização de Livros, Visualização de Usuários).

**Método Chamado:**
```python
BibliotecaApp.voltar(frame)
```
#### O que Acontece:

* O método voltar():
* Oculta o frame atual (frame.pack_forget()).
* Exibe o frame principal (self.main_frame.pack()).

## Encerramento do Programa
#### Como Funciona:
* O programa permanece em execução até que a janela seja fechada manualmente pelo usuário.
* Quando a janela é fechada, o loop principal (mainloop()) termina, e o programa finaliza sua execução.
