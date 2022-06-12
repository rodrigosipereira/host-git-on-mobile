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
   <img src="./assets/images/f-droid-home.jpg" alt="instalando o f-droid" height="55%" style="max-width:250px;">
- Desenvolvimento: <br>
  <img src="./assets/images/f-droid-category.jpg" alt="instalando o f-droid" height="55%" style="max-width:250px;">
- Termux: <br>
   <img src="./assets/images/f-droid-development-category.jpg" alt="instalando o f-droid" height="55%" style="max-width:250px;">
- Instalar: **No meu caso já está instalado, no seu vai estar escrito instalar** <img src="assets/images/termux-app-on-f-droid.jpg" alt="Instalar o termux" height="55%" style="max-height:250px;">
- Desenvolvimento:

<p align="center">Com estes **aplicativos acima** instalados podemos prosseguir</p>

<br>

## Instalar dependências do sistema:

<span align="left">
<img src="https://www.vectorlogo.zone/logos/linux/linux-icon.svg" alt="linux" width="22" height="22">
</span>
<code><p>&& -> Faz com que um comando seja executado após o outro, caso não ocorra um erro.</p></code>
<code><p><pre><code>apt update && apt upgrade -y</code></pre></p></code>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o coreutils" width="22" height="22"><code><p><pre><code>apt install coreutils -y</code></pre></p></code>
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/curl_haxx/curl_haxx-ar21.svg" alt="instalando o curl" width="22" height="22"><code><p><pre><code>apt install curl -y</code></pre></p></code>
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o tar" width="22" height="22"><code><p><pre><code>apt install tar -y</code></pre></p></code>
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o tar" width="22" height="22"><code><p>#Depois de rodar esse comando aparece uma janela pedido acesso ao armazenamento do celular.</p></code><code><p><pre><code>termux-setup-storage</code></pre></p></code><br>
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o gnupg" width="22" height="22"><code><p><pre><code>apt install gnupg -y</code></pre></p></code>
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o gnupg" width="22" height="22"><code><p><pre><code>apt install zsh -y</code></pre></p></code>
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="instalando o gnupg" width="22" height="22"><code><p># Definir o zsh como shell principal.</p></code><code><p><pre><code>chsh -s zsh</code></pre></p></code>
</span><br>
<span align="left" style="margin:0;padding:0;">
<img src="https://www.vectorlogo.zone/logos/vim/vim-ar21.svg" alt="vim" width="29" height="18" style="margin:0;padding:0;"><code><p><pre><code>apt install vim -y</code></pre></p></code>
</span><br>
<span align="left">
<img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="22" height="22"><code><p><pre><code>apt install git -y</code></pre></p></code>
</span>
<br>
<h2>Configurar a chave SSH</h2>

<p>Primeiro instale os pacotes necessários</p>
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="configurando a chave SSH" width="22" height="22"><code><p><pre><code>apt install openssl-tool -y && apt install openssh -y</code></pre></p></code>

<p>Configure o seu nome de usuario e email no git.</p>
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="configurando a chave SSH" width="22" height="22"><code><p><pre><code>git config --global user.name "seu_nome_de_usuario" && git config --global user.email "seu_email@email.com"</code></pre></p></code>

<p>Agora crie a sua chave de acesso SSH.</p>
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="configurando a chave SSH" width="22" height="22"><code><p><pre><code>ssh-keygen -t rsa -C seu_email@email.com</code></pre></p></code>

<img src="./assets/images/criar-chave-ssh.jpg" alt="Criar chave ssh" height="55%" style="max-width:250px;">

<p>Agora vá para sua conta do Github faça login e em configurações clique em Chaves SSH e GPG.</p>

<p>Vai aparecer para inserir o nome e a chave ssh, o nome pode ser o que você preferir, agora a chave você vai encontar no pasta .ssh/id_rsa.pub no Termux.</p>
<p>Para exibir a chave do arquivo execute este comando abaixo, e lembre-se de copiar chave inteira, senão você terá problemas para fazer a conexão.</p>
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="configurando a chave SSH" width="22" height="22"><code><p><pre><code>clear && cat .ssh/id_rsa.pub</code></pre></p></code>

<p>Com a chave copiada volte para o Github e cole, agora é só enviar.</p>
<p>Para ver se tudo deu certo vamos fazer a conexão.</p>
<img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="configurando a chave SSH" width="22" height="22"><code><p><pre><code>ssh -T git@github.com</code></pre></p></code>
<p>Vai aparecer 2 perguntas! A primeira você só digita yes, a segunda você vai digitar a senha que foi pedida no momento que você criou a sua chave SSH.</p>

<br>
<h2>Autor</h2>

<img style="border-radius:50px;" src="https://avatars.githubusercontent.com/u/61669301?v=4" width="100px;" alt="minha foto de perfil do github">
<sub><b><a href="https://github.com/rodrigosipereira">Rodrigo Silva</a></b></sub>

## Conecte-se comigo:

<a href="https://instagram.com/rodrigosilva.n1" target="blank"><img src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/instagram.svg" alt="Rodrigo Silva" height="41" width="41" /></a>
<a href="https://www.linkedin.com/in/rodrigo-silva-pereira" target="blank"><img src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg" alt="Rodrigo Silva" height="41" width="41" /></a>
