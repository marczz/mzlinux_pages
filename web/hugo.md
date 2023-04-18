---
title: Hugo
---
<!--
[[file:../../../../content-org/notes/web_notes/hugo_notes.org][Hugo notes]]
-->

[Hugo](https://gohugo.io/) is a static site generator written in go. It is in
Debian. Hugo can be used for documentation.

It uses since v 0.60 {{< iref "markdown#goldmark" "Goldmark" >}} for markdown
formatting, and {{< iref "source_code#chroma" Chroma >}} for
[syntax highlighting](https://gohugo.io/content-management/syntax-highlighting/).

    # Hugo documentation

-   [Hugo Documentation](https://gohugo.io/documentation/)


# Hugo Themes for Documentation.

There are many themes aimed to Documentation, you can find many in
[Hugo Themes tagged documentation](https://themes.gohugo.io/tags/docs/).

I list some of them with a side bar menu, to alow a hierarchical documentation organized
as a book.


You can use a dynamic search function to your static Hugo blog,
The options are described in
[Search for your Hugo Website | Hugo](https://gohugo.io/tools/search/).

This includes:
-   [hugo-lunr - npm](https://www.npmjs.com/package/hugo-lunr)
    generate {{< iref "static_sites#lunr" "lunr.js" >}} index files from an Hugo site.
-   [hugo-lyra](https://github.com/paolomainardi/hugo-lyra)
    A typescript module for creating LyraSearch _now renamed
    {{<iref "content_management#orama" "orama" >}}_ indexes for static Hugo sites,
    it comes with server and client libraries.
-   [Guide to setup a Bonsai search in Hugo](https://docs.bonsai.io/article/105-hugo)
    uses the commercial hosted search engines
    {{< iref "content_management#bonsai" "Bonsai" >}},
-   [PageFind Quickstart](https://pagefind.app/docs/) is an example of indexing an Hugo
    site with {{< iref "static_sites#pagefind" "PageFind" >}}, you can then include in
    your layout the [default ui](https://pagefind.app/docs/ui/) or a custom UI.

These also have also a search _usually with lunr_ integrated.
-   [DocDock](https://docdock.netlify.com/original/) (MIT license),
    [GitHub - docdock](https://github.com/vjeantet/hugo-theme-docdock)
    is a 2017 fork of [learn theme](https://github.com/matcornic/hugo-theme-learn)
    but it has diverged from learn since the fork.
-   [hugo-book](https://github.com/alex-shpak/hugo-book) (MIT license)
    -   [Hugo Book demo](https://hugo-book-demo.netlify.app/).
-   [docuapi](https://github.com/bep/docuapi) (Apache License)
    is targeted to API documentation.
-   [relearn](https://github.com/McShelby/hugo-theme-relearn)  (MIT license)
    is a 2020 fork of [learn theme](https://github.com/matcornic/hugo-theme-learn)
    it tries to be a drop-in replacement for the Learn theme.

    Relearn include a configurable lunr search.
-   [hugo-theme-techdoc](https://github.com/thingsym/hugo-theme-techdoc) (MIT license)
    has a search shortcode powered by {{< iref "static_sites#algolia" "Algolia" >}}.

Examples of Documentation build with Hugo:

-   [GetBoostrap](https://getbootstrap.com/) the documentation of
    {{< iref "html#bootstrap" "BootStrap" >}}: [Get bootstap source
    ](https://github.com/twbs/bootstrap/tree/master/site).
-   [BookStackApp](https://github.com/BookStackApp/website)
    has adapted for documentation
    [Casper for Hugo](https://github.com/vjeantet/hugo-theme-casper)
    is a single-column theme for Hugo _last commit 2018_

-   [Riak Docs](http://docs.basho.com/) is built with Hugo,
    [The source is on GitHub](https://github.com/basho/basho_docs).
-   [Docs.balsamiq.com](https://blog.balsamiq.com/new-documentation-site/).
-   [BookStackApp documentation](https://www.bookstackapp.com/docs/),
    [GitHub - BookStackApp](https://github.com/BookStackApp/website).

Building doc with Hugo:

-   [ox-hugo](https://ox-hugo.scripter.co) export an org file to hugo markdown.
-   [How We Rebuilt Our Documentation Using Hugo | Presslabs
    ](https://www.presslabs.com/how-to/documentation-hugo/)
-   [hugo-academic](https://github.com/gcushen/hugo-academic)
    [wowchemy](https://github.com/wowchemy/wowchemy-hugo-themes)
    website builder for Hugo
-   [Better Hugo/AsciiDoc HTML](http://ratfactor.com/hugo-adoc-html5s/).

Switching from Nikola to Hugo:

-   [Moving from Nikola to Hugo · What I learnt this week
    ](https://learnings.desipenguin.com/posts/migrating-to-hugo/)
-   [Moving from Nikola to Hugo - serialized.net
    ](https://serialized.net/2017/06/moving-from-nikola-to-hugo/)
-   [Nikola to Hugo python script
    ](https://gist.github.com/punchagan/025b0fbf032dc20d0b36d35ec7bf5339)


# Hugo development
## Hugo development blogs

-   [posts tagged Hugo | Nelis Oostens](http://oostens.me/posts/hugo/).

## Using icons in Hugo
-   [inline svg icons | Nelis Oostens
    ](http://oostens.me/posts/hugo-resources-inline-svg-icons/)..
-   [Using Font Awesome Icons in Hugo | Nick Galbreath
    ](https://www.client9.com/using-font-awesome-icons-in-hugo/).
-   [Font Awesome in Hugo - I am Matze](https://matze.rocks/posts/fontawesome_in_hugo/).

Emojis can be used also in Hugo either.

## Math in hugo
-   [Math Typesetting in Hugo | Mert Bakır
    ](https://mertbakir.gitlab.io/hugo/math-typesetting-in-hugo/)
    use [Katex](https://katex.org/).
-   [Hugo - MathJax Support
    ](https://bwaycer.github.io/hugo_tutorial.hugo/tutorials/mathjax/)
    uses [MathJax](https://www.mathjax.org/). _tutorial from a previous release of Hugo._
-   [Getting Mathjax to Work With Hug
    ](https://janert.me/blog/2021/getting-mathjax-to-work-with-hugo/)
-   [Render LaTeX math expressions in Hugo with MathJax 3 · Geoff Ruddock
    ](https://geoffruddock.com/math-typesetting-in-hugo/).
-   [How to use Mathjax in Hugo | Peter V. Mørch's Blog
    ](https://www.morch.com/posts/2021-07-24-mathjax-in-hugo/).


## Building Hugo site with CI
-   [Beautiful Hugo](https://pages.gitlab.io/hugo/)
    Hugo Blog Template for GitLab Pages

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
