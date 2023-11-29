---
date: 2023-11-29

categories:
  - Linux
---

# Minha distribuição Linux

Eu uso o [Arch Linux](https://archlinux.org/) já a alguns anos, gosto muito dela. Gosto do gerenciador de pacotes `pacman` e de poder modular as coisas do jeito que quiser, mantendo ela leve (mesmo que tenha espaço e hardware para um ambiente linux mais convencional), enfim, é um gosto que tenho.

Algum tempo atrás descobri a distribuição [Archcraft](https://archcraft.io/). Ela é, obviamente, baseada no Arch Linux e é simples na sua construção, seguindo a linha de como eu mesmo vinha montando o sistema com o Arch original. Inicialmente instalei ela para ver como ela era construída, os pacotes que eram utilizados, como era o sistema de trocar os temas. Eu já tinha uma ideia e um princípio de um script juntamente com uma estrutura de arquivos para gerar um utilitário que possibilitasse mudar completamente a aparência do ambiente rapidamente e quando eu quisesse, mas então antes de seguir em frente e aumentar a complexidade do que eu já tinha, fui ver como essa distribuição havia feito.

Eu acabei ficando no próprio Archcraft por bastante tempo e até pensei recentemente em voltar ao Arch original. Eu queria retirar algumas coisas do Archcraft, para mim utilizar o [Oh My Zsh](https://ohmyz.sh/) é demais para o que quero do zsh, além de que essa distribuição deixa por padrão várias coisas na pasta home e eu não gosto disso. Dá para ajeitar algumas das coisas, porém eu não queria ficar preso em ter que ajeitar novamente quando fosse atualizar a distribuição. Por isso, o Arch original parece mais simples, no sentido de ser exatamente como eu o fizer.

Contudo, o pessoal do Archcraft têm mais conhecimento e dedica mais tempo na construção da estrutura da distro ao mesmo tempo que eles seguem uma linha da qual lembra o que eu tendo a fazer. Para que eu não gaste mas muito tempo eu decidi continuar com o Archcraft e fazer uma extensão dele mesmo para as configurações que eu quiser e me preocupar apenas com pacotes adicionais que eu queira, não com todos. Assim eu já parto de um lugar que eu gosto e que pode ser instalado com um instalador gráfico (que é uma boa, pois da última vez que tentei utilizar o script de instalação do Arch Linux, eu não consegui fazer o particionamento com Windows e Arch partilhando SSD + HD e tive que ir na instalação mais manual do Arch).

Para atualizar para a última versão da distro eu vou precisar reinstalá-la, pois ela recebeu uma grande atualização. Junto a isso, eu tenho curiosidade de instalar o [Pop! Os](https://pop.system76.com/) novamente e ver como é utilizar ele com a opção que o deixa ele organizando as janelas (gosto de utilizar tiling window managers), porém, o instalador dele está exigindo um espaço na partição /boot que eu não tenho agora, exigindo também uma reinstalação do sistema.

Eu curto utilizar tiling window managers porque eles são extremamente leves. Quando eu pressiono o atalho para abrir o terminal a resposta é praticamente instantânea, eu gosto disso e não é assim quando estou num gerenciador de janelas flutuantes. Gosto muito do [i3wm](https://i3wm.org/), mas como o Archcraft já vem com o bspwm eu vou dar uma chance a ele (e também vou deixar o Hyperland de lado por agora já que o Wayland precisaria de uma atenção especial sem utilizar uma distro que já o tenha com as coisas ajeitadas por padrão). O Archcraft também já vem com uma opção legal se eu quiser ir para um ambiente de janelas flutuantes, que é o gerenciador de janelas que eu uso atualmente, o Openbox.

Agora eu tenho que ajeitar minha extensão do Archcraft para então reinstalá-lo e já poder utilizar os meus dotfiles. Quero não mexer na estrutura geral, porém o que eu conseguir deixar fora da /home eu vou. Muito desse trabalho já foi feito usando o [xdg-ninja](https://github.com/b3nj5m1n/xdg-ninja) e será mantido.

