# Instalando Ubuntu via WSL

A melhor fonte de informação para saber como instalar o Windows Subsystem for Linux (WSL) é pelo site oficial da Microsoft: https://docs.microsoft.com/en-us/windows/wsl/install-win10

Fique atento porque este manual pode ficar desatualizado (ele foi feito em junho de 2020).

## Instale o WSL

Antes de instalar o Ubuntu, temos que ativar o WSL. Para isso, abra o powerShell como administrador.

<img src=".\imgs\install_wsl\powershell.png" alt="Powershell" style="zoom: 67%;" />

Para chegar na imagem anterior você pode apertar o botão do Windows no teclado e digitar powershell diretamente.

Ao abrir o powershell você deverá ver algo semelhante a isto (repare que é importante ter escrito o Administrator no topo da janela, significa que você está com permissões de administrador).

<img src=".\imgs\install_wsl\powershell_02.png" style="zoom: 67%;" />

Digite o seguinte comando:

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

e aperte Enter.

Você verá uma tela parecida com esta, onde ele diz "Enabling feature(s)":

<img src=".\imgs\install_wsl\powershell_03.png" style="zoom: 67%;" />

Agora, aguarde (pode demorar um pouco). Após a mensagem de término, **reinicie o computador**.

## Instalando o Ubuntu

Agora vamos a distribuição do Linux que vamos usar, o Ubuntu.

Vá até a Microsoft Store

<img src=".\imgs\install_wsl\store.png" style="zoom:60%;" />

e procure por Ubuntu

<img src=".\imgs\install_wsl\store_02.png" style="zoom:60%;" />

Vamos usar a versão Ubuntu 18.04 LTS neste tutorial.

Clique nesta versão e instale, você verá o progresso como na imagem seguinte.

<img src=".\imgs\install_wsl\store_03.png" style="zoom:67%;" />

Ao término da instalação você pode clicar em Iniciar e verá a seguinte tela:

 <img src=".\imgs\install_wsl\ubuntu.png" style="zoom:67%;" />

Em alguns instantes o nosso Ubuntu que está iniciando pedirá um nome de usuário e uma senha, como na imagem a seguir.

<img src=".\imgs\install_wsl\ubuntu_02.png" style="zoom:67%;" />

E pronto, você agora tem acesso ao Ubuntu via WSL.

Agora toda vez que você quiser usar o terminal do ubuntu, basta procurar o aplicativo no menu iniciar do Windows.
