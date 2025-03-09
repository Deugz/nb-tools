# Markdown

## What is it

> Definition

### <strong> &#x2023; <u> Creators </u></strong>

developped by [John Gruber](https://daringfireball.net/projects/markdown/) and [Aaron Swartz](https://fr.wikipedia.org/wiki/Aaron_Swartz)



***
**Documentation**:
- Markdown
- Jupyter Book

**Dedicated tutorial**

- [Page layout](https://jupyterbook.org/en/stable/content/layout.html)


***

### <strong> &#x2023; <u> Why you should use it</u></strong>

- Simple
- Transposable

## A quick guided tour

```{note}

- Insert presentation like tour

```

## The page layout

- How to navigate this web-site

left menue = global
right menu = local


## Legend

### Links

We are all familiar withe the ![flag alt >](../../Docs/Svg_icons/external-link-alt-svgrepo-com.svg) icon

- ![flag alt >](../../Docs/Svg_icons/links/I_link.png) - **Internal link**: same web-site but different page
- ![flag alt >](../../Docs/Svg_icons/links/E_link.png) - **External link**: different web-site, *Wikipedia* for example
- ![flag alt >](../../Docs/Svg_icons/links/IE_link.png) - **Internal-External**: different web-site, but still one of mine, those could be:
    - Teaching
    - Thesis.A
    - Thesis.B

```{margin}

2 main methods:
- [badgen](https://badgen.net/)
- [shield](https://shields.io/)

also possible with sphinx

- [Sphinx-doc](https://sphinx-design.readthedocs.io/en/latest/badges_buttons.html#icons)


```

### Buttons

Markdown give you the possibility to generate buttons. They are a more informative version of the links presented above. I use on this web-site the following buttons:

- DOI
- Binder
- Link towards book (Teaching)

```{note}

Insert examples

```

## Comments

[/----------------------------------------------------------------------------------------------------------------------------------------------------------------------- Is it a comment ?/]: # 


Implement comments on top of big title to have a clear view of page subdivision (usefull when coding with vs code and having very long md files)



## Titles


## Images / figures


```{image} ../../Docs/Images/JWST_cloud1.jpg 
```
    
```{figure} ../../Docs/Images/JWST_cloud1.jpg
:name: JWST2
James Web Space Telescope [JWST](https://deugz.github.io/nb-teaching/_build/html/Bitesize/Astronomy/JWST/JWST.html)
```

## Tables


## Notes

Explain what notes correspond to what (proper admonition)



```{note}
:class: dropdown
The note body will be hidden!
```

```{warning}
- Copy notes from PhD
```

:::{tip}
This text is **standard** _Markdown_
:::

## Grid

put example

### with adaptable column width

::::{grid}

:::{grid-item}
:outline:
:columns: 3
A
:::
:::{grid-item}
:outline:
:columns: 9
B
:::
:::{grid-item}
:outline:
:columns: 6
C
:::
:::{grid-item}
:outline:
:columns: 6
D
:::

::::


### Multiple row

:::::{div} full-width
::::{grid} 1 1 2 3
:class-container: text-center
:gutter: 3


:::{grid-item-card}
:class-header: bg-light

:::

:::{grid-item-card}
:class-header: bg-light

:::

:::{grid-item-card}
:class-header: bg-light

:::

:::{grid-item-card}
:class-header: bg-light

:::

:::{grid-item-card}
:class-header: bg-light

:::

:::{grid-item-card}
:class-header: bg-light

:::

::::
:::::

### Full width content

:::::{div} full-width

:::::


<h3><strong>&#187;  <u>Formatting </u></strong></h3>

formatting is mood dependant and likely to change.

<h4>Maths</h4>

Different methods to write equation, bith can be referred in the following equation list

<h5>Method 1</h5>

$$
  \int_0^\infty \frac{x^3}{e^x-1}\,dx = \frac{\pi^4}{15}
$$

<h5>Method 2</h5>

```{math}
:label: my_label
w_{t+1} = (1 + r_{t+1}) s(w_t) + y_{t+1}
```

### Tabs

can be embeded in dropdown

- [Sphinx-doc](https://sphinx-design.readthedocs.io/en/latest/tabs.html#tab-set-options)

### Dropdown

- [Sphinx-doc](https://sphinx-design.readthedocs.io/en/latest/dropdowns.html)

## HTML Symbol

### Orga

::::{grid} 2

:::{grid-item}

- &#9989; - &#9989 -  ticked box
- &#x274C; - &#x274C - red cross
- &#x2192; - right arrow:
- &#127992; - magnifying glass
- &#128143; - Lovely couple
- &#128142; - Diamond
- &#128293; - Fire

- &#10024; - &#10024 - Stars

- &#128064; - &#128064 - Eyes

- &#128165; - Explosion

- &#128640; - &#128640 - Rocket 

- &#x26D4; - &#x26D4 - panneau stop

- &#129482; - &#129482 - Ice cube
    - &#x1F9CA; - &#x1F9CA - Ice cube 2
 
 
:::

:::{grid-item}

**PhD**

- 1

:::

::::

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
<a href="https://trello.com/c/HYO8arP5/29-markdown">Trello Card</a>
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






