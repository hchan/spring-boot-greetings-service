# Comparision of Spring Boot vs Micro Profile Thorntail vs Micro Profile Open Liberty
## Spring projects are more extensive
- Spring Data JPA 
- Spring CDC 
- Spring community is huge
- `SpringRunner` ... see below

## Personal feelings ( open to change ;))
- I just think the Spring Boot is shorter and easier to read ... 
- Testing with `SpringRunner` was easier than `Arquillian`
- Better IDE support
- Does Arquillian support random ports?
- For Arquillian Thorntail:
- `-Dthorntail.arquillian.daemon.port=19999 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Xbootclasspath/p:C:/Users/Henry/.m2/repository/org/jboss/logmanager/jboss-logmanager/2.1.11.Final/jboss-logmanager-2.1.11.Final.jar`
- Also had to run Project ... Clean often in Eclipse in `Thorntail`
- didn't even bother to get this to run under eclise with `Open Liberty`
- IDE support was nonexistent for (Thorntail and Open Liberty) - no suppurt for Eclipse Microprofile in Eclipse ironic?  I'm more than happy to be corrected
- takes a LONG time to run `java -jar target\*.jar`
- added a `GreetingServiceTest.runDummyServer` for debugging in interactive mode in `Thorntail` ... a hack
- SpringBoot has a `SpringBootApplication` ... vanilla `main` method
- code was not transferrable from Thorntail to Open Liberty ( Open Liberty's `@ConfigProperty` choked ) ... does this mean vendor lock-in with MicroProfile?

## Atlernative to Arquillian / SpringRunner
- I believe testing Microservices is part of Integration testing wrt [Martin Fowler's test Pyramid](https://martinfowler.com/articles/practical-test-pyramid.html)
- Java may not be the answer
- I STRONGLY recommend `Postman` (black box testing).  `Newman` can be used in CI
- Black box is good ... you also offset this work to other developers (i.e. a more junior developer with NodeJS skills)
- if you wish to migrate to `Postman` from `Arquillian`, there is a http://arquillian.org/guides/generator/  Arquillian APE REST Postman

 
## Conclusion
I still like Spring Boot more,
Then again, I'm open to giving Microprofile a shot
