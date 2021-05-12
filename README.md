# Ranger Documentation

before install ranger should install [iterm_beautiy](./doc/iterm_doc.md) first

this file show how to install ranger

git clone to `~/.config/`

copy file `rc.conf` in `temp` $\to$ project root

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

	**For Mac**

	```bash
	pip3 ranger-fm                              # can not use package have bug
	brew install fzf                            # use git to install on linux
	brew insatll atool                          # for zip
	brew install ffmpegthumbnailer              # for preview video
	brew install pandoc                         # md to pdf
	brew install basictex                       # pdflatex for mac
	brew install poppler                        # pdf preview for mac
	```

	**For Arch**

	```bash
	sudo pacman -S install fzf
	sudo pacman -S insatll atool             # for zip
	sudo pacman -S insatll ueberzug          # for x11 img preview
	sudo pacman -S insatll ffmpegthumbnailer # for preview video
	sudo pacman -S install pandoc            # md to pdf
	sudo pacman -S install texlive-core      # md to pdf
	```

	set alias
	```bash
	alias ra='ranger'
	```

3. Create default config file

	```bash
	ranger --copy-config=all
	```
