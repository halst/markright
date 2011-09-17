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

~~~~~~~
                                              ==================================
                                              Title or Headline 1, Right-aligned
                                                 with top and bottom underlining
                                              ==================================



=================================
Title or Headline 1, Left-aligned
with top and bottom underlining
=================================

                    =================================
                      Title or Headline 1, Centered
                     with top and bottom underlining
                    =================================
                                                                    
Title or Headline 1, Left-aligned with bottom underlining
=========================================================

            Title or Headline 1, Centered with bottom underlining
            =====================================================
            
                      Title or Headline 1, Right-aligned with bottom underlining
                      ==========================================================
                      
Headline 2, Left-aligned with bottom underlining
-------------------------------------------

            Headline 2, Centered with bottom underlining
            -------------------------------------------
            
                               Headline 2, Right-aligned with bottom underlining
                      ----------------------------------------------------------
                      
### Headline 3, left

                        ### Headline 3, center ##
                        
                                                      ### Headline 3, right  ###

#### Headline 4 inside a paragraph #######
Paragraph text, paragraph text. Paragraph text, paragraph text. Paragraph text, paragraph text. Paragraph text, paragraph text. Paragraph text, paragraph text. 
                        
Paragraph text left word-wrap, paragraph text left word-wrap,  paragraph text left word-wrap, paragraph text left word-wrap, paragraph text left word-wrap, paragraph text left word-wrap, paragraph text left word-wrap, paragraph text left word-wrap, paragraph text left word-wrap, paragraph text left word-wrap.

________________________________________________________________________________


Paragraph text left no-word-wrap, paragraph text left no-word-wrap, paragraph 
text left no-word-wrap, paragraph text left no-word-wrap, paragraph text left 
no-word-wrap, paragraph text left no-word-wrap, paragraph text left 
no-word-wrap, paragraph text left no-word-wrap.

Paragraph text left no-word-wrap with intentional line breaks.
Paragraph text left no-word-wrap with.
Paragraph text left no-word-wrap with intentional.
Paragraph text left no-word-wrap with intentional line breaks.

                                * * *
                       # Centered Headline 1 #
                Centered text, centered text, centered text, 
                        centered text, centered text, 
                    centered text, centered text, centered 
        text, centered text, centered text, centered text, centered text, 
                                centered text.
                                
                    Right-aligned text, right-aligned text,  right-aligned text,
                                        right-aligned text,  right-aligned text,
             ight-aligned text,  right-aligned text,  right-aligned text,  right
                                                                   aligned text.

Lorem ipsum dolor sit amet, consectetur adipisicing *italics*, sed do eiusmod tempor incididunt *italia* ut labore et dolore 3*3=9 magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco 2*2=4 laboris nisi ut aliquip ex ea commodo consequat *italics*. Duis aute **bold** irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est **bold old dold**.

      *Often epigraphs are written in italics and right-aligned, and they occupy
                                                                 several lines.*
                                                                   -- Epigrapher

       *"Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, 
                          consectetur, adipisci velit..."
    "There is no one who loves plain text itself, who seeks after it and 
                wants to have it, simply because it is plain..."*

[Lorem ipsum][http://www.lipsum.com/] dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation google [google.com] ullamco laboris nisi ut aliquip ex ea commodo consequat[link consequat.com]. Duis aute irure dolor in reprehenderit in voluptate 
[http://www.google.dk/search?sourceid=chrome&ie=UTF-8&q=voluptate] velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Inline image, inline image, inline image, inline image, inline image, [http://www.x-vinder.dk/sites/all/modules/contrib/smileys/packs/Roving/smile.png]
inline image, inline image, inline image.

[http://www.iconeasy.com/icon/thumbnails/Emoticon/IconTexto%20Emoticons/Smile%20Face%20Icon.jpg]

        [http://icons.iconseeker.com/png/128/vista-halloween/smile-2.png]
        
               [http://icons.iconseeker.com/png/128/vista-halloween/smile-2.png]

    Paragraph One Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    Totally different paragraph Lorem ipsum dolor sit amet, consectetur 
adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna 
aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi
ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Lorem ipsum dolor st dolore magna aliqua. Ut enim ad minim veniam, quis nostrud <span id="inline_html"> blah </span>exercitation ullamco laboris nisi ut aliquip ex ea commodo dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

<table border="1">
<tr>
<td>row 1, *cell 1*</td>
<td>row 1, **cell 2**</td>
</tr>
<tr>
<td>row 2, cell[link cell.com] 1</td>
<td>row 2, cell 2</td>
</tr>
</table>

[http://www.youtube.com/watch?v=c211yCCZdJY]

            [video http://www.youtube.com/watch?v=c211yCCZdJY]
            
         [http://www.youtube.com/watch?v=OeV_3EhXgos&feature=feedrec_grec_index]








~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~









