---
date: 2023-11-29

categories:
  - Nerdices
  - Linux
---

# Extensão própria do Archcraft

Eu já tenho uma estrutura de arquivos de configuração que se comportam como uma extensão dessa distribuição, porém ela sofreu uma grande atualização e eu vou ter que mudar algumas coisas. Instalei ela numa máquina virtual para ver o que mudou e eu poder organizar os arquivos.

Eia, pois, algumas preocupações.<!-- more --> Eu desejo ter os arquivos de configuração, novos temas, novos softwares, et cetera de forma a não esbarrar no sistema original e também manter a mesma filosofia com outros softwares além da distro, como o oh-my-zsh e o nvChad, por exemplo. Assim, que meus arquivos contenham carreguem as mudanças que eu desejo, porém que eles não impeçam a atualização fácil destes pacotes (o próprio Archcraft, o oh-my-zsh, o nvChad, et cetera.).

Contudo, vejo que não poderei fazer isso com perfeição, pois não poderei deixar tudo intacto e apenas construir por cima. Digo isso pois já sei que irei mudar coisas da distro, como desinstalar o vim, por exemplo, já que não o uso e a configuração do Archcraft deixa arquivos referentes ao vim na $HOME (não gosto disso). Além disso, arquivos referentes ao zsh também mudarão de posição, porém com as variáveis do sistema ajustadas corretamente, isso não deve dar problema. Logo após installar o Archcraft eu poderei mover os arquivos para os seus devidos lugares e dará tudo certo.

Também quero tomar cuidado para apenas manter na pasta de [dotfiles](./dotfiles.md) as coisas que eu realmente personalizo, e não arquivos que são gerados automaticamente pelos aplicativos e os quais eu nem edito. Assim mantenho as coisas mais simples, com mais visão do que eu realmente preciso me preocupar para manter a sincronia das minhas configurações, além de poupar espaço nos servidores do GitHub.

Observando a nova atualização, eu vejo que mesmo que eu mude os arquivos e scripts dos novos temas para os lugares novos, eu ainda precisarei esperar atualizar para mudá-los para os novos padrões. Vale dizer que, até o momento, só me preocupei com as configurações do Openbox. Só irei me preocupar com os bspwm depois de atualizar.

Vou listar as coisas que quero tirar da `$HOME` da instalação recém feita do Archcraft. Quero deixar documentado para uma futura visita, caso algo seja crucial deixar eu posso vir e mencionar no post:

```bash
.icons/
.mpd/
.ncmpcpp/
.vim_runtime/      # desinstalar o vim (deixando apenas o Neovim)
.bash_logout       # quero usar apenas o zsh para o terminal
.bash_profile      # quero usar apenas o zsh para o terminal
.bashrc            # quero usar apenas o zsh para o terminal
.dmrc
.face
.fehbg
.gtkrc-2.0
.hushlogin
.vimrc             # desinstalar o vim (deixando apenas o neovim)
.zcompdump...      # deixar apenas um .zshenv para ajeitar as coisas
.zcompdump...zwc   # deixar apenas um .zshenv para ajeitar as coisas
.zsh_history       # deixar apenas um .zshenv para ajeitar as coisas
.zshrc             # deixar apenas um .zshenv para ajeitar as coisas
```
