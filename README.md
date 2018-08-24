# Ashton Hellwig CV/Resume

## Common Errors

### Font ** not found

```bash
user> if [[ ! -d "${HOME}/.fonts/TTF" ]]; then
  mkdir -p "${HOME}/.fonts/TTF"
fi

user> ln -s /usr/share/texmf-dist/fonts/<path>/<to>/<font>/ ${HOME}/.fonts/<FONT_TYPE>/
```

Alernatively (as root):

```bash
root> ln -s /etc/fonts/conf.avail/09-texlive-fonts.conf /etc/fonts/conf.d/09-texlive-fonts.conf
```

```bash
root> fc-cache && mkfontscale && mkfontdir
```

### FontAwesome undefined

(Arch Linux)

```bash
# Create a build directory
cd $HOME
mkdir ./BUILDS
cd BUILDS

# Get the sources
git clone https://aur.archlinux.org/fontawesome.sty.git fontawesome-sty
cd fontawesome-sty

# Verify PKGBUILD
cat ./PKGBUILD | [less|more|most]

# Install
makepkg -si --noconfirm

# Update texhash
sudo texhash ; sudo mktexlsr
```

## External Licences

### cv-style.cls

> The class cv-style.cls was originally created by
> Adrien Friggeri and has been modified to be compiled using Overleaf by
> Alejandro Pérez Londoño. This template is under the licence [Creative commons 4.0][1].
>
> Changes, Germain Salvato Vallverdu
>
> April 2016
>   * remove lang options and update lastupdated macro. Put the text you want
>     in the macro.
>   * add shortcuts to adjust page layout
>   * change colors
>   * update sectioncolor macro. Now there is two arguments. The first one is
>     colored.

[1]: https://creativecommons.org/licenses/by/4.0/legalcode