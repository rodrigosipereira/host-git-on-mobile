<h1 align="center">Subindo repositório git remoto pelo celular</h1>
<p align="center">Neste guia eu vou explicar como eu fiz para subir meus projetos git pelo celular com SSH</p>

## Tópicos:
<!--ts-->
  * [Pré-requisitos](#pre-requisitos)
  * [Instalar dependências](#Instalar-dependências-do-sistema)
<!--te-->

## Pré-requisitos:
- [F-droid](https://f-droid.org)
- [Termux](#instalar-o-termux)

## Instalar o termux
- Abra o aplicativo f-droid
- Va para categorias: <br>
   <img src="./assets/images/f-droid-home.jpg" alt="vim" height="55%" style="max-width:250px;">
- Desenvolvimento: <br>
  <img src="./assets/images/f-droid-category.jpg" alt="vim" height="55%" style="max-width:80px;">
- Termux: <br>
   <img src="./assets/images/f-droid-development-category.jpg" alt="vim" height="55%" style="max-width:250px;">
- Instalar: **o meu caso já está instalado, no seu vai estar escrito instalar** <img src="assets/images/termux-app-on-f-droid.jpg" alt="Instalar o termux" height="55%" style="max-height:80px;">
- Desenvolvimento:

<p align="center">Com estes **aplicativos acima** instalados podemos prosseguir</p>

<br>

## Instalar dependências do sistema:

<span align="left">
<img src="https://www.vectorlogo.zone/logos/linux/linux-icon.svg" alt="linux" width="22" height="22">
</span> ```bash # && -> Faz com que um comando seja executado após o outro, caso não ocorra um erro.\napt update && apt upgrade -y ``` <br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o coreutils" width="22" height="22"> ```bash apt install coreutils -y```
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/curl_haxx/curl_haxx-ar21.svg" alt="instalando o curl" width="22" height="22"> ```bash apt install curl -y```
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o tar" width="22" height="22"> ```bash apt install tar -y```
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o tar" width="22" height="22"> ```bash #Depois de rodar esse comando aparece uma janela pedido acesso ao armazenamento do celular.\ntermux-setup-storage``` <br>
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o gnupg" width="22" height="22"> ```bash apt install gnupg -y```
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o gnupg" width="22" height="22"> ```bash apt install zsh -y```
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o gnupg" width="22" height="22"> ```bash # Definir o zsh como shell principal\nchsh -s zsh```
</span><br>
<span align="left" style="margin:0;padding:0;">
<img src="https://www.vectorlogo.zone/logos/vim/vim-ar21.svg" alt="vim" width="29" height="18" style="margin:0;padding:0;"> ```bash apt install vim -y```
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="22" height="22"> ```bash apt install git -y```
</span>
<!--
<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs/?username=rodrigosipereira&layout=compact&hide=html" alt="rodrigosipereira"></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=rodrigosipereira&show_icons=true" alt="rodrigosipereira"></p>
-->
<br><br>
## Autor

<img style="border-radius:50%;" src="https://avatars.githubusercontent.com/u/61669301?v=4" width="100px;" alt="">
<sub><b><a href="https://github.com/rodrigosipereira">Rodrigo Silva</a></b></sub>

## Conecte-se comigo:

<a href="https://instagram.com/rodrigosilva.n1" target="blank"><img src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/instagram.svg" alt="Rodrigo Silva" height="41" width="41" /></a>
<a href="https://www.linkedin.com/in/rodrigo-silva-pereira" target="blank"><img src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg" alt="Rodrigo Silva" height="41" width="41" /></a>
