# 01. Basics

Este é um pequeno tutorial para você dar os passos iniciais no caminho para aprender:
  - [a instalar o terminal do Ubuntu via WSL](./01_wsl.md)
  - [a instalar o Zsh e o Oh My Zsh (nossa ferramenta favorita pro terminal)](./02_zsh.md)
  - [a usar comandos essenciais do terminal do Ubuntu](03_terminal.md)
  - [a acessar arquivos do Windows via WSL](04_arquivos_wsl.md)
  - [a instalar e usar o Conda](05_conda.md)
  - [a usar o Git e o GitHub](06_git.md)
  - [a instalar, configurar e usar o VSCode](07_vscode.md)

Esta é a ordem que deve ser seguida neste tutorial/guia. Cada parte do guia deve funcionar sozinha, mas elas também se complementam. 

Criada e mantida pelo grande mestre [@mesquita](http://github.com/mesquita).


## Recursos Rápidos de Suporte para Conhecimentos de Base

## Git

Git é uma ferramenta para controle de versão de arquivos e vamos usá-la constantemente. Seja qual for o lugar que você vá, a equipe de desenvolvimento usará o Git. Logo, é muito importante que aprenda!

Git não é difícil, mas no primeiro instante causa uma leve confusão, então não hesite em pedir socorro!

- Quer uma ajudinha rápida para resolver seu problema? Então, veja [aqui](https://rogerdudler.github.io/git-guide/) (tutorial básico excelente)

- Para consultar comandos, veja essa [Cheatsheet](https://github.github.com/training-kit/downloads/pt_BR/github-git-cheat-sheet/)

- Se você não sabe usar Git e o GitHub, [essa página](https://try.github.io/) tem os recursos necessários.

## Python

Para rapidamente refrescar a memória sobre conceitos básicos de Python, consulte o
[Python Handbook](https://anandologdy.com/python-practice-book)

Para uma rápida introdução a Numpy e Matplotlib, veja [esse tutorial](http://cs231n.github.io/python-numpy-tutorial/) (Ambas bibliotecas serão usadas extensivamente).

Quer ir mais afundo em _Numpy_? Veja esse [Colab](https://colab.research.google.com/github/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/02.00-Introduction-to-NumPy.ipynb)

### Instalação

Recomendamos que use o gerenciador de pacotes [Conda](https://docs.conda.io/) para instalar python e as bibliotecas. [Clique aqui](https://docs.conda.io/en/latest/miniconda.html) para ir à página de download do Miniconda. Certifique-se de baixar a versão Python 3.7.

Se você está em uma máquina windows:

- Abra o executável depois de terminar o download e siga as instruções.
- Depois de completa a instalação, abra `prompt Anaconda` a partir do menu inicial. Isso vai abrir um terminal com o python habilitado.

Se você está em uma máquina linux:

- Abra o terminal e navegue até o diretório para onde foi baixadoo Anaconda

- Mude a permissão do arquivo para que possa ser possível executá-lo. Se o nome do arquivo baixador for `Miniconda3-latest-Linux-x86_64.sh`, então use o seguinte comando:

  `chmod a+x Miniconda3-latest-Linux-x86_64.sh`

- Agora, rode o script de instalação `./Miniconda3-latest-Linux-x86_64.sh` e siga as instruções de instalação no terminal.

## Interactive Python

Para entender melhor como o Jupyter notebook funciona, quais são os comandos especiais e os atalhos, começe por [aqui](https://colab.research.google.com/github/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/01.00-IPython-Beyond-Normal-Python.ipynb#scrollTo=qPlt8_Btyemw).
