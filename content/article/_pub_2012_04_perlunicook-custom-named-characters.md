{
   "title" : "Perl Unicode Cookbook: Custom Named Characters",
   "description" : "â 10: Custom named characters As several other recipes demonstrate, the charnames pragma offers considerable power to use and manipulate Unicode characters by their names. Its :alias option allows you to give your own lexically scoped nicknames to existing characters,...",
   "categories" : "unicode",
   "thumbnail" : null,
   "authors" : [
      "tom-christiansen"
   ],
   "image" : null,
   "draft" : null,
   "tags" : [],
   "date" : "2012-04-19T06:00:01-08:00",
   "slug" : "/pub/2012/04/perlunicook-custom-named-characters"
}





â 10: Custom named characters {#Custom-named-characters}
-----------------------------

As several other recipes demonstrate, the
[charnames](http://perldoc.perl.org/charnames.html) pragma offers
considerable power to use and manipulate Unicode characters by their
names. Its `:alias` option allows you to give your own lexically scoped
nicknames to existing characters, or even to give unnamed private-use
characters useful names:

     use charnames ":full", ":alias" => {
         ecute => "LATIN SMALL LETTER E WITH ACUTE",
         "APPLE LOGO" => 0xF8FF, # private use character
     };

     "\N{ecute}"
     "\N{APPLE LOGO}"

You may even override existing names (lexically, of course) with
different characters.

This feature has some limitations. For best effect, aliases should hew
to the rules of ASCII identifiers and must not resemble regex
quantifiers. You can only alias one character at a time; other options
exist to give a character sequence an alias.

As always, the documentation of the `charnames` pragma offers more
details.

Previous: [â 9: Unicode Named Character
Sequences](/media/_pub_2012_04_perlunicook-custom-named-characters/perlunicook-unicode-named-character-sequences.html)

Series Index: [The Standard
Preamble](/media/_pub_2012_04_perlunicook-custom-named-characters/perlunicook-standard-preamble.html)

Next: [â 11: Names of CJK
Codepoints](/media/_pub_2012_04_perlunicook-custom-named-characters/perlunicook-names-of-cjk-codepoints.html)

