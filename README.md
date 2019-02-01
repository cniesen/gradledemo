Multi SpringBoot
================
Gradle with multiple projects, each a separate springboot app.

Run `gradlew bootRun`
```
> Configure project :app1
In task bootRun in app1
In task dependsOnTask in app1

> Configure project :app2
In task bootRun in app2
In task dependsOnTask in app2
In task app1DepensOnTask in app2

> Task :app2:app1DepensOnTask
In task app1DepensOnTask.doFirst in app2
In task app1DepensOnTask.doLast in app2

> Task :app1:dependsOnTask
In task dependsOnTask.doFirst in app1
In task dependsOnTask.doLast in app1

> Task :app1:bootRun
In task bootRun.doFirst in app1
*** The app1 is running ... and that was it already. ***
In task bootRun.doLast in app1

> Task :app2:dependsOnTask
In task dependsOnTask.doFirst in app2
In task dependsOnTask.doLast in app2

> Task :app2:bootRun
In task bootRun.doFirst in app2
*** The app2 is running ... and that was it already. ***
In task bootRun.doLast in app2

BUILD SUCCESSFUL in 3s
9 actionable tasks: 5 executed, 4 up-to-date
```

Also run `gradlew app1::bootRun` to run only app1

```
> Configure project :app1
In task bootRun in app1
In task dependsOnTask in app1

> Configure project :app2
In task bootRun in app2
In task dependsOnTask in app2
In task app1DepensOnTask in app2

> Task :app2:app1DepensOnTask
In task app1DepensOnTask.doFirst in app2
In task app1DepensOnTask.doLast in app2

> Task :app1:dependsOnTask
In task dependsOnTask.doFirst in app1
In task dependsOnTask.doLast in app1

> Task :app1:bootRun
In task bootRun.doFirst in app1
*** The app1 is running ... and that was it already. ***
In task bootRun.doLast in app1

BUILD SUCCESSFUL in 2s
5 actionable tasks: 3 executed, 2 up-to-date
```

And run `gradlew app2::bootRun` to run only app2
```
> Configure project :app1
In task bootRun in app1
In task dependsOnTask in app1

> Configure project :app2
In task bootRun in app2
In task dependsOnTask in app2
In task app1DepensOnTask in app2

> Task :app2:dependsOnTask
In task dependsOnTask.doFirst in app2
In task dependsOnTask.doLast in app2

> Task :app2:bootRun
In task bootRun.doFirst in app2
*** The app2 is running ... and that was it already. ***
In task bootRun.doLast in app2

BUILD SUCCESSFUL in 2s
4 actionable tasks: 2 executed, 2 up-to-date
```
[See other branches for more demos]