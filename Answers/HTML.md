# HTML Questions Answers And External Sources

###<a name='#q1'>What's a `doctype` do? </a>
    
DOCTYPE is an instruction that associates a particular SGML or XML document with a document type definition DTD.

[Wikipedia](http://en.wikipedia.org/wiki/Document_type_declaration)

The HTML layout engines in modern web browsers perform DOCTYPE "sniffing" or "switching", wherein the DOCTYPE in a document served as text/html determines a layout mode, such as "quirks mode" or "standards mode".

[HTML Living standard](http://www.whatwg.org/specs/web-apps/current-work/multipage/syntax.html#the-doctype)

DOCTYPEs are required for legacy reasons. When omitted, browsers tend to use a different rendering mode that is incompatible with some specifications. Including the DOCTYPE in a document ensures that the browser makes a best-effort attempt at following the relevant specifications.


###<a name ='#q2'>What's the difference between standards mode and quirks mode?</a>

Layout engines in web browsers nowadays uses three modes: quirks mode, almost standards mode and standards mode.

In **quirks mode**, layout emulates nonstandard behavior in Navigator 4 and IE 5 for Windows. 

In **full standard mode**, the behavior is according to HTML and CSS specification.

In **almost standards mode**, there are only a very small number of quirks implemented.
    
[Mozila Quirks Mode Behavior](https://developer.mozilla.org/en-US/docs/Mozilla_Quirks_Mode_Behavior)

[Internet Explorer compatibility modes](http://goo.gl/aJpR2X)
 
  
###<a name ='#q3'>What are the limitations when serving XHTML pages?</a>

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