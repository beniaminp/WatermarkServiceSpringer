This is the WatermarkService for SpringerNature test.

This project is build using SpringBoot to run an embedded tomcat container.
I also used spring-core, spring-context, spring-tx...(can be found in pom.xml) with hibernate for ORM.
I used a SqLite database. I choose this option over an in memory database because I want to simulate a real scenario (In a real
scenario, is possible to add data to the service database from and external service, or to connect watermark service to an external documents database).
I tried to use only generics, to be possible to add new functionalities in the future without the need to change a lot from the application structure (new tables and entities
can be added without having to create new services for every entity).
I know that probably is not the best approach to the problem.
This is what I understood from the requirements and I hope that I understood correct :).

Prerequirements:

- you should have installed java 8
- you should have installed maven

To run this project, follow the steps:

- go to project folder ('cd WatermarkService/')
- run 'mvn clean' to clean the target directory
- run 'mvn package' to create 'target' folder, all dependencies and the executable WatermarkService.jar 
- go to target folder ('cd target/')
- under Linux systems, run './start.sh' (the process will start in background and will write logs to watermarkLog.txt)
- under Windows (and probably OSX) system, run java -jar WatermarkService.jar from command line

Configurations:

- in 'target/resources' folder you will find 2 files: application.properies and hibernate.properties
- in application.properites you can change you application start port(default 8080) and you database settings
- in hibernate.properties you can change the hibernate related settings

To stop the project:

- go to project target folder ('cd WatermarkService/target')
- under Linux systems, run ./stop.sh 
- under Windows (and probably OSX) system, find the pid of process and stop it
