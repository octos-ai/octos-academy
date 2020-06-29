# Oh My Zsh (Ou como melhorar sua vida mil vezes ao usar o terminal).

O terminal do Ubuntu pode ser algo assustador para quem nunca se aventurou a usá-lo, mas existem ferramentas que facilitam a nossa vida. Uma dessas ferramentas é o Zsh e o [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh).

Os próprios criadores dizem:

**Oh My Zsh will not make you a 10x developer... but you may feel like one.**

Quando você estiver usando o terminal com Zsh instalado verá que é verdade!

## Instalando o Oh My Zsh

Primeiro precisamos instalar o Zsh (Z shell):

​ https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH

No terminal do Ubuntu, digite:

```shell
sudo apt-get install zsh
```

Ao apertar Enter você verá o seguinte:

<img src=".\imgs\zsh\zsh.png" style="zoom:67%;" />

Entenda o que o terminal nos informou até agora: você pediu para instalar o zsh, ele informou que 2 novos pacotes serão instalados (zsh e zsh-common) e isso vai ocupar 15.2 MB do espaço da minha memória de disco. Ok, entendi. Quero prosseguir.

Para prosseguir você pode digitar **y** ou **Y**.

_Dica: neste caso, como Y está em maísculo no [Y/n] você pode simplesmente apertar **Enter**._

(OBS: Essa situação vai se repetir constantemente quando você usar o terminal, então essa dica é bem útil.)

Ao término da instalação vamos verificar a versão do zsh que instalamos.

Digite no terminal: `$ zsh --version`

(OBS: É muito comum vermos pela internet o símbolo **\$** antes de algum comando, isso geralmente indica que o que vem **depois** do símbolo **\$** é para ser inserido no terminal.)

Se tudo occoreu como previsto na instalação, você verá o seguinte:

<img src=".\imgs\zsh\zsh_02.png" style="zoom:60%;" />

Temos **zsh 5.4.2** como resultado. Ótimo. Instalamos o zsh.

Próximo etapa: tornar o zsh como padrão. Para isso você precisa digitar: `$ chsh -s $(which zsh)` no terminal. (Lembre-se de copiar depois do \$.)

Após o comando, o sistema deve pedir sua senha. Insira a senha e aperte Enter. Se nenhuma mensagem aparecer, tudo está ocorendo como planejado. Feche a janela do terminal e abra novamente.

Ao abrir novamente veremos o seguinte:

<img src=".\imgs\zsh\zsh_03.png" style="zoom:60%;" />

Digite 2 para usar as configurações recomendadas.

E pronto, agora estamos usando o zsh. Agora vamos para o que realmente interessa, o Oh My Zsh. Para instalar o Oh My Zsh, digite o seguinte comando:

```shell
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

e então a instalação irá ocorrer:

#### <img src=".\imgs\zsh\zsh_04.png" style="zoom: 67%;" />

Ao termino da instalação você verá que fica apenas um **~** no começo da linha que você digita seus comandos. Vamos mudar isso.

## Mudando de tema

Uma das coisas mais incríveis do oh my zsh são os temas criados pela comunidade. Agora vamos aprender onde podemos achar esses temas e como ativá-los.

No site https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes você pode muitos exemplos de temas e você pode escolher qual você mais gostar para usar. Pelo GitHub, você encontra também muitos outros temas bem interessantes, com funções e aparências diversas. Vale a pena dar uma olhada.

Aqui nós vamos usar o 'ys', um tema que traz bastante informação quando estamos utilizando o terminal. Vamos ver.

Para mudar o tema, temos que modificar o arquivo de configuração do Zsh especificando o tema que queremos.

Para encontrar o arquivo de configuração, digite: `$ ls -a`

Este comando irá nos listar o que temos no repositório, incluindo arquivos ocultos (no linux arquivos e pastas ocultas começam com "." (ponto) no nome).

<img src=".\imgs\zsh\zsh_05.png" style="zoom:67%;" />

Nós queremos modificar arquivo .zshrc. Vemos que ele está no repositório em que nos encontramos. Então vamos editá-lo usando: `$ vim .zshrc`

_Dica: se você digitar `$ vim .z` e apertar Tab, o zsh irá autocompletar para você, você pode continuar apertando Tab até chegar no arquivo que deseja._

Ao abrir o arquivo veremos o seguinte:

<img src=".\imgs\zsh\zsh_06.png" style="zoom:67%;" />

A linha que queremos alterar é a **ZSH_THEME="robbyrussell"**. Como estamos no VIM (editor de texto que funciona diretamente no terminal), podemos ir até a linha usando as setas e depois temos que digitar a letra **i** para entrar em modo de edição. Irá aparecer -- INSERT -- no canto inferior da tela.

Apague robbyrussell e digite ys. O resultado será: **ZSH_THEME="ys"** .

Aperte **Esc** depois **:** (dois pontos) e depois **x** e aperte Enter. (O que acabamos de fazer foi sair do modo de edição com **Esc** e depois **:** para digitar um comando. O comando foi **x** para salvar e sair.)

Ok, mudamos o tema, mas... nada mudou? Para realmente "ativar" o tema, precisamos digitar:

`$ source .zshrc`

<img src=".\imgs\zsh\zsh_07.png" style="zoom:67%;" />

Boa, agora vemos bem mais informações: nome do usuário e nome do computador (N-20N3PF1X7RKG neste caso), por enquanto. Teremos bem mais informações úteis quando estivermos usando o Git, por exemplo.

## Adicionando Plugins.

Outra coisa muito útil do zsh são os plugings. Os plugings implementam diversas funções interessantes.

Neste repositório:

https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/

temos um grande número de plugins. Vale a pena dar uma olhada. Agora vamos adicionar um bastante útil para nós: Git.

https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git

Este plugin nos providencia diversos atalhos que vão facilitar muito a nossa vida ao usar o git.

Como adicioná-lo é fácil, vamos novamente até o arquivo `.zshrc` com `$ vim .zshrc` e descemos até a linha onde temos **plugins=()**. Talvez já exista **plugins=(git)**, ou seja, o plugin de git já está ativado. Se já estiver assim, ótimo, podemos sair com: **Esc** + **:** + **q**. (O **q** neste caso é de sair, simplesmente.). Caso não tenha, coloque git entre os parênteses, salve e saia (com Esc + : + x).

Vamos explorar mais o esse plugin tem a oferecer na parte sobre Git.
