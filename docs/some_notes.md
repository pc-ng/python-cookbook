---
title: Some notes for Markdown with Materials
description: Nullam urna elit, malesuada eget finibus ut, ac tortor.
hide:
  - toc        # Hide table of contents
---

# Some notes on Markdown

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Adding abbreviations

The HTML specification is maintained by the W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium

## Adding glossary
using snippets to import the glossary from another file.
The HTML specification is maintained by the W3C.

--8<-- "includes/abbreviations.md"


## Admonitions
1. pymdownx.details: adds the collapsible feature. starts with `???` instead of `!!!`
2. pymdownx.superfences: allows for the nesting of code and content blocks inside admonitions

!!! note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

!!! note "Phasellus posuere in sem ut cursus"
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

!!! note ""
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

!!! note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

    ``` python
    def bubble_sort(items):
        for i in range(len(items)):
            for j in range(len(items) - 1 - i):
                if items[j] > items[j + 1]:
                    items[j], items[j + 1] = items[j + 1], items[j]
    ```

    Nunc eu odio eleifend, blandit leo a, volutpat sapien. Phasellus posuere in
    sem ut cursus. Nullam sit amet tincidunt ipsum, sit amet elementum turpis.
    Etiam ipsum quam, mattis in purus vitae, lacinia fermentum enim.


??? note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

???+ note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

#### others:

1. abstract, summary, tldr
2. info, todo
3. tip, hint, important
4. success, check, done
5. question, help, faq 
6. warning, caution, attention 
7. failure, fail, missing
8. danger, error
9. bug
10. example 
11. quote, site 

!!! quote 
    this is a quote 

!!! danger
    very dangerous!



## Image with `attr_list`
![Placeholder](https://dummyimage.com/600x400/eee/aaa){ align=left }



<figure>
  <img src="https://dummyimage.com/600x400/eee/aaa" width="300" />
  <figcaption>Image caption</figcaption>
</figure>


## Ordered lists
1. Vivamus id mi enim. Integer id turpis sapien. Ut condimentum lobortis
  sagittis. Aliquam purus tellus, faucibus eget urna at, iaculis venenatis
  nulla. Vivamus a pharetra leo.

    1. Vivamus venenatis porttitor tortor sit amet rutrum. Pellentesque aliquet
      quam enim, eu volutpat urna rutrum a. Nam vehicula nunc mauris, a
      ultricies libero efficitur sed.

    2. Morbi eget dapibus felis. Vivamus venenatis porttitor tortor sit amet
      rutrum. Pellentesque aliquet quam enim, eu volutpat urna rutrum a.

        1. Mauris dictum mi lacus
        2. Ut sit amet placerat ante
        3. Suspendisse ac eros arcu


## Definition lists
`Lorem ipsum dolor sit amet`
:   Sed sagittis eleifend rutrum. Donec vitae suscipit est. Nullam tempus
    tellus non sem sollicitudin, quis rutrum leo facilisis.

`Cras arcu libero`
:   Aliquam metus eros, pretium sed nulla venenatis, faucibus auctor ex. Proin
    ut eros sed sapien ullamcorper consequat. Nunc ligula ante.

    Duis mollis est eget nibh volutpat, fermentum aliquet dui mollis.
    Nam vulputate tincidunt fringilla.
    Nullam dignissim ultrices urna non auctor.

## Tasklists
- [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
- [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [ ] Praesent sed risus massa
- [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque



## Math with MathJax
$$
\operatorname{ker} f=\{g\in G:f(g)=e_{H}\}{\mbox{.}}
$$


The homomorphism $f$ is injective if and only if its kernel is only the 
singleton set $e_G$, because otherwise $\exists a,b\in G$ with $a\neq b$ such 
that $f(a)=f(b)$.

