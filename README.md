# AJUDA
## Criar shave SSH

Rode o comando abaixo trocando o "your_email@example.com" pelo seu e-mail cadastrado no github    

    **ssh-keygen -t ed25519 -C "your_email@example.com"**

*Na mensagem Abaixo Pressione [Enter]*

`Enter a file in which to save the key (/c/Users/YOU/.ssh/id_ALGORITHM):`

**Na mensagem abaixo informe sua senha**
> **Obs: Não vai aparecer nada**

`Enter passphrase (empty for no passphrase):`

`Enter same passphrase again:`

Feito esse processo acima, está na hora de copiar a chave para o GitHub.

**Windows**

```terminal
clip < ~/.ssh/id_ed25519.pub    
```
**Linux**
```terminal
cat ~/.ssh/id_ed25519.pub
```
Feito isso, só colar no perfil do GitHub.<p>
**[Settings >>> SSH and GPG keys >>> New SSH key](https://github.com/settings/ssh/new)**
</p>

## Comandos Terminal
1. `mkdir [nome Pasta]` **= Cria uma pasta**
2. `cd [nomePasta]` **Entra na pasta**
3. `cd ..`**Volta uma pasta**
4. `cls || clear`**Limpa tela**
------
## comandos Git
  * `git clone <link_ssh>`
  * `git add .`
  * `git commit -m "Commitando respostas`
  *  `git push` **"Envia para o GitHub"**

----------
## Erros

 ### `$![Rejected] -> Master -> Master (non-fast-foward)`
 
 Significa que foi feita uma alteração na nuvem e está dando conflito com algum arquivo.
 Solução:

 `git pull` **= Baixa todas as diferenças não sincronizadas.**
 
 ----
### `Author identity unknown`

`***Please tell me who you are.***`

Esse erro acima, informa que não é possivel identificar o autor do commit, e pede que seja informado alguns dados como E-mail e usuario do `GitHub`<br>
Para resolver esse problema rode o comando abaixo alterando o "you@example.com" para o seu e-mail do `GitHub`e altere também "**Your Name**" para seu nome.
```
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```
----