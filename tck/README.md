# Jakarta Servlet

This repository contains the code for Jakarta Servlet TCK

About Jakarta Servlet TCK
-------------------------
* == server-side API
  * -- for handling -- HTTP requests
  * -- based on -- Junit5 & Arquillian

Building
--------
* Prerequisites
  * JDK 17+
  * Maven 3.9.0+
* how to build? 
  * `mvn install`

How to use?
------------

```xml
    <dependencies>
      <dependency>
        <groupId>jakarta.servlet</groupId>
        <artifactId>tck-runtime</artifactId>
      </dependency>
    </dependencies>
    <plugin>
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-surefire-plugin</artifactId>
      <version>${surefire.version}</version>
      <configuration>
        <dependenciesToScan>
          <dependenciesToScan>jakarta.servlet:tck-runtime</dependenciesToScan>
        </dependenciesToScan>
        <systemProperties>
          <!-- if the servlet container doesn't support optional cross context -->  
          <servlet.tck.support.crossContext>false</servlet.tck.support.crossContext>
          <!-- if the servlet container doesn't support optional http2 push -->  
          <servlet.tck.support.http2Push>false</servlet.tck.support.http2Push>
          <!-- 
          the slf4j impl to include within the deployed wars, default value is org.slf4j:slf4j-simple
          -->  
          <servlet.tck.slf4jimpl>org.slf4j:slf4j-simple</servlet.tck.slf4jimpl>  
        </systemProperties>          
      </configuration>
    </plugin>
```
