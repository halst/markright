MarkUpRight - MarkUp similar to MarkDown
========================================

## Simplified links

### One-word links:

    This is an example [http://example.com/]

> This is an [example](http://example.com/)

### Multi-word links:

    This is [an example] [http://example.com/]

> This is [an example](http://example.com/)

#### Variation for compatability with markdown:

    This is [an example](http://example.com/)

> This is [an example](http://example.com/)

### Autolinking (unlike standard markdown):

    This is an example: http://example.com/

> This is an example: <http://example.com/>

#### Variation for compatability with markdown:

    This is an example: <http://example.com/>

> This is an example: <http://example.com/>

### Emphasis

    *italics*  **bold**

I think that `_italic_` and `__bold__` variation is more confusing than useful.

## Horizontal rules

Three or more asterics (or dashes?) on a single line.

## Images

    [image http://example.com/image.png]

should turn into an image.

## Image as a link

    [image http://example.com/image.png] [link http://example.com/]

## Video

### Youtube/Vimeo/etc.

    [video http://www.youtube.com/watch?v=RTb6S31Vf68]

should turn into embedded player.

### Video-files

    [video http://example.com/video.mp4]

should turn into HTML5 video.

## Maps

    [map http://maps.google.com/maps?q=S%C3%B8nderborg,+Denmark&hl=en&ie=UTF8&sll=54.913725,9.792252&sspn=0.278256,0.455246&vpsrc=0&t=h&z=10]

should turn into embedded map.

## Centered text

Every block of text, visualy centered, should turn into centered block.
(TODO resolve ambiguity)

                                   Title                               
                                   =====
                                by Foo Bar

* * *

    <center><h1>Title</h1> 
    by Foo Bar</center>

## Page brakes (useful for slides and titel pages)

Line of 3 or more underscores should turn into page brake (when viewed with pagination or for printed version). Example:

    ___________________________________________________________________

                  This page is intentionaly left blanc.
    ___________________________________________________________________



## May-be features

### Footnotes linking

    This project has high SIL [footnote SIL].

    [footnote SIL] SIL - Safety integrity level. 

* * *

    This project has high SIL<a href="#SIL"><sup>1</sup></a>.
   
    <span name="SIL"><sup>1</sup></span> SIL - Safety integrity level. 

### Reference linking

    ...pointed out in [Dijkstra68].
    For more info see [Dijkstra68].

    [Dijkstra68] A Case against the GO TO Statement by 
                 Edsger W.Dijkstra

* * *

    ...pointed out in [<a href="#Dijkstra68">Dijkstra68</a>].
    For more info see [<a href="#Dijkstra68">Dijkstra68</a>].
   
    <span name="Dijkstra68">[Dijkstra68]</span> A Case against the GO TO Statement by Edsger W.Dijkstra

### Header linking

Is kind of the opposite of footnotes linking.

    Chapter X
    =========
    ...
    As we discussed in previous chapter [header Chapter X].

***

    <h1 name="Chapter X">Chapter X</h1>
    ...
    As we discussed in previous <a href="#Chapter X">chapter</a>.
 
### Use features of [git flavored markdown](https://github.com/blog/832-rolling-out-the-redcarpet)? 
 - newlines
 - fenced code blocks
 - syntax highlighting

### Todo-lists

    [+] Brainstorm about features
    [-] Implement in Python

* * *

    <p class='done'>Brainstorm about features</p>
    <p class='undone'>Implement in Python</p>

### Notes, warnings, etc?

    [i] Some info here
    [!] Warning, Important!
    [Note] Note that this is a note
    [NB] Note that this is a note

## 'Papers'

    /------------------------------\
    Some text
    \------------------------------/

* * *

    <div class='paper'>
    Some text
    </div>

### In-document indentation

Indentation with 4 spaces will not yield code-block, but a list with no visible bullets.

        Apples
        Pears
        Bananas

* * *

    <ul class="no_bullet">
    <li>Apples</li>
    <li>Pears</li>
    <li>Bananas</li>
    </ul>

### Table of contentx, somehow?

### Some table syntax, maybe?

### Some smatry-pants, maybe?
