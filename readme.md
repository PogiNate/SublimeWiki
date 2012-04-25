Sublime Wiki
------------
A simple way to maintain a personal wiki in Sublime Text 2. 

This extension isn't designed to replace wikipedia, or even go on the web at all. This is a flat-file, no-nesting, no-nonsense system designed purely to give you (well, me) a place to catch fleeting thoughts and turn them into something useful. To keep it as fiddle-proof as possible, the list of features is intentionally kept very small.

In other words, It's job is to let you maintain a *personal* wiki without spending too much time on it. 
##How It Works
1. Create a directory where you want to keep all your files. I recommend setting this up in [DropBox](http://db.tt/WW19iU5) or some similar service so it auto-syncs across your computers.
2. Create a file with a name like `MainIndex.sublime-wiki` in that directory. The name isn't important, the extension is. Write some stuff in that file, and make sure to put in some `WikiWords`.
3. Any `WikiWords` (i.e. UpperCamelCase) will be converted to internal links.
   * By default, `Ctrl+F11` is the keystroke to folow a wiki link
   * If a file doesn't exist, you'll be given a new buffer with the default text for a new page.
   * if the file does exist it's opened. Yeah.
4. This system is sparse by design. There are only five things that get marked:
   * WikiLinks
   		* These are identified as `markup.underline.internal.link.SublimeWiki`. You may need to add style rules to your favorite theme to have it render.
	* Markdown-style `**bold** __markings__` are used. 
		* Identified as `markup.bold.SublimeWiki`
	* For that matter, Markdown-esque `_italic_ *strings*` are also supported.
		* Identified as `markup.italic.SublimeWiki`
	* "Double Quoted Strings"
		* Identified as `string.quoted.double.SublimeWiki`
	* URL links
		* Identified as `markup.underline.external.link.SublimeWiki`.

##How You Could Help
1. I would like to make the WikiWords linker more robust, and possibly find a way to have it identify any words that are the names of other pages in the directory, so that you could use any word as a keyword, a la [Tomboy](http://projects.gnome.org/tomboy/).
2. Support for external hyperlinks would be nice. Right now they're highlighted, but you can't follow them. If there's a good, cross-platform way to open a link in the default browser that would be great.


