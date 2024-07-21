* := interface /
  * provide -- client request information to a -- servlet
    * client request information as
      * parameter name and values
      * attributes
      * inputStream
  * uses
    * servlet container 
      * creates it
      * pass it as -- Servlet's `service(ServletRequest)`