* == methods / 
  * uses
    * servlet -- can communicate with -- its servlet container
      * _Example:_
        * `getMimeType()`
        * `log` -- write to a servlet log file --
  * 1! / web application / JVM
  * if web application is marked "distributed" | deployment descriptor -> 1 ServletContext instance / JVM
    * -> ServletContext can NOT be used -- as location, to share -- global information
      * Reason: 🧠information will NOT be global 🧠
      * _Example alternatives:_ DDBB
* 👁️web application == serverletS + content 👁️
  * content / installed
    * | subset of server's URL namespace -- _Example:_ "/catalog" --
    * -- via (possibly) -- ".war"
