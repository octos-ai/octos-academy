# Guia básico sobre Terminal

Agora vamos aprender um pouco sobre o terminal ou:

## Terminal, Shell, Console, Prompt...

Sim, o terminal pode ter vários nomes, por exemplo o zsh que acabamos de instalar se chama Z Shell. Tenha em mente que estamos falando quase sempre da exata mesma coisa. Isto é:

<img src=".\imgs\terminal\terminal.png" style="zoom:67%;" />

## Primeiros comandos

O primeiro comando é muito importante para termos a noção de localização dentro do nosso sistema.

`$ pwd`

Ao digitar este comando você verá algo semelhante a:

<img src=".\imgs\terminal\terminal_02.png" style="zoom: 67%;" />

O que isso significa? O comando `pwd` significa "**p**rint **w**orking **d**irectory", em uma tradução (bem) livre seria algo como "mostre na tela a pasta em que estou atualmente". Geralmente no linux o termo diretório é usado no lugar de pasta, e o "working" dá a ideia do diretório atual em que estamos.

Tudo bem, então já sei que estou (no meu caso) no diretório /home/vinicius.

Outro comando importante para nos localizarmos é o:

`$ ls`

O `ls` significa **l**i**s**t, ou listar. No meu caso, quando eu digito listar o que eu encontro é o seguinte:

<img src=".\imgs\terminal\terminal_03.png" style="zoom:67%;" />

Nada foi impresso na tela, o que aconteceu?

Isso significa que eu não tenho nenhuma pasta visível nesse diretório (/home/vinicius)!

Talvez eu tenha um diretório ou arquivo oculto na pasta, como eu faço para ver isso?

O comando `ls`, assim como a maioria dos comandos do terminal, tem uma help que mostra como usar o comando. Se você digite `$ ls --help` verá o seguinte:

<img src=".\imgs\terminal\terminal_04.png" style="zoom:67%;" />

O que queremos é justamente ver os arquivos que começam com **.** (ponto), que é a primeira opção. Então temos que usar `$ ls -a` ou `$ ls --all` para vermos estes arquivos. Neste caso **-a** ou **--all** são chamados de **_flags_**. Eles "acenam" para o `ls` que você usuário está querendo uma opção a mais do que um simples `ls` sozinho.

Agora você pode estar se perguntando, qual a diferença entre `$ ls -a` e `$ ls --all`? Nenhuma, eles vão mostrar o mesmo resultado. Veja:

<img src=".\imgs\terminal\terminal_05.png" style="zoom:67%;" />

Então por que existem os dois??

Quando você usa apenas um hífen, por exemplo `$ ls -a` o que vem depois do "hífen simples" é uma flag de apenas uma letra. E é possível fazer algo muito interessante: combinar flags de uma letra! No caso do `ls`podemos fazer o seguinte:

`$ ls -al`

Tente este comando e perceba que o output mudou. Agora volte no help do `ls` e veja o que a flag **l** mandou o comando fazer.

Quando você usa "hífen duplo", ou seja `ls --all` é uma maneira do sistema saber que você não está juntando múltiplas flags de 1 caracter (ou seja, querendo dizer `ls -a -l -l`), e sim usando uma flag única de três caracteres.

Agora que nós vimos que não temos nenhum arquivo ou diretório visível mas temos alguns arquivos e diretórios ocultos, que tal criamos um diretório? Para criar um diretório vamos usar o comando`mkdir`.

Sim, você já deve estar imaginando que `mkdir` significa **m**a**k**e **dir**ectory. Exatamente!

Agora vamos criar o seguinte diretório:

`$ mkdir tmp`

Agora se você der `$ ls`, se tudo ocorreu como esperado você deve ver o nosso novo diretório **tmp**.

Ok, criamos um diretório, mas como entrar nele? Para isso vamos usar o comando `cd` (**c**hange **d**irectory). Pode digitar:

`$ cd tmp`

e então apertar Enter. Ou então podemos dizer apenas `$ cd` e apertar **Tab** que o nosso amigo zsh irá completar com **tmp**. Veja, ele completa diretamente com **tmp** porque é o único diretório nesta pasta atual, caso tivéssemos mais diretórios dentro deste atual o Zsh nos daria uma lista de opção para caminharmos por ela (veremos isso em outros exemplos).

<img src=".\imgs\terminal\terminal_06.png" style="zoom:67%;" />

Usando um pouco do que a gente viu anteriormente, vemos que o nosso tema do Zsh nos mostra em que pasta estamos agora. Vemos também que ao dar `ls` ele mostra que o diretório não tem nada dentro (acabamos de criá-lo!). Vemos com `pwd` que estamos em /home/vinicius/tmp. Ótimo.

## Criando diretórios e nevagando por eles

Nós criamos a pasta **tmp** com o comando `$ mkdir tmp`, neste caso o **tmp** é chamado de parâmetro ou argumento da função `mkdir`. Você pode ver quais argumentos a função `mkdir` necessita em `$ mkdir --help`. Caso você tente usar `$ mkdir` sem nenhum argumento, a função te dará um erro e mandará você olhar o help.

No caso da função `mkdir` ela aceita diversos argumentos ao mesmo tmepo, ou seja, podemos criar diversas pastas ao mesmo tempo. Por exemplo:

`$ mkdir dir1 dir2 dir3`

Se você der um `ls` verá:

<img src=".\imgs\terminal\terminal_07.png" style="zoom:67%;" />

Perceba que dir1, dir2 e dir3 foram criados no mesmo nível. Caso o que você queira criar sub diretórios um dentro do outro, podemos fazer o seguinte, com a flag **-p**:

`$ mkdir -p dir4/dir5/dir6`

<img src=".\imgs\terminal\terminal_08.png" style="zoom:67%;" />

Vá ao help de `mkdir`e veja o que **-p** significa.

Perceba que no nível de **tmp** só foi criado o **dir4**. Então eu posso caminhar pelos diretórios como na imagem seguinte:

<img src=".\imgs\terminal\terminal_09.png" style="zoom:67%;" />

Perceba que o Zsh me diz no final que estou em **dir6**.

Agora eu posso voltar ao diretório anterior também usando `cd`. Existem muitas formas.

Posso utilizar `$ cd ../../..`, ou seja, voltar 3 níveis de uma vez.

Posso fazer `$ cd ..`, depois `$ cd ..`, depois `$ cd ..`, ou seja, subir 1 nível de cada vez.

Essas formas são por meio de paths relativos, ou seja, você não precisa explicitar exatamente o nome do caminho, você apenas está dizendo que quer voltar um nível (ou três). Mas também podemos usar um path direto, ao fazermos: `$ cd ~/tmp` da onde estivermos vamos voltar para a pasta **tmp**.

## Criando arquivos e os manipulando

Podemos usar um editor de texto como o **vim** diretamente pelo terminal para criarmos arquivos. Mas neste tutorial vamos criar arquivos de texto de maneira mais simples. Vamos utilizar o comando `echo`. Se você fizer:

`$ echo "Testando 1, 2, 3"`

você verá que ele imprimiu na tela o que você escreveu. Mas podemos fazer o seguinte:

`$ echo "Testando 1, 2, 3" > teste_1.txt`

Com o **>** (maior que) você está dizendo para o comando `echo` salvar o que está entre aspas em **teste_1.txt**.

Nada foi impresso na tela, se eu usar o comando `ls` eu vejo que o **teste_1.txt** foi criado... Mas como eu vejo o que tem dentro dele? Existem algumas opções para isso, mas vamos começar com o comando `cat`:

`$ cat teste_1.txt`

<img src=".\imgs\terminal\terminal_10.png" style="zoom:67%;" />

Funcionou né? Criamos o **teste_1.txt** e conseguimos visualizá-lo.

O comando `cat`não é apenas um visualizador de arquivos. Tente criar outros arquivos com `echo` e passá-los juntos como argumentos do `cat`. Por exemplo `$ cat teste_1.txt teste2.txt teste_3.txt` e veja o que acontece. Para mais informações veja o help do `cat`.

Outros comandos para você procurar: `less`e `more`.

## Movendo, renomeando e copiando arquivos

Caso eu queira mudar o meu arquivo **teste_1.txt** de lugar, como eu faço? Digamos que eu queria colocá-lo em **dir4**. Basta eu usar o comando `mv`.

Veja:

<img src=".\imgs\terminal\terminal_11.png" style="zoom:67%;" />

Perceba que eu tive que mudar meu diretório com `cd` e depois fazer um `ls` para ver se **teste_1.txt** realmente estava lá. Então eu tenho que voltar com `cd ..` para o nível superior. Não tem uma maneira mais direta de fazer isso? Tem! Eu poderia simplesmente ter feito `$ ls dir4`. Veja:

<img src=".\imgs\terminal\terminal_12.png" style="zoom:67%;" />

Eu consegui ver que o meu arquivo estava em **dir4** com muito menos trabalho. Excelente.

Agora eu quero copiar o meu **teste_1.txt**, como eu faço? Podemos usar o comando `cp`. Veja:

<img src=".\imgs\terminal\terminal_13.png" style="zoom:67%;" />

Perceba que eu escrevi

`$ cp teste_1.txt mu_arquivo.txt`

foi um erro, eu queria ter escrito **meu_arquivo.txt**! Como eu faço então para renomear o arquivo e consertar o meu erro? A maneira tradicional de se renomear o arquivo é usando o `mv` e movendo o arquivo para o mesmo diretório só que com outro nome. Vamos fazer isso então:

`$ mv mu_arquivo.txt meu_arquivo.txt`

<img src=".\imgs\terminal\terminal_14.png" style="zoom:67%;" />

Veja bem, não temos mais o arquivo antigo escrito de forma errada, apenas o arquivo final. Sucesso!

## Apagando arquivos e diretórios

Apagar um arquivo ou diretório é algo muito comum. O comando para isso no linux é `rm`. Vamos ver como ele funciona.

Um pouco de contexto, eu estou em **dir4** e vou criar um arquivo chamado **outro.txt** para ilustrar esta parte. Ficaremos assim então:

<img src=".\imgs\terminal\terminal_15.png" style="zoom:67%;" />

Então primeiramente eu vou removar o **outro.txt** que eu acabei de criar, para isso podemos fazer:

`$ rm outro.txt`

Simples, certo? Com `ls`você pode ver que ele foi apagado!

Mas o `rm` também aceita mais de um argumento. Podemos fazer:

`$ rm meu_arquivo.txt teste_1.txt`

e os dois arquivos vão ser apagados ao mesmo tempo!

Se você der `ls` agora verá que sobrou apenas o diretório **dir5**. Vamos apagá-lo então!

`$ rm dir5`

Funcionou?? Não, não funcionou. O `rm` está nos dizendo que **dir5** é um diretório e ele não consegue remover. O que fazer então? O jeito mais usual é fazer o seguinte:

`$ rm -r dir5`

Procure no help do `rm` o que **-r** quer dizer!

Agora sua pasta **dir4** deve estar vazia vazia... Se você der um `ls`o comando vai te retornar absolutamente nada. Vamos voltar então para **tmp**, com por exemplo `$ cd ..`. Então podemos dar um `ls` e vemos os nossos diretórios **dir1** ... **dir4**, certo? Agora eu quero deletar todos eles!

Existem algumas maneiras de fazer isso, você pode fazer

`$ rm -r dir1 dir2 dir3 dir4`

ou uma maneira mais esperta

`$ rm -r dir*`

O que significa o asterísco? Significa que todos os arquivos ou diretórios que o início do nome é **dir** vai ser apagado.

Vamos ver isso em ação mais uma vez.

<img src=".\imgs\terminal\terminal_16.png" style="zoom:67%;" />

Veja que eu criei dois diretórios **tabelas_excel** e **tabelas_csv** assim como um arquivos **tabela_exemplo.xls**. Ao mandar apagar `$ rm -r tabe*` tudo foi apagado! Perceba que este comando é bem "poderoso", então use com sabedoria e veja o que você está fazendo.

OBS: O Google e StackOverflow deverão ser consultados em caso de dúvidas.

## Instalando programas

Para instalar programas pelo terminal nós vamos utilizar o comando `apt-get`.

Vamos começar com um exemplo:

`$ apt-get install tree`

Muito provável que o terminal tenha reclamado e perguntado se você é **root**. Podemos traduzir isso da seguinte maneira: está perguntando se você tem permissões de administador, ou super usuário. O administador tem poderes de modificar e deletar arquivos (exemplo) em qualquer lugar do sistema. Para instalar o programa neste caso precisamos ser um super usuário, para isso vamos colocar o comando `sudo` na frente do `apt-get`. Desta maneira:

`$ sudo apt-get install tree`

O sistema vai pedir sua senha de usuário e você então poderá instalar o arquivo. Caso você encontre um erro e não consiga instalar o **tree** é muito provável que o seu `apt-get` esteja desatualizado. Neste caso faça: `$ sudo apt-get update` e aperte Enter. Depois de completado tente novamente instalar o **tree**.

Sucesso? Vamos ver se funcionou:

<img src=".\imgs\terminal\terminal_17.png" style="zoom:67%;" />

Funcionou se o programa rodou sem erro, ótimo. Mas... sem graça né? Vamos criar umas pastas e ver como fica o ouput do tree. Vejamos:

<img src=".\imgs\terminal\terminal_18.png" style="zoom:67%;" />

Ah, bem melhor. Bacana. Ele mostra a _árvore_ de pastas e arquivos. Veja mais um exemplo depois de eu ter criado mais arquivos:

<img src=".\imgs\terminal\terminal_19.png" style="zoom:67%;" />

Por fim, vamos apagar tudo!

`cd ..` voltamos para /home/vinicius e `rm -r tmp` deletar tudo recursivamente.

<img src=".\imgs\terminal\terminal_20.png" style="zoom:67%;" />

Fim!
