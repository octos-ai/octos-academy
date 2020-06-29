# Visual Studio Code

Visual Studio Code (VSCode) é um editor de texto muito poderoso, principalmente por conta das inúmeras extensões criadas pela comunidade de usuários.

## Faça o download do VSCode

https://code.visualstudio.com/docs/?dv=win

Siga o guia de instalação padrão do aplicativo. No fim ele vai dar a opção de iniciar o vscode, então você deverá ver a seguinte tela:

<img src=".\imgs\vscode\tela_inicial_vscode.png" style="zoom: 67%;" />

Se você chegou até aqui você instalou o vscode com sucesso.

As extensões do vscode o tornam muito poderoso, iremos utilizar muitas delas para nos ajudar de diversas formas (desde colorir os parênteses e chaves até corrigir nosso código automaticamente!)

## Extensões

As extensões ficam aqui:

<img src=".\imgs\vscode\vs_02.png" style="zoom:67%;" />

Veja que eu já tenho uma instalada, a Remote - WSL. Você deve instalar essa também é, por exemplo, a de Python. Procure por ela e a instale:

<img src=".\imgs\vscode\vs_03.png" style="zoom:67%;" />

Veja que quem a criou foi a Microsoft, é esta que devemos instalar.

Muitas outras extensões são úteis, procure na internet por "Best vscode extensions for python" e verá muitas outras extensões que são indicadas para o desenvolvimento em python!

Por enquanto vamos focar na Remote - WSL.

## Remote - WSL

Se você clicar no ícone acima das extensões verá o seguinte:

<img src=".\imgs\vscode\vs_04.png" style="zoom:67%;" />

Veja que ele já nos mostra nossa distribuição do Ubuntu instalada e o meu nome de usuário do ubuntu! Clique com botão direito e "Open folder in WSL". A seguinte tela aparecerá para você:

<img src=".\imgs\vscode\vs_05.png" style="zoom:67%;" />

Tá, mas eu quero desenvolver dentro da minha pasta **teste** que é aquela que criamos no GitHub e onde estou desenvolvendo meu código!

Se você for em File > Open Folder..., você verá esta janela, digite então o caminho até a nossa pasta Teste e aperte OK

<img src=".\imgs\vscode\vs_06.png" style="zoom:67%;" />

Ok, veremos então:

<img src=".\imgs\vscode\vs_07.png" style="zoom:67%;" />

Ah, bem melhor! Estamos dentro da nossa pasta **teste**!!

Veja no canto inferior esquerdo temos WSL: Ubuntu 18-04 e logo depois **master** escrito, isso indica em que branch o nosso repositório do git está!

Se você clicar em **master** você verá:

<img src=".\imgs\vscode\vs_08.png" style="zoom:67%;" />

viu, podemos criar uma branch nova por aqui. Vamos criar uma branch nova! Eu criei uma branch **adiciona_texto**.

<img src=".\imgs\vscode\vs_09.png" style="zoom:67%;" />

Viu? Já estamos na branch nova. Semelhante a fazer `$ git checkout -b adiciona_texto`.

Posso clicar com botão direito e criar um novo arquivo:

<img src=".\imgs\vscode\vs_10.png" style="zoom:67%;" />

Veja o arquivo que eu criei e seu conteúdo:

<img src=".\imgs\vscode\vs_11.png" style="zoom:67%;" />

Foi um código em python chamado **texto.py**! Veja que temos um menu do lado que apareceu um "1" num círculo azul. Se você clicar nele e clicar no texto.py, verá o seguinte:

<img src=".\imgs\vscode\vs_12.png" style="zoom:67%;" />

Incrível né? É exatamente o Git sendo mostrado pelo vscode!

Você pode fazer o comando `$ git add` ao clicar em:

<img src=".\imgs\vscode\vs_13.png" style="zoom:67%;" />

E ``\$ git commit -m "Adiciona texto.py" ao digitar a mensagem:

<img src=".\imgs\vscode\vs_14.png" style="zoom:67%;" />

Por mim o commit é terminado apertando Ctrl + Enter! Pronto, você fez um commit usando o vscode! Não acredita?

Se você voltar no terminal verá que o zsh já está te dizendo que você está na branch nova **adiciona_texto**, se você der um `ls`ele vai te mostrar o **texto.py** nos arquivos. Um `$ git log` vai te mostrar exatamente seu último commit feito no vscode:

<img src=".\imgs\vscode\vs_15.png" style="zoom:67%;" />

Então funcionou mesmo, certo?

No meu do "source control" você tem acesso a outros commits que a gente viu anteriormente, como `git push`e `git pull`. Dá para fazer tudo pelo vscode!

<img src=".\imgs\vscode\vs_16.png" style="zoom:67%;" />

Dica: existe um extensão do GitHub pro vscode que permite que você abra um PR pelo próprio vscode. Dê uma pesquisada.

## Executando um programa em Python pelo VScode

Queremos saber se o nosso arquivo **texto.py** realmente funciona. Vamos então ver como podemos rodá-lo pelo vscode! Se você abrir o arquivo e apertar F5, verá o seguinte:

<img src=".\imgs\vscode\vs_17.png" style="zoom:67%;" />

Não temos nenhuma opção de python aqui... Estranho né? Porque queremos rodar um código em python, não em node.js... Vá até as extensões e você verá o seguinte:

<img src=".\imgs\vscode\vs_18.png" style="zoom:67%;" />

Pois bem, a gente tinha instalado a extensão Python localmente mas não no WSL! Instale no WSL. Após a instalação o sistema vai pedir que você faça um reload.

Quando você fizer o reload, provavelmente a primeira coisa que você verá será o vscode pedindo para você escolher um interpretador de python. Dependendo do ambiente do conda que você estiver trabalhando, a versão do python pode variar. Eu escolhi o ambiente base no momento. Veja que aparece do lado da branch que você está, no canto inferior esquerdo, qual a versão do python e o ambiente do conda!!

Agora com F5 nós temos a seguinte opção!

<img src=".\imgs\vscode\vs_19.png" style="zoom:67%;" />

Ótimo! Aperte Enter!

<img src=".\imgs\vscode\vs_20.png" style="zoom:67%;" />

Veja o que foi aberto, um terminal! Exatamente com o nosso zsh bonitinho e tudo mais!

O nosso código realmente funcionou, quem diria! "Texto novo!" foi impresso na tela.

---

Agora, se eu quisesse ter aberto um terminal antes, como eu faria?

Tem um menu lá no topo chamado Terminal > New Terminal. Simples assim.

---

Okay, agora eu fiz um código um pouco mais complexo, veja:

<img src=".\imgs\vscode\vs_21.png" style="zoom:67%;" />

Esse código funciona? Ao apertar F5 e escolhermos a primeira opção, a gente vê que "8" é impresso na tela. Okay, funciona!

Ta, mas eu tô com uma dúvida no funcionamento desse programa... que debugá-lo. Como faz? Você pode clicar do lado dos números das linhas e uma bolinha vermelho vai aparecer.

<img src=".\imgs\vscode\vs_22.png" style="zoom:67%;" />

Quando você apertar F5 + Enter novamente:

<img src=".\imgs\vscode\vs_23.png" style="zoom:67%;" />

O código parou exatamente onde colocarmos o breakpoint. Veja no lado esquerdo o valor de **a**, a variável **b** ainda não tem valor, se você apertar Step Over (F10) (ou a setinha caindo do lado do play) você verá que **b** assume o valor 5, se clicar novamente chega o momento do print e o código acaba. Esse é o funcionamento básico do debugger!!

---

Nesse momento, se você for no controle de versão, você verá o seguinte:

<img src=".\imgs\vscode\vs_24.png" style="zoom:67%;" />

Tá, mas que arquivo é esse "settings.json", a gente não criou isso. Bem, ele é criado sozinho pelo vscode! Se você der uma olhada na nossa árvore de arquivos, você verá que ele está dentro de .vscode...

Não tem uma maneira da gente ignorar esse arquivo e ele não ficar aparecendo toda hora no controle de versão??? Tem sim. É só adicionar o arquivo (ou a pasta) no **.gitignore**

<img src=".\imgs\vscode\vs_25.png" style="zoom:67%;" />

Abra o .gitignore e adicionar .vscode no topo do arquivo:

<img src=".\imgs\vscode\vs_26.png" style="zoom:67%;" />

Da onde vem esse .gitignore?? Lembre-se que quando criamos o repositório teste no GitHub, nós escolhemos para iniciá-lo com um gitignore de python. Pois bem, o GitHub já cria o gitignore com os arquivos mais comuns a serem ignorados em um projeto de python!

Pronto, o que temos agora no controle de versão:

<img src=".\imgs\vscode\vs_27.png" style="zoom:67%;" />

Apenas justamente o que mudamos! Ótimo.

Agora veja se você consegue adicionar os arquivos, fazer um commit e dar um push pro github. No fim você deverá ver:

<img src=".\imgs\vscode\vs_28.png" style="zoom:67%;" />

Sucesso!

---

Extra: você pode procurar por essential na extensões e instalar extensões que algum usuário juntou, como em:

<img src=".\imgs\vscode\vs_29.png" style="zoom:67%;" />

Se você não gostar de alguma é só desativar!
