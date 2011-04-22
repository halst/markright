MarkRight: MarkUp similar to MarkDown
==============================

## Simplified links

One-word links:

    This is an example [http://example.com/]

> This is an [example](http://example.com/)

Multi-word links:

    This is [an example] [http://example.com/]

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

***

    <center><h1>Title</h1> 
    by Foo Bar</center>

## Footnotes linking

    ...pointed out in [Dijkstra68].
    For more info see [Dijkstra68].

    [Dijkstra68] A Case against the GO TO Statement by Edsger W.Dijkstra

***

    ...pointed out in <a href="#Dijkstra68">Dijkstra68</a>.
    For more info see <a href="#Dijkstra68">Dijkstra68</a>.
   
    <p id="Dijkstra68">[Dijkstra68] A Case against the GO TO Statement by Edsger W.Dijkstra</p>

## Header linking

Is kinda the opposite of footnotes linking.

    Header
    ======
    ...
    Go back to that header [Header].

***

    <h1 id="Header">Header</h1>
    ...
    <p>Go back to that <a href="#Header">header</a>.
 
## Automatic table of contents

    [table of contents]

## Use features of [git flavored markdown](https://github.com/blog/832-rolling-out-the-redcarpet)? 
 - newlines
 - multiple underscores in words
 - url autolinking
 - fenced code blocks
 - syntax highlighting

## Todo-lists

    [+] Brainstorm about features
    [-] Implement in Python

***

    <p class='done'>Brainstorm about features</p>
    <p class='undone'>Implement in Python</p>

## 'Papers'

    /------------------------------\
    Some text
    \------------------------------/

***

    <div class='paper'>
    Some text
    </div>

## In-document indentation

Indentation with 4 spaces will not yield code-block, but a list with no visible bullets.

        Apples
        Pears
        Bananas

***

    <ul class="no_bullet">
    <li>Apples</li>
    <li>Pears</li>
    <li>Bananas</li>
    </ul>

## Some table syntax, maybe?

## Some smatry-pants, maybe?