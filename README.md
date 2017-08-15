# README


## PURPOSE

The purpose of this script is to notify website users they are using TLSv1.0 or other version of encruption that has been
deprecated.  This notification can be used in advance of the encryption ciphers being disabled entirely or used indefinately.
The banner can be injected with a multiple of triggers, beyond the inital intended goal.


Designed to be used with a Stream profile in F5 LTM.
This iRule takes advantage of the Stream profile which does not require additional memory allocation
for HTML storage, bit parsing, re-chunking, etc.
The banner text can quickly be changed and is resizeable to any window size or format.  Including mobile.
Text format, font, color and background color are also easily changable.
The javascript is appended to the closing </body> tag in the HTML to provide easy identification an insertion
into the HTML code, without consideration for inline CSS, HTML body formatting, customizations, etc.

## REQUIREMENTS
F5 LTM virtual-server must have a client SSL profile attached.

## USAGE
1. Create a string datagroup named tls_warn and add "tlsv1" to the string varible.
2. Create an iRule with the attached iRule code.
3. Modify/Create virtual-server with "Stream" and "HTTPCompression" profiles enabled.
4. Apply iRule to virtual-server.

Test.
Done.
