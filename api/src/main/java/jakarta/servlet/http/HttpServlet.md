* := abstract class / 
  * if you want a suitable HTTP servlet -- for a -- Web site
    * 👁️-> create a subclass / override >= 1 of next methods 👁️
      * `doGet()`
      * `doPost()`
      * `doPut()`
      * `doDelete()`
      * `init()` & `destroy()`
      * `getServletInfo()`
    * about other methods
      * `service()`
        * NOT recommend to override
      * `doOptions()` & `doTrace()`
        * NOT recommend to override
  * `isSensitiveHeader(String)`
    * check HTTP request headers, and exclude the sensitive | `TRACE` request (== `doTrace()`)
      * HTTP header names are case-insensitive
    * 👁️headers / considered sensitive, start with 👁️
      * "authorization"
      * "cookie"
      * "x-forwarded"
      * "forwarded"
      * "proxy-authorization"
    * if you want to customize this sensitive header behavior -> override
      * `isSensitiveHeader` &
      * `doTrace`
  * `getLastModified`
    * returns last time (ms since midnight January 1, 1970 GMT), `HttpServletRequest` was modified
    * if Servlet supports HTTP GET requests & can quickly determine it -> should override it
      * Reason: 🧠 browser & proxy caches work more efficiently 🧠