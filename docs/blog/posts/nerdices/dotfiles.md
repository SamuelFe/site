---
date: 2023-11-29

categories:
  - Nerdices
  - Linux
---

# dotfiles

Atualmente eu mantenho meus arquivos de configuração como arquivos que na verdade são links simbólicos para uma outra pasta onde os edito e controlo, a pasta `~/.dotfiles`. De lá, posso fazer os links irem para seus lugares corretos usando o programa stow.

Esse post é pra documentar a mudança que desejo fazer para simplificar a estrutura da pasta `~/.dotfiles`.<!-- more --> Atualmente ela está feita de tal forma que não preciso usar um arquivo `.stow-local-ignore` e posso selecionar os arquivos a serem “linkados” ao sistema por aplicativo, porém, as vezes em que isso foi útil foram extremamente raras. Estou optando por me desfazer deste esquema para simplificar a estrutura e assim a pasta de configurações fica simplesmente com a “cara” da pasta $HOME.

Atualmente a estrutura da pasta está assim:

```bash
.
├── .git
│   ├── ...
├── .gitignore
├── README.md
├── dmscripts
│   └── .config
│       └── dmscripts
├── home
│   └── .zshenv
├── install
├── lf
│   └── .config
│       └── lf
├── local
│   └── .local
│       └── share...
├── lsd
│   └── .config
│       └── lsd
├── mpv
│   └── .config
│       └── mpv
├── nvim
│   └── .config
│       ├── nvim
│       └── nvim.old
├── oh-my-zsh
│   └── .config
│       └── oh-my-zsh
├── openbox
│   └── .config
│       └── openbox
├── packages
├── rofi
│   └── .config
│       └── rofi
├── shell
│   └── .config
│       └── shell
├── sxhkd
│   └── .config
│       └── sxhkd
├── uninstall
├── yay
│   └── .config
│       └── yay
├── zathura
│   └── .config
│       └── zathura
└── zsh
    └── .config
        └── zsh
```

E vou mudar para algo assim:

```bash
.
├── .config
│   ├── dmscripts
│   │   └── config
│   ├── lf
│   │   ├── lfcd.sh
│   │   └── lfrc
│   ├── lsd
│   │   ├── config.yaml
│   │   └── themes
│   ├── mpv
│   │   ├── input.conf
│   │   ├── mpv.conf
│   │   └── watch_later
│   ├── nvim
│   │   └── lua
│   ├── nvim.old
│   │   ├── coc-settings.json
│   │   ├── colors
│   │   ├── init.vim
│   │   ├── plugin-configs
│   │   ├── snippets
│   │   └── spell
│   ├── oh-my-zsh
│   │   └── custom
│   ├── openbox
│   │   ├── polybar
│   │   └── scripts
│   ├── rofi
│   │   ├── config.rasi
│   │   ├── config.rasi.bkp
│   │   └── themes
│   ├── shell
│   │   └── aliases
│   ├── sxhkd
│   │   ├── bindings
│   │   └── sxhkdrc
│   ├── yay
│   │   └── config.json
│   ├── zathura
│   │   └── zathurarc
│   └── zsh
│       ├── .zcompdump
│       ├── .zcompdump-arch-5.9
│       ├── .zprofile
│       ├── .zshrc
│       └── plugins_configs
├── .git
│   ├── ...
│   ...
├── .gitignore
├── .local
│   └── share
│       ├── applications
│       └── themes
├── .stow-local-ignore
├── .zshenv
├── README.md
├── install
├── packages
└── uninstall
```
