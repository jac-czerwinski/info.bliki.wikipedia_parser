
> The Java Wikipedia API (Bliki engine)
> is a parser library for converting
> Wikipedia wikitext notation to HTML.

## Features

  * renders Mediawiki/Wikipedia wiki syntax to HTML. It supports:
    wiki tags for bold, italic, headers, nowiki, source, table of content,...
    wiki tables, lists, categories, footnotes (references)
    Image:... tag support
    wiki <source> tag for syntax highlighting of source code fragments:
        java, php, python, html/xml, javascript,...

    templates (includeonly, noinclude,...)]
        The following template parser functions are implemented:
        Expr, If, Ifeq, Iferror, Ifexist, Ifexpr, LC, LCFirst, Padleft,
        Padright, Subst, Switch, Tag, UC, UCFirst, URLEncode
        only partial support is available for: Fullurl, Localurl, NS, Time
  * extendable through a model interface (IWikiModel.java)
  * converts HTML to Wikipedia (available as Appengine, GWT application)
  * helper classes for the Wikimedia api.php for downloading wiki texts...
  * Example HTMLCreatorExample.java which shows, how to download a complete
    wiki page with templates and images and render it to HTML.
    The templates are cached in a Derby database.
  * helper classes to work with MediaWiki XML dump files.
  * BlikiConverter - A converter tool for using the Wiki2HTML, Plain2Wiki and
    HTML2Wiki conversion methods in a Java Swing GUI
  * Lua/Scribunto extension (WIP)

Try the [online converter][] on Google App Engine.

## Installation from source

	$ git submodule init && git submodule update
	$ mvn install -DskipTests

[online converter]: http://w-i-k-i.appspot.com/