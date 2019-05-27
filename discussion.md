
## Spring projects are more extensive
- Spring Data JPA 
- Spring CDC 
- Spring community is huge
- `SpringRunner` ... see below

## Personal feelings ( open to change ;))
- I just think the Spring Boot is shorter and easier to read ... 
- Testing with `SpringRunner` was easier than `Arquillian`
- Does Arquillian support random ports?
- Had to add:
- `-Dthorntail.arquillian.daemon.port=19999 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Xbootclasspath/p:C:/Users/Henry/.m2/repository/org/jboss/logmanager/jboss-logmanager/2.1.11.Final/jboss-logmanager-2.1.11.Final.jar`
- Also had to run Project ... Clean often in Eclipse in `Thorntail`
- Alternatively, I could use Open Liberty (maybe the cleanup problem will go away)?
- which also brings up the next issue ... which vendor for Microprofile ... will I get into a vendor-lock problem?
- IDE support was nonexistent in Eclipse with (Eclipse Mircroprofile) - ironic?  I'm more than happy to be corrected
- Without running tests, the only other way to start microprofile-thorntail 
- `java -jar target\*.jar` ... not great for debugging
- takes a LONG time to run `java -jar target\*.jar`
- added a `GreetingServiceTest.runDummyServer` for debugging in interactive mode in `Thorntail` ... a hack
- SpringBoot has a `SpringBootApplication` ... vanilla `main` method
 
## Atlernative to Arquillian / SpringRunner
- I believe testing Microservices is part of Integration testing wrt [Martin Fowler's test Pyramid](https://martinfowler.com/articles/practical-test-pyramid.html)
- Java may not be the answer
- I STRONGLY recommend `Postman` (black box testing).  `Newman` can be used in CI
- Black box is good ... you also offset this work to other developers (i.e. a more junior developer with NodeJS skills)
- if you wish to migrate to `Postman` from `Arquillian`, there is a http://arquillian.org/guides/generator/  Arquillian APE REST Postman

 
# Conclusion
I still like Spring Boot more,
Then again, I'm open to giving Microprofile a shot
