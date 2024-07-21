* := interface /
  * `getOutputStream()`
    * uses
      * send binary data | MIME body response
      * \+ manual work, to -- send -- binary and text data
        * _Example:_ Multipart
  * `getWriter()`
    * uses
      * send character data | MIME body response
  * uses
    * servlet container 
      * creates it
      * pass it as -- Servlet's `service(ServletResponse)`
* ways to specify charset for the MIME body response
  * / request
    * -- via --
      * `setCharacterEncoding(String)` OR
      * `setCharacterEncoding(Charset)`
      * `setContentType`
      * `setLocale`
        * implicit specification
    * 👁️must be called before `getWriter` 👁️
  * / web-app
    * `ServletContext.setRequestCharacterEncoding`
  * / container
    * for ALL web applications deployed | container
  * "ISO-8859-1"
    * default charset
* TODO:
* Check [RFC 2045](http://www.ietf.org/rfc/rfc2045.txt)