# HTML Questions Answers and external sources

1. <a name='q1'>What's a `doctype` do? </a>
   
    DOCTYPE is an instruction that associates a particular SGML or XML document with a document type definition DTD.
    
    [Wikipedia](http://en.wikipedia.org/wiki/Document_type_declaration)
    
    The HTML layout engines in modern web browsers perform DOCTYPE "sniffing" or "switching", wherein the DOCTYPE in a document served as text/html determines a layout mode, such as "quirks mode" or "standards mode".
    
    [HTML Living standard](http://www.whatwg.org/specs/web-apps/current-work/multipage/syntax.html#the-doctype)
    
    DOCTYPEs are required for legacy reasons. When omitted, browsers tend to use a different rendering mode that is incompatible with some specifications. Including the DOCTYPE in a document ensures that the browser makes a best-effort attempt at following the relevant specifications.


1. What's the difference between standards mode and quirks mode?