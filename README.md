# UniTeX

UniTeX is a collection of scientific oriented and minimalistic [LaTeX](https://www.latex-project.org/) templates suitable for many assignement types.

![LaTeX](https://img.shields.io/badge/latex-%23008080.svg?style=for-the-badge&logo=latex&logoColor=white) ![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)

## Table of contents

- [Requirements](#requirements)
- [Installation](#installation)
- [Quick start](#quick-start)
- [Screenshots](#screenshots)
  - [Classic](#classic)
  - [Article](#article)
  - [Homework](#homework)
- [TODO](#todo)
- [Credits](#credits)

## Requirements

UniTeX requires a complete TeX distribution (you can find the most used TeX distributions
[here](https://www.latex-project.org/get/#tex-distributions)). Most features need external tools such as latexmk that fully automates LaTeX document generation. Latexmk is usually part of TeX distributions like MikTeX and MacTeX but you can always install it separately by following [these](https://mg.readthedocs.io/latexmk.html) steps.

A Unix shell is also required to install UniTeX properly. A pdf viewer like [Skim](https://skim-app.sourceforge.io/),
[Zathura](https://pwmt.org/projects/zathura/index.html) and [SumatraPDF](https://www.sumatrapdfreader.org/free-pdf-reader) is also fun to have
when working on LaTeX projects.

## Installation

The ideal way to install UniTeX is via the install script `install.sh`.

```shell
$ git clone https://github.com/BCarnaval/UniTeX
...
$ cd UniTeX && chmod +x install.sh && ./install.sh
```

By doing it like so, you will be able to use UniTeX's commands `unitex -...`.

## Quick start

Once [installation](#Installation) properly done and `unitex -v` command outputs no error, you can directly build
your first UniTeX template

1. Create a folder (**test** in home folder for the example) in which store template's files that you will actually edit.

```shell
$ mkdir ~/test
```

2. Build your template inside this directory using `unitex` by specifying the flags **-b build**: template (classic, article, homework), **-d directory**: directory in which build it (use directory created in step 1.) and **-o opt**: building options (`clean`, `dry`, `targz` or `zip`).

```shell
$ unitex -b classic -d ~/test -o dry
```

Here, the `dry` option means that latexmk will not compile your project continuously and not clean the directory either. To clean it, you must use the option `clean` with the `-o` flag. These commands being done (`dry` and `clean`), you should have the following content inside your **test** folder

```shell
$ ls ~/test
Makefile
PageTitre.tex
colors.sty
commands.sty
figs
main.pdf
main.tex
refs.bib
sections
style.sty
```

3. If you read this I am assuming that your **test** directory isn't missing any files and you now are ready to configure/customize the template to satisfy the nature of your project. To do this, you simply open your favorite text editor and remove default values from `PageTitre.tex`, `main.tex`, all the files inside `sections/` and `figs/` directories, references from `refs.bib` and feel free to add your personnal commands inside `commands.sty`.

## Screenshots

### Classic

Example of what you should get from 'classic' template and Yale's darkblue as main color

<table>
  <tr>
    <td>Default title page</td>
    <td>Sections layout</td>
  </tr>
  <tr>
    <td><img src="/../screenshots/screenshots/title_screen.png" width=360 height=480></td>
    <td><img src="/../screenshots/screenshots/mid_screen.png" width=360 height=480></td>
  </tr>
 </table>

<table>
  <tr>
    <td>Maths display</td>
    <td>References</td>
  </tr>
  <tr>
    <td><img src="screenshots/math_screen.png" width=360 height=480></td>
    <td><img src="screenshots/refs_screen.png" width=360 height=480></td>
  </tr>
 </table>
 
### Article

### Homework

## TODO

- [x] 'Classic' template
- [ ] 'Article' template (RevTeX)
- [ ] 'Homework' template (Overleaf's rebuild)
- [x] Install/uninstall scripts
- [ ] Test on fresh Linux and Mac OS (Docker)
- [ ] Man pages (MacOS, Linux)
- [ ] Version control
- [ ] REAME.md

## Credits
