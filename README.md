# astra-bib

This submodule contains the latest bibliography for [The optimisation group](http://www.it.uu.se/research/group/optimisation/). Use this as a git submodule for your bibliography when writing papers.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

You need (pdf)latex, bibtex, and git.

### Installing

Navigate to the folder of your latex paper, initialise it as a github repository

```bash
git init
```

Then add this repository as a submodule, initialise it, and update it.

```bash
git submodule add https://github.com/astra-uu-se/astra-bib.git
git submodule init
git submodule update --remote
```

Add the bibliography to your latex file.

```latex
...
\bibliography{astra-bib/astra}
```

Additionally you can change the `.gitsubmodules` file if you are using a branch other than master:
```git
[submodule "astra-bib"]
	path = astra-bib
	url = https://github.com/astra-uu-se/astra-bib.git
    branch = your-branch-name-here
```

## Compiling the bibliography

In order to compile the bibliography for a paper with name `paper.tex` (**Note:** you can also use the `pdflatex` command instead of the `latex` command).

```bash
latex paper; latex paper; bibtex paper; latex paper
```

### Updating

```bash
git submodule update --remote
```
## Contributing

**Note: Do not add or commit directly to a submodule!**.
Clone this repository, then perform any changes to the clone before adding and commiting.
