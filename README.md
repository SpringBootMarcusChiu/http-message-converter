https://www.javacodegeeks.com/2013/07/spring-mvc-requestbody-and-responsebody-demystified.html

I think Spring comes default with XML and JSON converter. Here in the basic Spring Boot 
Application we have create a custom converter for text/csv mime type

0. start server
   mvn spring-boot:run

1. curl -X PUT --header "Content-Type: text/csv" localhost:8080/bookcase -d '"123","Spring in Action"'
   curl -X PUT --header "Content-Type: text/csv" localhost:8080/bookcase -d $'"123","Spring in Action"\n"1234","Hello World"'

2. curl -X GET --header "Content-Type: text/csv" localhost:8080/bookcase