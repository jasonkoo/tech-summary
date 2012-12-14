# Block Elements

## Headers
Use 1-6 hash characters at the start of the line, corresponding to header levels 1-6. For example:

    # This is an H1
    ## This is an H2
    ###### This is an H6

## Blockquotes
Markdown uses > characters for blockquoting. Just put the > character at the beginning of each line you need to quote. For example:

    >This is a quote line.
    >This is anothoer quote line.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

## Lists
Markdown supports ordered and unorder lists.

Unordered lists use asterisks(*), pluses(+), or hyphens(-) interchangably as list markers. For example:

    * Red
    * Green
    * Blue

Ordered lists use numbers followed by periods.

    1. Bird
    2. McHale
    3. Parish

## Code blocks
Markdown converts text with four spaces at the front of each line to code blocks. Github flavored markdown(GFM) supports that, but it also supports fenced blocks. Just wrap your code blocks in ``` and you won't need to indent manually to trigger a code block.

GFM adds syntax highlighting if you request it. In your fenced block, add an optional language identifier and GFM will run it through syntax highlighting. For example, to syntax highlight Ruby code:

    ```ruby
    require 'redcarpet'
    markdown = Redcarpet.new("Hello World!")
    puts markdown.to_html
    ```
## Horizontal rules
You can produce a horizontal rule tag (<hr />) by placing three or more hyphens, asterisks, or underscores on a line by themselves. 


# Span Elements

## Links
Markdown supports two style of links: inline and reference.

Inline link

    This is [an example](http://example.com/ "Title") inline link.
    [This link](http://example.net/) has no title attribute.

will produce

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>
    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

Reference link

    This is [an example][id] reference-style link.

Then, anywhere in the document, you define your link label like this, on a line by itself:

    [id]: http://example.com/  "Optional Title Here"


# Miscellaneous
