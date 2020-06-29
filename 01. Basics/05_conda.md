## Conda

O conda é uma ferramenta muito completa para instalar e administrar pacotes para diversas linguagens de programação. Nosso foco é Python, e vamos usar o miniconda aqui. É bem legal você dar uma olhada mais afundo do porquê usar o Conda e quais são as ferramentas que ele oferece. Aqui vamos abordar talvez só a superfície.

## Instalando o Miniconda

Primeiro, faça o download do instalador do miniconda para o Linux: https://docs.conda.io/en/latest/miniconda.html#linux-installers

Versão usada neste tutorial: Python Version 3.7, name Miniconda3 Linux 64-bit.

Com a parte do tutorial anterior, você já é capaz de copiar o instalador que foi baixado para `/home/vinicius` (no caso `vinicius` vai ser o seu usuário do Ubuntu que você colocou).

Caso você tenha conseguido copiar o instalador para sua home, você verá algo do tipo:

<img src=".\imgs\conda\conda.png" style="zoom:67%;" />

Caso não tenha conseguido, dê uma olhada no tutorial anterior sobre arquivos no WSL.

A próxima etapa é instalar o miniconda com:

`$ bash Miniconda3-latest-Linux-x86_64.sh`

Continue apertando Enter, digite "yes" e aperte Enter para instalar no caminho padrão:

<img src=".\imgs\conda\conda_02.png" style="zoom:67%;" />

Digite "yes" para ele inicializar o conda no zsh. Feche o terminal e abra novamente.

A primeira coisa diferente a se perceber é o **(base)**:

<img src=".\imgs\conda\conda_03.png" style="zoom:67%;" />

Agora com o conda instalado e ativado, o **base** é o _environment_ em que estamos. Os _environments_ nos permitem que criamos ambientes separados para diferentes projetos. Nesses ambientes separados nós podemos instalar pacotes e suas depedências sem criar conflitos com outros ambientes. Você está criando um ambiente de desenvolvimento (neste caso de Python) que você poderá, por exemplo, instalar uma versão do Numpy (pacote de computação númerica) em um ambiente e outra versão em outro ambiente, sem que tenhamos nenhum conflito.

O Conda também é muito esperto e lida com conflitos do sistema operacional para nós. Pesquise mais sobre isso e veja como funciona.

# Environments

O ambiente padrão é o **base**, que já é criado quando você instala o conda. Vamos criar o nosso próprio ambiente. Para isso podemos usar o comando:

`$ conda create --name tutorial`

<img src=".\imgs\conda\conda_04.png" style="zoom:67%;" />

Podemos ver que para ativar o nosso ambiente **tutorial** nós temos que fazer:

`$ conda activate tutorial`

e você vai perceber que o **base** mudou para **tutorial**. Podemos ver todos (os dois) ambientes que temos até agora, fazendo:

`$ conda info --envs`

<img src=".\imgs\conda\conda_05.png" style="zoom:67%;" />

Veja que temos um **\*** no tutorial, indicando que estamos nele (além de termos **(tutorial)** escrito sobre **# vinicius...**, claro)

### Instalando pacotes

Agora vamos instalar um pacote no nosso ambiente.

`$ conda install numpy`

Ao executarmos este comando, não nós especificamos em momento nenhum qual versão do numpy nós queríamos instalar. Então a versão mais atual será instalada, e com esta versão mais atual todas as depedências (outros pacotes importantes para o funcionamento desta versão do Numpy).

Ao terminar a instalação, nós podemos ver quais pacotes agora fazem parte do nosso ambiente.

`$ conda list`

irá listar todos os pactoes e suas versões. Veja:

<img src=".\imgs\conda\conda_06.png" style="zoom:67%;" />

Veja que a versão do Numpy instalado foi a 1.18.1, e que a versão do Python é 3.8.3.

Podemos voltar para o ambiente **base** e ver quais pacotes estão instalados.

<img src=".\imgs\conda\conda_07.png" style="zoom:67%;" />

Veja que não temos Numpy e a versão do Python é 3.7.6. Ou seja, ao instalarmos a versão mais nova do Numpy, o Python também foi atualizado. O usuário mais atento percebeu que aconteceria antes de aceitar a instalação do Numpy.

#### Instalando um pacote com uma versão específica

Para instalar um pacote com uma versão específica no conda, faça o seguinte:

`$ conda install scipy=0.15.0`

Neste exemplo vamos instalar o pacote **scipy** na versão **0.15.0**.

Múltiplos pacotes com versões específicas ao mesmo tempo:

`$ conda install scipy=0.15.0 curl=7.26.0`

### Criando um ambiente a partir de pacotes especificados em um arquivo de requerimentos

É muito comum criarmos um ambiente a partir de um arquivo que nos diz exatamente quais pacotes precisam ser instalados.

Se tivermos um arquivo requirements.txt que foi criado diretamente de um ambiente do conda, ele vai ter mais ou menos essa cara:

<img src=".\imgs\conda\conda_08.png" style="zoom:67%;" />

O próprio começo do arquivo já nos diz como criar o ambiente. Vamos fazer:

`$ conda create --name tutorial02 --file requirements.txt`

Agora se você executar `$ conda info --envs`verá que tutorial02 foi criado.

Existem outras formas de criar ambientes a partir de arquivos, veja: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

### Atualizando um pacote

Para atualizar um pacote para sua versão mais atual, basta fazer:

`$ conda update numpy`

Neste caso vamos atualizar o **numpy** para sua versão mais recente. Simples, não?

### Apagando um ambiente

As vezes, nós criamos muitos e muitos ambientes para diversas tarefas. Tarefas que nem sempre vão a frente, o que terminam. Os ambientes antigos acabam esquecidos e tomam espaço. Então, apagar um ambiente às vezes se torna necessário.

Para remover um ambiente podemos executar:

`$ conda remove --name tutorial02 --all`

Neste caso estamos deletando **tutorial02**. Verifique com `$ conda info --envs`se ele realmente foi deletado. Se tudo ocorreu bem, você verá apenas **base** e **tutorial**.

Agora você também pode apagar o **tutorial** porque chegamos ao fim.

`$ conda remove --name tutorial --all`

Agora você tem apenas o **base** e todos os outros que você ainda criará.
