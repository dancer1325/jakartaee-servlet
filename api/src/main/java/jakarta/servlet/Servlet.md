* == life-cycle methods / 👁️must be implemented by ALL servlets 👁️
  * are called in the order
    * `.init()`
      * -> servlet is initialized & constructed
    * `.service()`
      * if client invoked it -> handle it
        * HTTP requests -- are dispatched to the corresponding -- handler methods / HTTP request type 
    * `.destroy()`
      * -> servlet is out of service, and then -> garbage collected
  * other methods
    * `.getServletConfig()`
      * get any startup information
    * `.getServletInfo()`
* ways to implement it
  * extend `GenericServlet`
  * extend `HttpServlet`