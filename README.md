MarkRight
=======
Markdown extension for personal projects


###General features

### Simplified one-word links

While `This is [an example](http://example.com/)` should still yield 'This is [an example](http://example.com/)',
I suggest to have a shortcut for one-word links, i.e.:

    This is an example (http://example.com/)

will turn into

> This is an [example](http://example.com/)

### Centered text

Every line that starts with 8 spaces or more should be centered:

                                   Title                               
                                   =====
                                by Foo Bar

will turn into

    <center><h1>Title</h1> 
    by Foo Bar</center>

### Use features of [git flavored markdown](https://github.com/blog/832-rolling-out-the-redcarpet)? 
 - newlines
 - multiple underscores in words
 - url autolinking
 - fenced code blocks
 - syntax highlighting

## Very specific features

### Auto-embedding youtube videos

    http://www.youtube.com/watch?v=gj8QmRQtVao

will turn into pre-formated embedded video.

### 'Papers'

    /------------------------------\
    Some text
    \------------------------------/

will turn into

    <div class='paper'>
    Some text
    </div>

### In-document indentation

Indentation with 4 spaces will not yield code-block, but a list with no visible bullets.

        Apples
        Pears
        Bananas

will turn into

    <ul class="no_bullet">
    <li>Apples</li>
    <li>Pears</li>
    <li>Bananas</li>
    </ul>

### Some table syntax, maybe?