# USO DO MARKDOWN 

### O texto fica formatado similiar aos emails em texto puro de antigamente. Fica mais legível que o HTML, pois não tem TAGS para atrapalhar a leitura do código formatado, e os códigos utilizados no MarkDown parecem com a formatação de textos de email em ASCII, bastante populares antigamente, antes dos emails com texto em HTML se popularizarem.

### Marknown não substitui HTML. È utilizado por facilitar a digitação e convertido para o HTML. Para qualquer marcação que não é coberta pela sintaxe do Marknown, o usuário pode simplesmente utilizar HTML, porém existem algumas restrições. 




Elementos HTML de nível de bloco, como ```<div>, <table>, <pre>, <p>```, dentre outros, devem estar separados do conteúdo anterior e posterior do bloco por linhas em branco, e as tags de início e fim do bloco não devem ser indentadas com tabulações ou espaços.

    Exemplo:

	Texto antes do bloco, separado por um espaço em branco.

	<table>
		<tr>
			<td>Foo</td>
		</tr>
	</table>

	Texto depois do bloco, separado por um espaço em branco.
	Antes da tag tag <table> e </table> não existem espaços ou tabulações.

A sintaxe de formatação do Marknown **não é** processada dentro de tags HTML de nível de bloco.
	
*Span level HTML tags* (`<span>, <cite>, or <del>`) podem ser utilizadas em qualquer lugar. A sintaxe do Marknown é processada dentro de *span-level tags*.

In HTML, there are two characters that demand special treatment: 

< and &. 

Left angle brackets are used to start tags; 
ampersands are used to denote HTML entities. 
If you want to use them as literal characters, you must escape them as entities, e.g. &lt;, and &amp;.

Markdown allows you to use these characters naturally, taking care of all the necessary escaping for you. 
If you use an ampersand as part of an HTML entity, it remains unchanged; otherwise it will be translated into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

&copy;

and Markdown will leave it alone. But if you write:

AT&T

Markdown will translate it to:

AT&amp;T

Similarly, if you use angle brackets as delimiters for HTML tags, Markdown will treat them as such. But if you write:

4 < 5

Markdown will translate it to:

4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and ampersands are always encoded automatically. This makes it easy to use Markdown to write about HTML code.

-------------------------------------------------------------------------------------  
------------------------------------------------------------------------------------- 
-------------------------------------------------------------------------------------

# DICAS DE COMANDOS DE FORMATAÇÃO DO MARKDOWN #

# TÍTULOS #

> ```text
> Título com H1  (Setext-style)
> ============= 
> ```
> 
> Título com H1  (Setext-style)
> ============= 
>
> ```text
> Título com H2  (Setext-style)  
> --------------  
> ```
> 
> Título com H2  (Setext-style)  
> --------------  
</br></br>

> ```text 
> # Título com H1   (Atx-style)
> 
> ## Título com H2   (Atx-style) 
> 
> ### Título com H3   (Atx-style)
> 
> #### Título com H4   (Atx-style)
> 
> ##### Título com H5   (Atx-style)
> 
> ###### Título com H6   (Atx-style)   
> ```
> 
> # Título com H1   (Atx-style)
> 
> ## Título com H2   (Atx-style)
> 
> ### Título com H3   (Atx-style)
> 
> #### Título com H4   (Atx-style)
> 
> ##### Título com H5   (Atx-style)
> 
> ###### Título com H6   (Atx-style)   
> 

**NOTA:** Pode-se adicionar hashtag (`#`) no fim do título também, porém a quantidade é irrelevante.  
Exemplo:  
> ```text
> ### Exemplo de `<h3>` ###
> ```
> ### Exemplo de `<h3>` ###
>
> 
> ```text
> ### Exemplo de `<h3>` de novo!!! ###
> ```
> ### Exemplo de `<h3>` de novo!!! #
>
</br>

-----------------------------------
-----------------------------------
-----------------------------------

# PARÁGRAFOS
É apenas uma ou mais linhas consecutivas de texto separadas por uma ou mais linhas em branco. Infelizmente, por causa dessa definição, se quiser um espaçamento vertical maior que uma linha, é necessário a adição da tag `</br>`.

Parágrafos normais não são indentados com espaços ou tabulações.

Se não quiser deixar uma ou mais linhas em branco entre dois parágrafos, é só terminar o primeiro parágrafo com 2 ou mais espaços em branco.  

Exemplo:
> ```text
> Primeira linha, terminada com apenas um enter.
> Segunda linha.
>
> 
> Agora esta linha vai terminar com dois espaços em branco e enter.  
> Outra linha.
>
> 
> Separado por uma linha em branco.
>
> Outra linha.
>
> 
> Dois espaços em branco e separado por uma linha em branco.  
>
> Outra linha.
> ```
>
>
>
> Primeira linha, terminada com apenas um enter.
> Segunda linha.
>
> 
> Agora esta linha vai terminar com dois espaços em branco e enter.  
> Outra linha.
>
> 
> Separado por uma linha em branco.
>
> Outra linha.
>
> 
> Dois espaços em branco e separado por uma linha em branco.  
>
> Outra linha.

</br></br>

-----------------------------------
-----------------------------------
-----------------------------------

# Quebras de Linha adiconais # 

Pode-se utilizar a tag `</br>`.

Exemplo:
> ```text
> Antes.
> </br></br></br>
> Depois.
> ```
> Antes.
> </br></br></br>
> Depois.  
>  

</br></br>
  
-----------
-----------
-----------

# LINHAS HORIZONTAIS # 

É só digitar très ou mais asteriscos (`*`) ou traços (`-`) ou underscore (`_`), separados ou não por espaços. A única limitação fica por conta dos traços, que não podem ser em uma linha logo após um texto, porque senão será entendido que é um título nível `<h2>`.

Exemplos: 

> Linha horizontal logo após este texto. Adicionar um linha em branco entre o texto e a formatação de linha horizontal.
> 
> -----------------------------
> Outra linha horizontal:
> ***********************
>
> Mais uma:
> _________
>



</br>

-----------------------------------
-----------------------------------
-----------------------------------


# Ênfase em um texto #  
## Dando ênfase em alguma palavra ou trecho do texto. # 
  
- Ênfase (itálico)
> *ITÁLICO*  
> _ITÁLICO_

- ÊNFASE FORTE (negrito)
> **NEGRITO**  
> __NEGRITO__

- Itálico e negrito  
> ***ITÁLICO E NEGRITO***  
> _**ITÁLICO E NEGRITO**_  
> *__ITÁLICO E NEGRITO__*

```
*ITÁLICO*  
_ITÁLICO_

**NEGRITO**  
__NEGRITO__

***ITÁLICO E NEGRITO***
_**ITÁLICO E NEGRITO**_
*__ITÁLICO E NEGRITO__*

```

**NOTA**: Pode ser utilizado no meio de uma palavra.  

Exemplo:  
```text
Para*lele*pípedo
```
Para*lele*pípedo  

```text
Para\*lele\*pípedo
```
Para\*lele\*pípedo  

Dando ênfase em alguma palavra ou trecho do texto.

    Some of these words *are emphasized*.

- Some of these words *are emphasized*.
-

    Some of these words _are emphasized also_.

- Some of these words _are emphasized also_.
- 

    Use two asterisks for **strong emphasis**.

- Use two asterisks for **strong emphasis**.
- 


Or, if you prefer, __use two underscores instead__.

- Or, if you prefer, __use two underscores instead__.

### TEXTO TACHADO/RISCADO###
- ~~TEXTO TACHADO~~
```text
~~TEXTO TACHADO~~
```

-----------------------------------
-----------------------------------
-----------------------------------

# BLOCOS DE CITAÇÃO (_BLOCKQUOTES_) #

```text
## Podem ser utilizados com sub-níveis.
> Nível 1 do bloco de citação.  
> Outros níveis:  
>> Nível 2   
>>> Nível 3  
>>>> Nível 4  
>>>>> Nível 5  
>>>>>> Nível 6.  
>>>>>> Infelizemente terá que usar um texto ou uma tag `</br>` para poder ficar um espaço vertical na parte inferior ao sub-nível 6. Os níveis 5 e 4 estão sem a tag `</br>` na parte inferior, já os níveis 3, 2 e 1 possuem a tag de quebra de linha.
>>>>> 
>>>>> 
>>>>> 
>>>>
>>>> 
>>>
>>>  </br>
>>   
>> </br>
>
> </br>
```

## Podem ser utilizados com sub-níveis.
> Nível 1 do bloco de citação.  
> Outros níveis:  
>> Nível 2   
>>> Nível 3  
>>>> Nível 4  
>>>>> Nível 5  
>>>>>> Nível 6.  
>>>>>> Infelizemente terá que usar um texto ou uma tag `</br>` para poder ficar um espaço vertical na parte inferior ao sub-nível 6. Os níveis 5 e 4 estão sem a tag `</br>` na parte inferior, já os níveis 3, 2 e 1 possuem a tag de quebra de linha.
>>>>> 
>>>>> 
>>>>> 
>>>>
>>>> 
>>>
>>>  </br>
>>   
>> </br>
>
> </br>

```
>
> Esta é uma citação em bloco (blockquote).
> 
> Se digitar algum comando do MarkDown dentro de um blockquote, ele aparecerá.
>
```
>
> Esta é uma citação em bloco (*blockquote*).
> 
> Este é o primeiro nível de uma citação.  
>
>> Este é o segundo nível.
>
> > Este é o terceiro, e por aí vai...
> 
> Voltando para o primeiro nível.
> Tem que digitar algo para voltar ou então criar uma linha digitando no mínimo 3 '-', '_' ou '*'.  
> Pode também utilizar a tag `</br>` para aumentar o espaçamento vertical.
> </br></br></br>  

-----------------------------------
-----------------------------------
-----------------------------------

# LISTAS

- ## LISTAS NÃO-ORDENADAS ##  
Podem ser criadas listas não-ordenadas digitando os itens da lista em linhas separadas e inciando a linha com um dos seguintes caractéres: `-`, `+` e `*`.  

```text
Exemplo 1:
- Maçã
- Uva
- Pera

Exemplo 2:
+ Feijão
+ Arroz
+ Macarrão

Exemplo 3:
* Gato
* Cachorro
* Passarinho
```

> Exemplo 1:
> - Maçã
> - Uva
> - Pera
> 
> Exemplo 2:
> + Feijão
> + Arroz
> + Macarrão
> 
> Exemplo 3:
> * Gato
> * Cachorro
> * Passarinho
> 

Pode-se usar sub-níveis usando TABs:  

> Exemplo :
> * Carro
>   - Esportivo
>   - Utilitário
> * Moto
>   + Esportiva
>   + Sport-turing
> - Caminhão  
>   - Pequeno
>   + Médio
>   * Grande
>       - Feio
>       - Bonito
> + Bicicleta
>

- ## LISTAS ORDENADAS ##  

Exemplo 1:
1. Um  
2. Dois  
3. Três    

Exemplo 2:
1. Um
1. Dois
1. Três

Exemplo 3:

5.   
5.   
5.   

Exemplo 4 - forçando a criação de uma sequência numérica específica:   

98\.  
99\.    
94\.   

-----------------------------------
-----------------------------------
-----------------------------------
  
# LINKS

- ## Link 1 ##

```text
[CLIQUE AQUI](https://www.google.com)
```

> [CLIQUE AQUI](https://www.google.com)

- ## Link 2: com texto alternativo ##

```text
[Show Me the Code](https://showmethecode.com.br "Blog")
```

> [Show Me the Code](https://showmethecode.com.br "Blog")

- ## Link 3: usando variável ##

```text
[Clique Aqui][site-URL]

[site-URL]:https://showmethecode.com.br
```
> [Clique Aqui][site-URL]
> 
> [site-URL]:https://showmethecode.com.br

- ## Outros exemplos ##
```text
I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].  
[desafio 1] [4].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"
  [4]: https://raw.githubusercontent.com/carlosevandro/bloco-de-anotacoes/master/aulas/aula_001/desafio1_aula001.PNG "IMAGEM DO DESAFIO 1"
```
> I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].  
> [desafio 1][4].
> 
>   [1]: http://google.com/        "Google"
>   [2]: http://search.yahoo.com/  "Yahoo Search"
>   [3]: http://search.msn.com/    "MSN Search"
>   [4]: 
> https://raw.githubusercontent.com/carlosevandro/bloco-de-anotacoes/master/aulas/aula_001/desafio1_aula001.PNG "IMAGEM DO DESAFIO 1"
> 

- ##  Criação de links “automáticos” para URLs e endereços de email
```text
<http://example.com/>  
```

> <http://example.com/>  
>

```text
<email@host.com>
```
><email@host.com>
>

---
---
---
  
# IMAGENS

- ## Imagem 1 ##
```text
![Alt text](desafio1_aula001.PNG)
```

> ![Alt text](desafio1_aula001.PNG)

- ## Imagem 2 ##
```text
![Alt text](desafio1_aula001.PNG "Imagem do desafio 1")
```
> ![Alt text](desafio1_aula001.PNG "Imagem do desafio 1")

## Imagem 3 ##

```text
![Markdown][image]
[image]: images/photo.png
```

> ![Markdown][image]  
>
> [image]: images/photo.png  

---
---
---
# IMAGEM COM LINK #

- ## Imagem com link 1 ##

```text
[![Markdown](images/photo.png)](https://showmethecode.com.br)
```

> [![Markdown](images/photo.png)](https://showmethecode.com.br)

- ## Imagem com link 2: com variável ##

```text
[![Markdown][image-thumbs]][image-url]

[image-thumbs]:images/photo.png
[image-url]:https://showmethecode.com.br
```

> [![Markdown][image-thumbs]][image-url]
> 
> [image-thumbs]:images/photo.png
> [image-url]:https://showmethecode.com.br  

-------------------------------------------------------------------------------------  
-------------------------------------------------------------------------------------  
-------------------------------------------------------------------------------------  

# CÓDIGOS #

- ## Exemplo em linha ##
```text
Informe os parâmetros `username` e `password` para a função `login()`.
```

> Informe os parâmetros `username` e `password` para a função `login()`.


- ## Exemplo em linha com crase dentro do código ##

```text
``const message = `My name is ${name}`. ``
```

> ``const message = `My name is ${name}`. ``

</br></br>
- ## Exemplo em bloco de código 1: 4 espaços na frente do código. ##
</br>

```text
    //login.js
    const username = 'robertoachar';
    const password = 'secret';

    login(username, password);
```
>     //login.js
>     const username = 'robertoachar';
>     const password = 'secret';
> 
>     login(username, password);

**NOTA:** os 4 espaços podem ser substituídos por um TAB. O melhor mesmo é usar a abordagem a seguir.

</br></br>
- ## Exemplo em bloco de código 2: com três crases no começo e no fim ## 
</br>     

    ```
    //login.js

    const username = 'robertoachar';
    const password = 'secret';

    login(username, password);
    ```

> ```
> //login.js
> 
> const username = 'robertoachar';
> const password = 'secret';
> 
> login(username, password);
> ```
</br></br>

-------------------------------------------------------------------------------------  
-------------------------------------------------------------------------------------  
-------------------------------------------------------------------------------------  

# MARKDOWN (APENAS) NO GITHUB.    #
## GitHub Flavored Markdown (GFM) ##
</br>

- ## SYNTAX HIGHLIGHTING ##
>    
>     ```javascript  
>     function fancyAlert(arg) {  
>       if(arg) {  
>         $.facebox({div:'#foo'})  
>       }  
>     }  
>     ```
>
> Resultado:  
>   ```javascript
> function fancyAlert(arg) {
>     if(arg) {
>       $.facebox({div:'#foo'})  
>     }  
> }
> ```  
> Algumas opções de linguagens para syntax highlighting:
> 
> - **javascript** (ou  apenas digite **js**): linguagem JavaScript
> - **text**: apenas texto puro, sem formatação
> - **pyhton**: linguagem python
> - **bash**: linguagem bash
> -

- ## LISTAS DE TAREFAS ##
> ```text
> - [X] TEXTO 1  
> - [ ] TEXTO 2  
> - [ ] TEXTO 3  
> - [ ] TEXTO 4  
> - [ ] TEXTO 5  
> ```
> 
> Resultado:
>
> - [X] TEXTO 1  
> - [ ] TEXTO 2  
> - [ ] TEXTO 3  
> - [ ] TEXTO 4  
> - [ ] TEXTO 5  

- ## TABELAS ##



| Tablesssssssss  | Are zxxxxxxx | Coolllllllllllll |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

</br></br>

| Nome | Idade | Profissão |
| - | - | - |
|Roberto | 36 |

</br></br>

| Nome | Idade  | Profissão |  
| ---- | ------ | --------- |  
| Roberto | 36  | Desenvolvedor |  
| Rodrigo | 35  | Professor |
| Renan | 33 | Músico  |




- ## USANDO EMOJI ##

> :smile:
> 
> :simple_smile:
> 
> :joy:
> 
> :shit:  
> :hankey:  
> :poop:  
> 
> :+1:  
> :thumbsup:



- ## TACHADO (_STRIKETHROUGH_) ##

- ## AUTOMATIC LINKING FOR URLs

- ## USERNAME @mentions ##

- ## SHA REFERENCES ##

- ## ISSUE REFERENCES WITHIN A REPOSITORY ##


# EXEMPLO DE ESTRUTURA DE REPRESENTAÇÃO DE ESTRTUTRA DE ARQUIVOS #

## Project files

```text
.
|--- src
|    |--- index.js
|--- test
|    |--- test.js
|--- .editorconfig
|--- .eslintignore
|--- .eslintrc.json
|--- .gitattributes
|--- .gitignore
|--- .npmrc
|--- .prettierrc
|--- .travis.yml
|--- appveyor.yml
|--- CHANGELOG.md
|--- circle.yml
|--- LICENSE
|--- package.json
|--- README.md
```