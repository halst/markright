MarkRight
=======
Markdown extensions I'm thinking of for personal projects.

## Simplified links

One-word links:

    This is an example [http://example.com/]

should turn into

> This is an [example](http://example.com/)

Multi-word links:

    This is [an example] [http://example.com/]

should turn into

> This is [an example](http://example.com/)

## Simplified images

    [image http://example.com/image.png]

should turn into an image.

## Simplified embedded objects

Commonly used embedded objects, like YouTube videos and Google Maps could also be auto-embedded:

    [youtube http://www.youtube.com/watch?v=P0zWopVbW4k]
    [map http://maps.google.com/?ie=UTF8&ll=54.876607,15.117188&spn=34.745161,58.886719&t=h&z=4]

## Centered text

Everything that starts with 8 spaces or more should be centered:

                                   Title                               
                                   =====
                                by Foo Bar

should turn into

    <center><h1>Title</h1> 
    by Foo Bar</center>

## Use features of [git flavored markdown](https://github.com/blog/832-rolling-out-the-redcarpet)? 
 - newlines
 - multiple underscores in words
 - url autolinking
 - fenced code blocks
 - syntax highlighting

## 'Papers'

    /------------------------------\
    Some text
    \------------------------------/

will turn into

    <div class='paper'>
    Some text
    </div>

## In-document indentation

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

## Some table syntax, maybe?