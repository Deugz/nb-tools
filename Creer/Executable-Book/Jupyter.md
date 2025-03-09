# Jupyter Book

:::::{div} full-width

<br>

<p class="emphase"> Intro line </p>


**Ressources**:

- [jupyterdays](https://ubc-dsci.github.io/jupyterdays/sessions/beuzen/jupyter_book_tutorial.html) from UBC (a bit outdated but good source)
- [Guide en Francais](https://perso.crans.org/besson/Info-Prepas-MP2I/Modele-de-livre-avec-Jupyter-Book/book.pdf)


***


:::::




## Introduction

### <strong> &#x2023; <u> Jupyter Book 101 </u></strong> 

:::::{div} full-width

::::{grid} 3

:::{grid-item}
:columns: 3

<br>
This video walk you through the steps required to start your journey using Jupyter Book. This is personnaly where I started. 


:::

:::{grid-item}
:columns: 1



:::



:::{grid-item}
:columns: 8

<div class="embedresize">
<iframe width="100%" height="56.25%" src="https://www.youtube.com/embed/lZ2FHTkyaMU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

:::

::::

:::::

### <strong> &#x2023; <u> Before to start </u></strong>

:::::{div} full width

::::{grid} 3

:::{grid-item}
:columns: 4

#### Requirements

- **Knowledge**

    - [Markdown](): this is the synthax you will use to write your book content


<br>

- **Softwares**

    - [Anaconda]() 

    - [Jupyter Lab]
    - Python IDE
    - Command Line Interface (CLI)


:::

:::{grid-item}
:columns: 4

#### Ressources


- [Jupyter meet the earth](https://jupytearth.org/index.html)
    - To explore and extract information (figures ...)



:::

:::{grid-item}
:columns: 4

#### Examples


- [Turing Way]() ... Good guide for open science


:::

::::

:::::



### <strong> &#x2023; <u> Create your first book </u></strong>

:::::{div} full-width

::::{grid} 2

:::{grid-item}

Open `Jupyter Lab` and enter the following command.

```

jb create bookname/

```

:::

:::{grid-item}

```{note} 

You can also **fork** a book created by someone else via Github (*link towards templates when created*).

```

:::

::::

:::::



<p class="emphase">This is it! You have just created your first book, now let's explore a bit deeper</p>


## Project Structure

### <strong> &#x2023; <u> Folders </u></strong> 

:::::{div} full-width

::::{grid} 2

:::{grid-item}
:columns: 4


```text
quickstart/
  ├── 🆕 _build
  │   ├── exports
  │   ├── site
  │   │   ├── content
  │   │   ├── public
  │   │   └── config.json
  │   ├── temp
  │   └── templates
  │       ├── site/myst/book-theme
  │       └── tex/myst/arxiv_two_column
  ├── images
  │   ├── image.png
  │   └── image.gif
  ├── 01-paper.md
  ├── 02-notebook.ipynb
  ├── README.md
  └── 🆕 myst.yml
```

:::

:::{grid-item}
:columns: 8

```{note}

Insert real folder structure of this book (show below in dropdown the full ontology map)

```

Explanation of the different folders etc ...
- _build
- _static

:::
::::
:::::

### <strong> &#x2023; <u> Files </u></strong> 

```{note}

Explain the different files _tocuse grid 2 
- 1 is capture d'ecran de page or page structure
- gauch is explanation of different section
```


::::::::{div} full-width
:::::::{dropdown} In Depth Explanation

::::::{tab-set}

:::::{tab-item} _config.yml

- [Jupyter-Book](https://jupyterbook.org/en/stable/customize/config.html)

::::{grid} 2

:::{grid-item}
:columns: 6

- **title**: title of your book (will appear on the navbar)
- **author**: you obviously (will appear in the footer)
- **logo**: will appear on the top left (above the left navbar)
<br>
- **execute**: if you want to force or not the execution of the ipynb files when building the book, can take different value
    - force: 
<br>
- **latex**:
<br>
- **bibtex_bibfiles**:
<br>
- **repository**:
<br>
- **html**:
<br>
- **sphinx**:

:::

:::{grid-item}
:columns: 6

```yml
title: Tools
author: <strong>Vincent Deguin</strong> (with ❤️)
logo: _static/Logo/logo_SFTP.png

execute:
  execute_notebooks: force

latex:
  latex_documents:
    targetname: book.tex

bibtex_bibfiles:
  - Biblio/reference.bib

repository:
  url: https://github.com/Deugz/nb-tools  # Online location of your book
  path_to_book: _build/html/  # Optional path to your book, relative to the repository root
  branch: main  # Which branch of the repository should be used when creating links (optional)

html:
  favicon                   : "_static/Logo/logo_SFTP.png"  
  use_edit_page_button      : true
  use_repository_button     : true
  use_issues_button         : true
  use_multitoc_numbering    : false
  extra_navbar              : ""
  extra_footer: |
  
    <br><img class="CC_licence" src="https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-nc-sa.svg" alt="Licence CC BY NC SA 2"/> 
     
  home_page_in_navbar       : false
  baseurl                   : "https://deugz.github.io/nb-tools/_build/html/"
  comments:
    hypothesis              : true
    utterances              : 
      repo: "https://github.com/Deugz/nb-tools"
  announcement              : "⚠ Work in Progress  ⚠"

sphinx:
  config:
    language: en
    bibtex_reference_style: author_year
    html_show_copyright: false
  extra_extensions:
  - sphinx_design
  - sphinx.ext.intersphinx

```

:::


::::

:::::

:::::{tab-item} _toc.yml 


:::::

:::::{tab-item} Markdown files (.md)


:::::

:::::{tab-item} Python notebooks (.ipynb)


:::::


:::::{tab-item} .gitignore


:::::

:::::{tab-item} .noJekyll


:::::


::::::
:::::::
::::::::




## The Build Process

### <strong> &#x2023; <u> HTML </u></strong> 

```

jb build bookname

```

::::{div} full-width

```{figure} Docs/2020-10-jb-tech-stack-jupytercon-12m.png
:width: 100%


[Source](https://docs.google.com/presentation/d/1THlclr3BhoywMmseMo8kyH7QVX2ea_Xk-cO2Tl6yiFk/edit#slide=id.g536532a834_0_12)
```

::::


::::::{div} full-width
:::::{dropdown} In Depth Explanation

::::{tab-set}

:::{tab-item} 1. Author

- [Jupytext](https://jupytext.readthedocs.io/en/latest/formats.html#myst-markdown)

:::

:::{tab-item} 2. Cache and execute 

- [Jupyter Cache](https://jupyter-cache.readthedocs.io/en/latest/)

:::

:::{tab-item} 3. Parse to sphinx

- [MYST-NB](https://myst-nb.readthedocs.io/en/latest/)
- [MYST Parser](https://myst-parser.readthedocs.io/en/latest/)

```{note}

Check the difference between the 2

```

:::

:::{tab-item} 4. Build Output

2 options:
- html 
- pdf

:::


:::{tab-item} 5. Sphinx Extensions

- Implement the one I use
- [Sphinx Panels](https://sphinx-panels.readthedocs.io/en/latest/)
    - [Docs](https://pypi.org/project/sphinx-book-theme/)

:::

:::{tab-item} 6. Customization

- [Sphinx book theme](https://github.com/executablebooks/sphinx-book-theme)


:::

:::{tab-item} 7. Controller Process

- [Jupyter Book](https://jupyterbook.org/en/stable/intro.html)


:::



::::
:::::
::::::


### <strong> &#x2023; <u> PDF </u></strong>

- via latex



## Sphinx



# Comments  


***

<br>

:::::::{div} full-width

::::::{grid} 3

:::::{grid-item-card}
:class-header: bg-light
:columns: 5

**Notes**
^^^

<br>

<blockquote class="trello-card">
<a href="https://trello.com/c/9Dqh0lg9/31-jupyter-book">Trello Card</a>
</blockquote>
<script src="https://p.trellocdn.com/embed.min.js"></script>

:::::



:::::{grid-item-card}
:class-header: bg-light
:columns: 4
**Page**
^^^

<br>

- Author:  Vincent Deguin;
- Status:  ![flag alt >](../../_static/Svg_icons/Under_construction.svg)  <span class="hovertext" data-hover="To be Reviewed">🔎</span>
- Reviewed: <span class="hovertext" data-hover="Insert here who has done what">&#x274C;</span>
- Updated: 28/05/2023



   
:::::

:::::{grid-item-card}
:class-header: bg-light
:columns: 3
<span style="float: right">![flag alt >](../../_static/Svg_icons/coins-money-svgrepo-com.svg)</span>**Help** 
^^^

<br>

<script type='text/javascript' src='https://storage.ko-fi.com/cdn/widget/Widget_2.js'></script><script type='text/javascript'>kofiwidget2.init('Buy me a coffee', '#317315', 'O4O6EZO78');kofiwidget2.draw();</script> 

<br>
<br>

or

<br>

![flag alt >](../../_static/Svg_icons/patreon-svgrepo-com.svg) [Patreon](https://www.patreon.com/Science_for_the_People) 

:::::
::::::
:::::::



<script src="https://utteranc.es/client.js"
        repo="Deugz/nb-tools"
        issue-term="pathname"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>


