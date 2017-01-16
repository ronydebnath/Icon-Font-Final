Open *demo.html* to see a list of all the glyphs in your font along with their codes/ligatures.

To use the generated font in desktop programs, you can install the TTF font. In order to copy the character associated with each icon, refer to the text box at the bottom right corner of each glyph in demo.html. The character inside this text box may be invisible; but it can still be copied. 

##Supporting IE 7 and IE 6

Old versions of Internet Explorer (IE 7 and older), don't support pseudo elements. If you need to support these browsers, please refer to both a javascript polyfill and a special CSS file (that uses CSS expressions, aka dynamic properties) comes with this package. You can use either of these files.

##Serving Fonts from a Different Domain

Cross domain font requests fail in Firefox and newer versions of Internet Explorer. Therefore, if served from a different domain, your web fonts need to have the appropriate “Access-Control-Allow-Origin” response header. You can use the following two configs to properly set headers:

# For Apache
---
<FilesMatch ".(eot|ttf|otf|woff)">
  Header set Access-Control-Allow-Origin "*"
</FilesMatch>
---

# For nginx
---
location ~* \.(eot|ttf|woff)$ {
  add_header Access-Control-Allow-Origin '*';
}
---
To learn more about enabling cross-origin resource sharing, see enable-cors.org.


##Installing and Using Fonts Locally

To use the generated font in desktop applications, you can install the TTF font on your system. When installing the TTF font or viewing it, the operating system may not show all the glyphs in your font, but that doesn't mean that the glyphs aren't included in the font. In most cases only the basic Latin characters are shown.

If you are using macOS (or OS X), you can use Font Book to see all the glyphs included in the font by pressing cmd + 2 or choosing the second option on top left of Font Book.

After installing the TTF font, open the demo.html (included in the zip pack you downloaded) to see a list of the glyphs in your font. The text box located to the bottom right of each glyph contains a character (which may be invisible). You can copy and use this character in any desktop application that allows entering text and choosing a custom font to display it.

Note: When using type tools in a desktop applications, do not enter characters that don't exist in your font. If you do so, the desktop application may switch your selected font to a different font. You should only be copy/pasting the characters that exist in your font.
The following gif demonstrates different methods of copying characters assigned to your glyphs.

You won't need any of the files located under the *demo-files* directory when including the generated font in your own projects.


