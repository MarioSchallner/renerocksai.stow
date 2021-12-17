# What to install

Eventually, we will go down the ansible route.

## Essentials

- binutils
- build-essential, cmake
- neovim, [see below](#neovim)
- git
- git-crypt
- stow
- i3
- zsh
  - oh-my-zsh
  - [starship](#starship-prompt)
- tmux
- htop
- ncdu
- xclip
- ripgrep
- zig
- python
  - anaconda python 3.9 (version checks of some shitty tools fail with 3.10)
- lua5.1
  - stylua
    - via [github](https://github.com/JohnnyMorganz/StyLua) releases or cargo (install first)
  - luacheck
    - via apt or luarocks (install first)
- flutter
- libasound2-dev
- mediainfo
- zip, unzip
- p7zip
- rar
- xz-utils

### more stuff

- obs-studio
- texlive
- sdl2-dev
- steam-installer
- flameshot
- discord
- samba client / utils
- (audacity)
- krita
- cloc
- docker-ce
- ffmpeg
- firefox
- gcc, g++
- gimp
- ghdl, gtkwave
- imagemagick
- jq
- insomnia
- mongodb-org
- ninja-tools
- nodejs

## neovim

See [here](https://github.com/neovim/neovim/wiki/Installing-Neovim#install-from-source) for more info.

```console
git clone
make CMAKE_BUILD_TYPE=Release
sudo make install
```

```console
pip install neovim
```

## firenvim

- browser plugin
- then:
  - bro tip from theprimeagen: use a truthy number instead of 0 below for all non-chrome or firefox:  chromium browsers like chromium, brave, etc
  - see [theprimeagen's video](https://www.youtube.com/watch?v=ID_kNcj9cMo) for install issues with brave

```console
nvim --headless "+call firenvim#install(0) | q"
```

## Language Servers

### Python

```console
$ cd language-servers

# to get all the python lsp stuff
$ pip install -r requirements.txt 
```

### lua

- Execute `~/.config/nvim/bundle/nlua.nvim/scripts/download_sumneko.lua via`
  - `:luafile %` after loading it in nvim.
- then copy the executable and supporting files like shown below:

```console
cd ~/.cache/nvim/nlua/sumneko_lua/lua-language-server/bin
mkdir Linux
cp * Linux/
```

### zig

Download the zig language server from github and unpack it in ~/bin/

### markdownlint (for null-ls)

```console
sudo npm install -g markdownlint-cli
```

## starship prompt

```console
sh -c "$(curl -fsSL https://starship.rs/install.sh)"
```
