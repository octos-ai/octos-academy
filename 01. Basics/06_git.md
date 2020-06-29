# Git e GitHub

O Git é um sistema de controle de versão de arquivos. Provavelmente o mais utilizado. Aqui vamos aprender apenas os comandos básicos, os mais utilizados. O Git é muito completo e tem muito mais ferramentas do que veremos neste tutorial. O site oficial do [Git](https://git-scm.com/) traz a documentação completa e muito mais informações. Mas, para ser sincero, a maior fonte de conhecimento sobre Git vem do StackOverflow e do Google em geral.

Agora, O GitHub é um site onde as pessoas guardam cópias remotas do seus repositórios que são controlados pelo Git localmente. No GitHub as pessoas podem ver seus arquivos, histórico de modificações e muitos mais. Bem, essa é uma das funções do GitHub, que hoje em dia serve para muito mais coisa. Por exemplo, é possível trabalhar em equipe usando o GitHub e gerenciando as modificações dos arquivos do time usando o sistema de _Pull Requests_ (vamos ver depois como funciona!). O GitHub não é o único a oferecer esses serviços, outros sites semelhantes são: GitLab e BitBucket, por exemplo.

## Criando seu primeiro repositório local e remotamente

Existem muitas formas de iniciar um repositório local e remotamente (no GitHub). Vamos explorar talvez a mais comum delas. Vamos iniciar um repositório no GitHub e cloná-lo localmente.

Vá até o site do GitHub, faça o login (ou crie sua conta e faça o login). No canto superior direito você pode clicar no **+** e verá:

<img src=".\imgs\git\git.png" style="zoom:67%;" />

Depois disso você verá:

<img src=".\imgs\git\git_02.png" style="zoom:67%;" />

O nome do meu repositório é **teste**. Ao lado aparece o meu username, mesquita. Eu coloquei uma descrição, coloquei o repositório como Privado (só eu e quem eu liberar poderá ver este repositório e o que tem dentro dele). Escolhi inicializar com um README, escolhi um .gitignore do Python e a licença MIT License. Veremos cada coisa em detalhe mais pra frente. Aperte _Create repository_

<img src=".\imgs\git\git_03.png" style="zoom:67%;" />

e **parabéns**, você criou o seu repositório!

Veja que o que tem dentro do arquivo README.md é exatamente o que está aparecendo no final da tela, "teste" e "Este repositório é um teste". Você pode alterar este arquivo para informar quem for usar o seu repositório sobre o que ele se trata de uma forma explicativa.

Ok. Mas, este repositório está apenas no GitHub, como fazer para "baixarmos" ele para o nosso computador? (Ou: clonarmos localmente, mesma coisa).

Podemos fazer isso da seguinte maneira, podemos clicar no botão verde **Clone or download** e copiarmos o link:

<img src=".\imgs\git\git_04.png" style="zoom:67%;" />

Use o comando

`$ git clone LINK`

no terminal do Ubuntu e você terá algo como:

<img src=".\imgs\git\git_06.png" style="zoom:67%;" />

Perceba que a pasta **teste** foi criada.

Ao entrar na pasta **teste** você verá o seguinte:

<img src=".\imgs\git\git_07.png" style="zoom:67%;" />

Perceba que agora aparece **on git:master**. Isso quer nos dizer que estamos numa pasta onde o git está ativado e estamos na branch chamada **master** (vamos ver o que é um branch mais pra frente). Também já temos os arquivos LICENSE e README.md que estavam aparecendo no GitHub. Mas, cadê o arquivo gitignore? Veja que ele tem um ponto no começo do nome, então ele está oculto.

### Comandos básicos do Git

Vamos fazer uma abordagem bem prática aqui. Quais comandos mais usamos no dia a dia. Vamos fazer o seguinte: criaremos um arquivo de texto e controlaremos suas modificações com o Git.

<img src=".\imgs\git\git_08.png" style="zoom:67%;" />

Pronto, criei um arquivo chamado **arquivo.txt** e ele já está na minha pasta /teste.

Agora, se eu executar o comando:

`$ git status`

ou

`$ gst`

(Neste caso o `$ gst` funciona porque justamente estamos usando o Zsh e instalamos o plugin do Git. https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git aqui você pode ver todos os outros atalhos)

Você verá o seguinte após executar o comando:

<img src=".\imgs\git\git_09.png" style="zoom:67%;" />

Pois bem, isso nos informa que o nosso **arquivo.txt** não está sendo "trackeado" pelo Git, ou seja, o Git não está obsevando as modificações que estão acontecendo neste arquivo.

Vamos então adicionar este arquivo ao git:

`$ git add arquivo.tx`

<img src=".\imgs\git\git_10.png" style="zoom:67%;" />

(Veja que eu usei os atalhos do Zsh, você também pode usar!)

Após adicionar o arquivo, dei `git status` novamente e vi que git me diz que tenho mudanças não commitadas. O que é um commit? O comando commit irá registrar a situação atual do arquivo no momento que você executar o comando, é como se ele tirasse um foto do interior do seu arquivo no momento que você commitar o arquivo. Para ajudar a identificar qual momento você criou a "fotografia" (o commit) do arquivo, esta função guarda outras informações. É guardado a hora, quem fez a modificação no arquivo, é dado um identificador único para o commit e você irá digitar uma mensagem única para este commit.

Vamos ver então como funciona. Entramos com o comando:

`$ git commit -m "Adiciona arquivo.txt"`

Ao entrar com este comando, todos os arquivos que estão verdinhos depois de "Changes to be committed" vão entrar no mesmo commit. o **-m** nos dá opção de inserir uma mensagem curta sobre este commit, neste caso "Adiciona arquivo.txt".

<img src=".\imgs\git\git_11.png" style="zoom:67%;" />

Algumas observações:

- Veja que foi pedido para preencher a sua identidade. Eu costumo preencher com o email e usuário do GitHub.
- Cada grupo/empresa/time/local tem seu próprio jeito de escrever as mensagens do commit. Veja com seu time qual o padrão utilizado.
- Quando você faz um `git add` num arquivo, ele vai para o que é chamado de **staging area**. Os arquivos nesta área estão 'prontos' para serem commitados, é o que aparece verdinho.

Após preencher os dados e fazer o commit novamente, deu certo e apareceu algo do tipo:

<img src=".\imgs\git\git_12.png" style="zoom:67%;" />

Veja que ao dar `git status` novamente ele diz que eu estou 1 commit a frente de "origin/master". O que isso significa?

Origin é o nome dado ao servidor remoto (neste caso o GitHub), se executarmos o comando:

`$ git remote --verbose`

Nós veremos:

<img src=".\imgs\git\git_13.png" style="zoom:67%;" />

Então toda vez que falarmos de "origin", você tem que saber que estamos nos referindo ao local remoto, no nosso caso o GitHub! Perceba que podemos ter vários servidores remotos, um mesmo repositório local pode estar conectado ao GitHub e ao GitLab ao mesmo tempo. Neste caso teríamos, por exemplo, um **origin-lab https://gitlab.com/mesquita/teste.git ** ou algo semelhante!

Bem, mas vamos continuar. Nós criamos um arquivo e agora o git está de olho nele. Vamos alterá-lo!

<img src=".\imgs\git\git_14.png" style="zoom:67%;" />

Veja, eu alterei o arquivo colocando "teste" como conteúdo dele.

Ao darmos `git status` novamente veremos o seguinte:

<img src=".\imgs\git\git_15.png" style="zoom:67%;" />

O Git realmente está de olho nele, viu que nosso arquivo foi modificado. Para commitar a mudança que fizemos precisamos adicioná-lo com o `git add` e depois registramos o commit com `git commit`.

Mas... o que foi mudado?

Se fizermos `$ git diff arquivo.txt` podemos ver:

<img src=".\imgs\git\git_16.png" style="zoom:67%;" />

(Aperte **q** para sair do diff)

Bem, a mudança foi muito simples, a linha com "Conteúdo do arquivo" foi deletada (em vermelho) e "teste" (em verde) foi colocado no lugar!

Ok, mudança exatamente isso. Então vamos commitar.

![]()<img src=".\imgs\git\git_17.png" alt="git_17" style="zoom:67%;" />

Veja que agora estamos 2 commits na frente de origin/master.

Agora, uma pergunta. Depois dessas duas mudanças, como eu faço para ver meu histórico de mudanças? A resposta é o comando

`$ git log`

<img src=".\imgs\git\git_18.png" style="zoom:67%;" />

Veja que as mudanças mais velhas ficam na parte de baixo e as mais novas na parte de cima. Este "Initial commit" foi criado na hora que criamos o repositório no GitHub!

O comando `git log` é muito mais completo, vale a pena explorar outras opções de visualização do histórico de mudança que ele nos dá.

Okay, agora eu quero atualizar o GitHub com as mudanças que eu fiz localmente, como eu faço? Assim:

`$ git push origin master`

Neste comando `git push` você está enviando as informações da branch **master** para **origin** (GitHub). O terminal vai pedir seu login e senha.

Se der certo, no GitHub você verá:

<img src=".\imgs\git\git_19.png" style="zoom:67%;" />

Veja quem está lá agora, o **arquivo.txt**!

Agora que nossa branch **master** local está atualizada com a remota, você pode inclusive ver o histórico de alterações no próprio GitHub.

<img src=".\imgs\git\git_20.png" style="zoom:67%;" />

Ao clicar em commits você verá exatamente os mesmos commits que vimos anteriormente com `git log`. Você também pode entrar em cada commit e ver o que exatamente foi mudado. Claro que você também consegue ver o que foi mudado de commit pra commit pelo terminal, localmente. Fica então esse exercício ao leitor (Google & StackOverflow!).

Próxima situação: não quero mais o **arquivo.txt**, não preciso mais dele, vou deletar.

<img src=".\imgs\git\git_21.png" style="zoom:67%;" />

Ao deletar com

`$ rm arquivo.txt`

o git nos informa que ele foi deletado. Para informar ao git que ele deve parar de seguir as mudanças do **arquivo.txt** nós fazemos:

`$ git rm arquivo.txt`

E então commitamos a mudança.

<img src=".\imgs\git\git_22.png" style="zoom:67%;" />

Pronto. Podemos atualizar o GitHub:

`$ git push origin master`

Tá, pediu meu usuário e senha novamente! Chato isso né? Não tem um jeito de não ficar pedindo constamente? Tem!

Rode:

`$ git config --global credential.helper store`

depois execute novamente o `$ git push origin master`, será a última vez que ele vai pedir username e password. Da próxima vez já estará salvo!

Agora com o GitHub atualizado, você verá que temos um commit a mais na contagem e o arquivo deletado realmente desapareceu. Sucesso!!

Próxima situação bem comum: um arquivo foi alterado no GitHub (por você ou por outra pessoa) e você tem que atualizar esta atualização localmente. Como proceder para manter local e remoto atualizados neste caso?

A alteração que eu vou fazer neste caso será mudar o README.md pelo próprio GitHub (dê uma olhada para descobrir como alterar um arquivo pelo próprio GitHub, não é difícil!)

<img src=".\imgs\git\git_23.png" style="zoom:67%;" />

Pronto, alterei. Veja que agora temos 5 commits e veja que o README mudou.

Mas essas alterações não estão no meu repositório local. Se eu der uma olhada no que está em README.md verei: "Este repositório é um teste." apenas!

Para atualizar vamos fazer o seguinte:

`$ git pull origin master`

<img src=".\imgs\git\git_24.png" style="zoom:67%;" />

Pronto, fizemos o **pull** e atualizamos localmente.

Esta não é a única forma de atualizar seu repositório localmente, pesquise qual é a diferença entre "git fetch + git merge vs git pull" para se informar mais.

### Branches

Por enquanto, tudo o que fizemos foi na mesma branch, a **master**, que é a branch criada por padrão no Git. Uma branch serve para você fazer alterações no código sem se preocupar em "estragar" o código que está funcionando. Vamos imaginar o seguinte: o código principal do seu time está na branch **master**, mas você precisa acrescentar uma função em um programa e não quer estragar o código que está na **master**. O que você deve fazer então é criar uma branch a partir da **master**, por exemplo chamada **implementa_funcao** e fazer o desenvolvimento da sua função nesta branch. Quando você terminar e tiver certeza que está funcionando, você abrirá um _Pull Request_ (PR) para a branch **master**, que é uma função existente no GitHub para que outras pessoas avaliem se seu código pode ser unido/mesclado (merged) com o da branch **master**. Muita coisa? Vamos aos poucos.

Como criamos uma branch?

`$ git branch implementa_funcao`

ou

`$ git checkout -b implementa_funcao`

A primeira simplesmente cria a branch implementa_funcao, a segunda cria e muda da branch atual (master) para a branch criada automaticamente (implementa_funcao).

Se você usou a primeira opção, para mudar de branch você pode fazer: `$ git checkout implementa_funcao`.

Perceba que o zsh nos informa que a branch que estamos é a implementa_funcao quando mudamos.

Agora vamos criar um arquivo, adicioná-lo ao git e fazer um commit:

<img src=".\imgs\git\git_25.png" style="zoom:67%;" />

Veja com `ls` que temos o arquivo **teste.txt** criado.

Agora perceba o seguinte: ao mudarmos para a master novamente com `$ git checkout master`

<img src=".\imgs\git\git_26.png" style="zoom:67%;" />

Não temos o arquivo **teste.txt** na master! As alterações que fizemos na branch implementa_funcao ficam apenas nessa branch, até que façamos o merge com a master (vamos ver isso depois!).

Beleza. Criei minha branch auxiliar implementa_funcao, terminei de implementar as alterações que eu tinha que fazer. O que eu faço agora?

Bem, se estamos trabalhando num time, temos que abrir um Pull Request para fazer o merge com o código principal. Primeiro vamos jogar nossa branch para o GitHub:

`$ git push origin implementa_funcao`

(Veja que ele não pediu username e senha! Se pediu você terá que rever o passo de salvar a senha feito anteriormente!)

Veja o GitHub:

<img src=".\imgs\git\git_27.png" style="zoom:67%;" />

Agora ele nos diz uma branch nova foi criada e nos dá a opção de "Compare & pull request", vamos fazer isso:

<img src=".\imgs\git\git_28.png" style="zoom:67%;" />

No começo da página devemos colocar um título para o PR, assim como uma descrição e outras informações adicionais (quem vai revisar o PR em (Reviewers), etc). Ao rolar a página você consegue ver quais arquivos estão sendo adicionados/modificados e o que está sendo adicionado/modificado.

OBS: Perceba que estamos fazendo o PR para a branch **master** neste caso, alguns projetos não permitem que você faça um PR diretamente para a branch master e sim para uma branch auxiliar como a **dev**, por exemplo. Procure se informar das regras para PR. Outras regras envolvem estilo de título de PR e comentários a serem feitos.

Ao criar o PR você verá:

<img src=".\imgs\git\git_30.png" style="zoom:67%;" />

E então os membros do seu time farão comentários e pedirão alterações para que você faça no seu código. Você pode alterar localmente e enviar as alterações com um `git push` , o que você enviar de alteração com o comando aparecerá no PR.

---

Neste caso é apenas um exemplo, este repositório é apenas seu. Você não precisaria fazer um PR. Você poderia fazer o merge das branches localmente.

Fazendo o seguinte: mude para a **master** com `$ git checkout master` e execute o `$ git merge implementa_funcao` você verá que agora o **teste.txt** está na master.

Você pode enviar as alterações para o remoto com `$ git push origin master` e **teste.txt** estará no GitHub!

---

Você terminou de trabalhar com a branch implementa_funcao e o código já está na branch master. Então vale a pena apagar a implementa_funcao! Como?

`$ git branch -d implementa_funcao`

Caso você tenha "desistido" de uma branch e o código que foi alterado lá não tenha sido feito merge a nenhuma branch, você pode se livrar dessa branch também, usando a flag **-D** no lugar do **-d** para forçar que ela seja deletada.

Tudo bem, eu deletei a branch localmente, mas você lembra que a gente enviou ela pro GitHub? Como deletá-la no GitHub também?

Pelo próprio GitHub você pode ir em:

<img src=".\imgs\git\git_31.png" style="zoom:67%;" />

e apertar:

<img src=".\imgs\git\git_32.png" style="zoom:67%;" />

Tá bom, não deu certo por aí né? Ele disse que tem um PR aberto usando essa branch! Justo, a gente realmente abriu um PR usando essa branch!! Primeiro vá em Pull Requests, role até o final da página e aperte "Close pull request". Agora você pode voltar em branches e deletar a implementa_funcao.

Localmente podemos fazer o seguinte:

`$ git push origin --delete implementa_funcao`

Pronto!

<img src=".\imgs\git\git_33.png" style="zoom:67%;" />

Das duas formas você verá apenas a master como branch. Tanto remotamente como na imagem anterior ou locamente com `$ git branch`.

---

Este é o fim do guia básico de Git. Existem muitos outros comandos úteis, por exemplo o `git stash`. Dê uma pesquisada!
