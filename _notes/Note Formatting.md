---
theme: Getting Started
---

## Front Matter
At the top of each new note, you must include the triple dashes that make up [Jekyll Front Matter](https://jekyllrb.com/docs/front-matter/).

````js
---
---
````

## Note Title
The title of the `.md` file will automatically become the note title heading, rendered as an `<h1>`. Keeping this in mind, start your note content from `<h2>` or `##`.

### Title Override
Use variable `title:` in the front matter to create a note title that is different from the filename. 

```js
---
title: A note about cats
---
```

In the example above, the filename is `cats.md` but the longer title shows up in the note's heading and `<title>`. See it live at [[cats]].

## Themes (aka Categories)
On the [[archive]] page, I've set it to automatically display all notes and their themes (if any). Think of a theme like a category without the chronological blog connotation. Inspired by [Low Tech Mag's Archive Page](https://solar.lowtechmagazine.com/archives.html).

Themes will also display underneath note title, if they are not null. Eventually I want to make a theme page to view all notes with common themes.

## Internal Links
By default, all links created with `<a>` will show up as external links, open in new window, and display a small arrow.

For internal links, either add `class="internal-link"` to the HTML or add `{: .internal-link}` after a Markdown link like this:

```[Markdown Link](/cats){: .internal-link}```

## Github Flavored Markdown
This site uses [Commonmark Github Flavored Markdown](https://github.com/github/jekyll-commonmark-ghpages), which replaces the default Kramdown functionality. Read the [Github Markdown Documentation](https://github.github.com/gfm/).

Most importantly, you can create tables that are compatible with Obsidian and Github:

| foo | bar |
| --- | --- |
| baz | bim |

The table above was created with this markup:
`````js
| foo | bar |
| --- | --- |
| baz | bim |
`````

More info in the [GFM Documentation](https://github.github.com/gfm/#tables-extension-)

Other options you can add to Commonmark in `_config.yml`:

```js
Valid options: DEFAULT, VALIDATE_UTF8, SMART, LIBERAL_HTML_TAG, FOOTNOTES, STRIKETHROUGH_DOUBLE_TILDE, SOURCEPOS, HARDBREAKS, SAFE, NOBREAKS, GITHUB_PRE_LANG, TABLE_PREFER_STYLE_ATTRIBUTES, FULL_INFO_STRING
```

Note that a code block created with ` `` ` has text wrapping, while ` ``` ` does not.

Description of each option [here](https://github.com/gjtorikian/commonmarker#options)

## Typographic Symbols
"Smart" quotes are automatically generated with Commonmark, but the typographic options are documented in [Kramdown](https://kramdown.gettalong.org/syntax.html#typographic-symbols), the built in Jekyll Markdown parser.

-   `---` will become an em-dash (like this —)
-   `--` will become an en-dash (like this –)
-   `...` will become an ellipsis (like this …)
-   `<<` will become a left guillemet (like this «) – an optional following space will become a non-breakable space
-   `>>` will become a right guillemet (like this ») – an optional leading space will become a non-breakable space