# HTML Questions Answers And External Sources

###<a name='q1'>What's a `doctype` do? </a>
    
DOCTYPE is an instruction that associates a particular SGML or XML document with a document type definition DTD.

[Wikipedia](http://en.wikipedia.org/wiki/Document_type_declaration)

The HTML layout engines in modern web browsers perform DOCTYPE "sniffing" or "switching", wherein the DOCTYPE in a document served as text/html determines a layout mode, such as "quirks mode" or "standards mode".

[HTML Living standard](http://www.whatwg.org/specs/web-apps/current-work/multipage/syntax.html#the-doctype)

DOCTYPEs are required for legacy reasons. When omitted, browsers tend to use a different rendering mode that is incompatible with some specifications. Including the DOCTYPE in a document ensures that the browser makes a best-effort attempt at following the relevant specifications.


###<a name ='q2'>What's the difference between standards mode and quirks mode?</a>

Layout engines in web browsers nowadays uses three modes: quirks mode, almost standards mode and standards mode.

In **quirks mode**, layout emulates nonstandard behavior in Navigator 4 and IE 5 for Windows. 

In **full standard mode**, the behavior is according to HTML and CSS specification.

In **almost standards mode**, there are only a very small number of quirks implemented.
    
[Mozila Quirks Mode Behavior](https://developer.mozilla.org/en-US/docs/Mozilla_Quirks_Mode_Behavior)

[Internet Explorer compatibility modes](http://goo.gl/aJpR2X)
 
  
###<a name ='q3'>What are the limitations when serving XHTML pages?</a>

* XHTML does not promote separation of content and presentation any more than HTML does.

* Proper XHTML is an application of XML and as such requires that authors follow strict rules when authoring XHTML. In particular:
    1. Raw < and & characters are not allowed except inside of CDATA Sections (<![CDATA[ ... ]]>).
    1. Comments (<!—— ... ——>) must not contain double dashes (——).
    1. Content contained within Comments (<!—— ... ——>) can be ignored.
    
* __Are there any problems with serving pages as `application/xhtml+xml`?__


When an XHTML page is served with MIME type text/html it is treated by all browsers as if it were nothing more than HTML. 
However when an XHTML page is served with MIME type text/xml or application/xhtml+xml,
then it should be treated as an XML document which must conform to the strict rules for authoring and displaying XML.
Prior to version 9, Microsoft® Internet Explorer only supports XHTML if 
it is served with MIME media type text/html rather than the recommended `application/xhtml+xml`.

Inline style and script tags can cause problems in XHTML when it is treated as XML rather than HTML.
             
[Using CSS and JavaScript in XHTML - MDN](http://goo.gl/ApM59d)

[XHTML™ 1.0](http://www.w3.org/TR/xhtml1/)

###<a name ='q4'>How do you serve a page with content in multiple languages?</a>

The human language of each passage or phrase in the content can be programmatically determined except for proper names, technical terms, words of indeterminate language, and words or phrases that have become part of the vernacular of the immediately surrounding text.
    
If you wanted to include a passage in Bulgarian you would need to use the `lang` attribute to mark the change in language.
The `lang` attribute can be used with almost every HTML element, making it very easy to change languages within a page.
To include a Bulgarian quotation on an English page you would simply add the lang attribute to the `blockquote` tag:

    <blockquote lang=”bg”>
    <p>Това, дето ми е на главата, мога да сваля, но това, дето ми е в сърцето, не мога да извадя.</p>
    </blockquote>

####<a name ='q4a'> What kind of things must you be wary of when design or developing for multilingual sites?</a>

If you don't provide a primary language code or set the code incorrectly it may be impossible for someone using a screen reader or Braille device to understand the content. 
If the primary language of the web page has not been identified, screen reading software in general will read out the content in the same language as the default setting for the screen reader.

Unlike assisting technologies such as screen readers, Google does not recognise language identifiers such as 'lang' attributes in the code of the page. 
Google tries to work out the main languages of your pages itself. In order to make language identification easier for Google, Google recommends only using one language per page.