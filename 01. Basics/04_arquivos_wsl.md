# Arquivos no WSL

Como eu faço para ver meus arquivos do Windows quando estou no terminal do Ubuntu do WSL?

Eles ficam em **/mnt/c**. Se você fizer: `$ cd /mnt/c`, você verá algo como:

<img src=".\imgs\wsl\wsl.png" style="zoom:67%;" />

A partir daí você pode caminhar (usando `cd`) pelas pastas do Windows e manipular os arquivos como você quiser.

Vou dar um exemplo de como você pode copiar um arquivo que está numa pasta sua do Windows pro WSL.

## Copiando arquivo "para dentro do Ubuntu"

Eu tenho um arquivo que eu acabei de baixar, o nome dele é **exemplo** e está em Downloads:

<img src=".\imgs\wsl\wsl_02.png" style="zoom:67%;" />

Como eu faço para mover este arquivo para `/home/vinicius` pelo terminal?

Primeiro, vamos até os Downloads do Windows, veja:

<img src=".\imgs\wsl\wsl_03.png" style="zoom:67%;" />

Já estou de olho no meu arquivo **exemplo.txt**. Agora eu vou copiar o arquivo usando:

`$ cp /mnt/c/Users/mesquita/Downloads/exemplo.txt /home/vinicius`

Será que deu certo? Podemos conferir com

`$ ls /home/vinicius` para ver se o arquivo está lá. Vejamos:

<img src=".\imgs\wsl\wsl_04.png" style="zoom:67%;" />

Realmente está lá em `/home/vinicius`. Agora, podemos voltar para `/home/vinicius` com `$ cd /home/vinicius` e ver o que tem dentro de **exemplo.txt** usando o comando `$ cat exemplo.txt` .

<img src=".\imgs\wsl\wsl_05.png" style="zoom:67%;" />

Sucesso!
