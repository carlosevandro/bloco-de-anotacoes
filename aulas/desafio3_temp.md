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
.
.

