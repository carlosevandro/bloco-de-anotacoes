# Dicas do Terminal

Vou listar alguns comandos que estamos aprendendo:   

- `cd` (navega entre pastas)  
Exemplo para entrar em uma pasta:

```
cd nomeDaPasta
```

- Exemplo para sair de uma pasta:

```
cd ..
```

- `mkdir` (cria pastas)  
Exemplo de como criar uma pasta
```
mkdir nomeDaPasta
```  


# Dicas do Git

- `git init` (começar a seguir as pastas e arquivos de um projeto)  
Esse comando nós utilizamos para começar um projeto com o Git.  
Chamamos a pasta do projeto de repositório ou só repo.  
Pra usar ele só entrar na pasta do seu projeto e executar assim:  
```   
git init
```   

- `git statu` (informa o estado do repo)  
Usando o comando acima você terá como resultado informações de como está o estado dos arquivos e pastas, na verdade você receberá informações apenas dos arquivos e pastas novos, removidos ou alterados.  

- `git add` (segue os arquivos ou pastas no momento atual)  
Com o comando `git status` voc?ê fica sabendo do rolê dos arquivos e pastas e com o `git add` você guarad este momento dos arquivos e pastas para em seguida realizar o commit (não lembra o que commit vê abaxo aí).  

Se você quer guardar o momento de todos os arquivos e pastas só executar o comando abaixo:  
```  
git add .
```  

Mas se você quer pegar apenas alguns arquivos, você pode deixar o comando mais direto, dessa forma:

```  
git add pasta/arquivo
```  

- `git commit` (esse guarda o momento atual)  
Com o `commit` não é mais necessário ficar criando pastas old ou com datas bizarras. Ele é o cara que guarda o momento do seu repo.  
A parte legal é que você deve e pode informar uma mensagem junto com o momento atual para ficar mais fácil de achar esse estado se um dia precisar voltar nele. Ex:  

```  
git commit -m "Anotações do git até o commmit"  
```  

- git log (listas dos estados que guardamos `commit`)  
Com esse comando consegumos ver todos os `commit`s que já fizemos na vida do repo que você estiver :-)  

Mudando uma mensagem de **commit**.
---  

Um erro comum que pode acontecer ao utilizar o **git** é o de cometer um erro de digitação na mensagem do commit, e só perceber o erro após apertar o ENTER.  

Com o comando `git commit --amend`, o usuário pode corrigir o erro do **commit** localmente, antes de realizar um **push**.

### Primeira opção: modificando a mensagem do último commit por uma mensagem de 1 linha:
>
> `git commit --amend -m "nova mensagem de commit"`
> 

### Segunda opção: modificando a mesagem do último commit por uma mensagem com várias linhas:

>  1 - Digite o comando `git commit --amend` . A mensagem será modificada pelo editor padrão configurado no sistema linux (se quiser mudar o editor padrão, digite `sudo update-alternatives --config editor`). Normalmente o editor padraõ é o **vim**.
>  
>  2 - Digite a mensagem que possui várias linhas, salve e saia do editor.
>
> 

Pronto, a mensagem do último commit foi alterada e pode ser visualizada antes do **push** com o comando `git log`.