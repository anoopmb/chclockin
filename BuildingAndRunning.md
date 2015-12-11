To build the app, do

`mvn clean install`

in the server directory. This creates chclockin.war in the target directory.

To run the app in-place (does not require Tomcat), do

`mvn jetty:run`

in the server directory. This stands the app up on port 8080

or

`mvn jetty:run -Djetty.port=<port>`

to start on the port of your choice.