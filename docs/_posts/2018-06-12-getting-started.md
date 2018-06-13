---
layout: default
title: Getting Started with Markdown and Git
---

## Getting Started with Markdown and Git ##

0. Preliminary Setup

    - Created a repository on Github
    - Added a docs directory with an index.md file
    - Turned on GitHub Pages and configured theme in settings
    - Added a \_post directory and added post list to index page

    ```
    {% for post in site.posts %}
    ## [{{ post.title }}]({{ post.url | relative_url }})  
    {{ post.date | date_to_long_string }}  
    {{ post.excerpt | strip_html | truncatewords: 50 }}
    {% endfor %}
    ```

1. Create a [GitHub](https://github.com) account
2. Accept invite as contributor to repository
3. [Edit a file](https://help.github.com/articles/editing-files-in-your-repository/) and commit changes

    - See [Mastering Markdown](https://guides.github.com/features/mastering-markdown/) for the basics on using GitHub Flavored Markdown (GFM).
    - For a fuller explication of the GFM standard, see [GitHub Flavored Markdown Spec](https://github.github.com/gfm/).
    - Markdown can be used in the .md file we are working on together and in the commit message.
    - There are many git workflows that teams can use, here is a [simple introduction](http://rogerdudler.github.io/git-guide/) that gives the basics of the git process.
4. [Add a new file](https://help.github.com/articles/adding-a-file-to-a-repository/) to the repository.

    - browse to docs directory of repository
    - create file with .md extension
    - add necessary front matter (see example in another file, e.g. layout and title)

5. [Add an issue](https://help.github.com/articles/creating-an-issue/) that the team needs to discuss about the project.

    - notice all of the options you have with assigning issues or categorizing, etc.
    - you can use markdown in your issue too :)

6. Choose an editor (e.g. [Atom](https://atom.io/))

    - Install Atom
    - [Setup Atom for Github](https://www.hongkiat.com/blog/manage-git-github-atom/)
    - Learn the git workflow in Atom (team decide on branching or not, etc.)
    - commit and push changes to shared repository

7. Use [pandoc](https://pandoc.org/) to convert markdown to word

    - Mac OS: install [Homebrew](https://brew.sh/) package manager
    - [Install pandoc](https://pandoc.org/installing.html) (Use homebrew for Mac OS)
    - use command something like

            pandoc -o [output_docx] -f markdown+smart -t docx [input_md]

8. A helpful walk-through on writing with Markdown and Pandoc: [Sustainable Authorship in Plain Text using Pandoc and Markdown](https://programminghistorian.org/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown)

9. Integrate with Zotero for bibligraphic management

    - [Install Zotero](https://www.zotero.org/)
    - Configure more readable citekeys with [Better BibTeX](https://retorque.re/zotero-better-bibtex/installation/)
    - See nice [Markdown/Pandoc/Zotero tutorial](http://raphaelkabo.com/blog/posts/markdown-to-word) by [Raphael Kabo](https://raphaelkabo.com/)
