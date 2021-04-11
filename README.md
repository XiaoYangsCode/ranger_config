# Ranger Documentation

before install ranger should install [iterm_beautiy](./doc/iterm_doc.md) first

this file show how to install ranger

git clone to `~/.config/`

1. Keymapping

| hotkey      | action                      |
|-------------|-----------------------------|
| `a`         | rename create file          |
| `A`         | rename file at the end      |
| `I`         | rename file at the head     |
| `at`        | create a new file           |
| `af`        | create a new file with nvim |
| `cw`        | buklrename                  |
| `M`         | mkcd                        |
| `C-f`       | fzf_select                  |
| `g`         | go to fold                  |
| `o`         | sort                        |
| `shift`+`s` | cd to path in terminal      |
| `y`         | yank                        |
| `p`         | paste                       |
| `d`         | cut or delete               |
| `space`     | choose one file             |
| `v`         | choose all file             |
| `w`         | task view                   |
| `C`         | compress file to zip        |
| `yy`+`X`    | extract file from zip       |
| `cp`        | change md to pdf            |


2. Install package

  install nerd-font first at [https://github.com/ryanoasis/nerd-fonts](https://github.com/ryanoasis/nerd-fonts)
```bash
mkdir -p ~/.local/share/fonts
cd ~/.local/share/fonts && curl -fLo "Droid Sans Mono for Powerline Nerd Font Complete.otf" https://github.com/ryanoasis/nerd-fonts/raw/master/patched-fonts/DroidSansMono/complete/Droid%20Sans%20Mono%20Nerd%20Font%20Complete.otf
```

```bash
pip3 ranger-fm                              # can not use package have bug
brew install fzf                            # use git to install on linux
brew insatll atool                          # for zip
brew install w3m                            # for preview on linux mac use iterm2
brew install ffmpegthumbnailer              # for preview video
brew install pandoc                         # md to pdf
brew install basictex                       # pdflatex for mac
sudo apt install texlive-latext-base        # pdflatex for linux
sudo apt install texlive-latext-recommended # pdflatex for linux
sudo apt install texlive-fonts-recommended  # pdflatex for linux
sudo apt install texlive-latext-extra       # pdflatex for linux
brew install poppler                        # pdf preview for mac
```
set alias
```bash
alias ra='ranger'
```

3. Create default config file

```bash
ranger --copy-config=all
```
4. Change config file

we can learn how to change config at [https://github.com/ranger/ranger/wiki](https://github.com/ranger/ranger/wiki)
- Img video and pdf preview
- Set default Open editor(use nvim)

change rifle.conf, editor to nvim

orginal
```bash
#-------------------------------------------
# Misc
#-------------------------------------------
# Define the "editor" for text files as first action
mime ^text,  label editor = $EDITOR -- "$@"
mime ^text,  label pager  = "$PAGER" -- "$@"
!mime ^text, label editor, ext xml|json|csv|tex|py|pl|rb|js|sh|php = $EDITOR -- "$@"
!mime ^text, label pager,  ext xml|json|csv|tex|py|pl|rb|js|sh|php = "$PAGER" -- "$@"
```
to
```bash
#-------------------------------------------
# Misc
#-------------------------------------------
# Define the "editor" for text files as first action
mime ^text,  label editor = nvim -- "$@"
mime ^text,  label pager  = "$PAGER" -- "$@"
!mime ^text, label editor, ext xml|json|csv|tex|py|pl|rb|js|sh|php = nvim -- "$@"
!mime ^text, label pager,  ext xml|json|csv|tex|py|pl|rb|js|sh|php = "$PAGER" -- "$@"
```
- Install plugins: Ranger Devicons plugin (needs to install nerd-font first)

5. Custom commands
- mkcd (mkdir + cd)
- fzf_select
- compress and extracter for zip
- code for `move to trash` is not same on linux and mac (in rc.conf)

6. Problem
**comment scope.sh for freeze the wnd**
```bash
#pygmentize -f "${pygmentize_format}" -O "style=${PYGMENTIZE_STYLE}"\
    #-- "${FILE_PATH}" && exit 5
```



