# Readme for liv810.github.io

## File Structure
liv810.github.io/
 - **_data/**           .yml files that outline the list items and displaycards to render within a section.
                        One .yml file per section.
 - **_layouts/**        Layouts for .md-generated files.
 - **_plugins/**        Is this necessary????
 - **_site/**           Auto-generated by Jekyll upon "jekyll build" (or "jekyll serve"). The version of the site that is served.
 - **css/**             CSS files, one for the homepage, one for the Wunderlist-based files.
 - **images/**          All images and icons go here.
 - **&ast;.md**         Files from which .html files are auto-generated. They refer to which _layout they're based on and that's basically it.
                        There probably exists a more elegant way to not have to write one of these per file...

## Libraries
- mmenu             Jquery-based menu plugin.
- maphilight        Colors image-map regions when hovered over, on the homepage.


## How mmenu works (within the context of my page)
http://mmenu.frebsite.nl/
- Sidebar is a "widescreen" menu that is always expanded (unless the window is too small).
- Displaycards are menus that appear when list items, which are hrefs to displaycards, are clicked.
  Clicking on a list item (e.g. href="#1") then triggers to reveal the displaycard (whose HTML and javascript have been pre-written).

## mmenu oddities
- Version 7.0.0 & 7.2.2 (and presumably everything in between)
	- "offCanvas": {"position": "right"} not work
	- have to include positioning CSS and "extensions": ["position-right"] instead
		- but positioning is "incompatible with" sidebar extension (http://mmenu.frebsite.nl/documentation/extensions/positioning.html)

## Term definitions (try to keep consistent in the code).
- *Sidebar*
  Refers to the left sidebar that should (basically) be always present and allows the user to select which list to view.
- *List item*
  Refers to an item within a list, as rendered in a white rectangle in the main div of the page.
- *Displaycard*
  Refers to the right sidebar that contains the details about a list item.
