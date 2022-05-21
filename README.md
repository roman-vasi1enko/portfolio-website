# My Portfolio Page

Portfolio Page including links to my projects and ways to get in touch with me.

**Link to project:** https://roman.vasilenko.co/

![Roman's Portfolio Page Preview](https://github.com/roman-vasi1enko/roman-vasi1enko/raw/main/assets/romanvasilenkoco2.gif)

## How It's Made:

**Tech used:** HTML, CSS, JavaScript

The page combines a robust side-scrolling framework (with various "scroll-assist" features like drag/momentum scrolling, keyboard shortcuts, etc.) with a unique look and feel, a lightbox gallery, and, of course, full responsiveness.

## Optimizations

1. The vertical scrolling on the Apple touchpad works quirky, so it needs some attention next time.
2. While the page is responsive on mobile, some of the sections' design doesn't look perfect.
    - For example, change the size and position of my picture, add spacing to each project section, etc.

## Lessons Learned

Browsers deal with side-scrolling pages differently to vertically-oriented ones in that they require elements (or at the very least, the top-most wrapper element) to have a defined (fixed) width. This leads to several limitations (e.g., the page won't automatically grow/shrink in the same way a vertically-oriented one will). Here are the solutions:

- The entire page is made up of "panel" elements, each of which can be assigned an optional "size" modifier (satisfying the fixed width requirement).

- For panels that don't use a size modifier, individual containing elements *inside* them (eg. a column) can be assigned a "span" modifier to give those a fixed width instead (also satisfying the fixed width requirement).

Another fun quirk of side-scrolling pages is how to actually implement horizontal scrolling *without* resorting to using the (usually ugly) horizontal scrollbar. Here's how to do it in 4 ways:

- *Dragging:* Users can simply click and drag the page left or right to scroll it around. This works exactly as you'd expect, and even has a nice "post-scroll momentum" effect.
- *Scroll Wheel:* modify the scroll wheel's behavior to translate vertical
scrolling into horizontal scrolling, allowing the user to use either the scroll wheel
or trackpad to scroll the page (the latter of which retains the ability to horziontally scroll as normal, so nothing changes there).
  - Special thanks to @miorel + @pieterv of Facebook for "normalizeWheel()" :)
- *Scroll Zones:* Users can hover the mouse cursor on the left or right edges of the page
to automatically scroll in either direction.
- *Keyboard Shortcuts:* Finally, users can simply use the left/right arrows, page up/down,
home/end, and the spacebar to scroll the page.
