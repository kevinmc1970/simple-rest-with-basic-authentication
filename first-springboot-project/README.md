created this project from tutorial https://www.youtube.com/watch?v=PSP1-2cN7vM&t=1349s (spingboot in 28 minutes)

springboot is quick way of creating a development, test and prod environment ready for starting a new application

had fun and games just getting the maven part of eclipse working - fix was to empty repo and run maven build.

had to add a few things to the pom.xml for springboot but fairly easy and I think there might be a way to create all of that in 1 go but tutorial is going through everything

Step 1 - ended up with a springboot app running on localhost:8080 (Tomcat server created and started by SB) - just by ruuning Application class

Step 2 - creating restful service - just use @RestController and @RequestMapping annotations
- error finding WelcomeService when in different package because @SpringBootApplication applies component scan to same package defined in!

step 3 - starter-web is the most common SB starter 
- auto-configurations - such as Dispatcher Servlet for spring, jackson, hibernate validation, /error page etc  
- can see it all by adding application.properties with logging.level.org.springframework: DEBUG

step 4 - SB makes sure that all versions of jars are compatible with each other

video ended so started this one https://www.youtube.com/watch?v=YEEUn5JZ9t0 - Rest Web Service with SB (and Spring Initializer)

// tried auto spring web security
- before this app would let me go to /welcome
- added dependency and went to /welcome - LOGIN PAGE POPUP appeared (didn't even need @EnableWebSecurity) - login page auto included!
- username=user and password in logs Using default security password: f9b9cdc0-f440-4d13-ba11-1c9372845237
- can change this in application.properties so have done user=notuser password=password
- didnt work until I took 'spring.' off front of property names!
- think app doesn't need @EnableWebSecurity - maybe a later version of spring




