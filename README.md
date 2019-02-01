Multi SpringBoot
================
Gradle with multiple projects, each a separate springboot web app.
This branch runs gradle in parallel, which allows both webserver to 
be started simultaneously. 

Run `gradlew bootRun`
Visit http://localhost:8081/ and http://localhost:8082/

Also run `gradlew app1::bootRun` to run only app1

And run `gradlew app2::bootRun` to run only app2

[See other branches for more demos]