# FleetCheck – Build Systems Lab

This project is intentionally incomplete. Follow the worksheet in the order given.

Expected final application output:

```
FleetCheck 1.0
Vehicles loaded: 4
Vehicles requiring service: 2
Average mileage: 37000 km
```

Do not copy the solution POM. The objective is to observe how each build change alters the result.


Evidence 8.1: gradle : The term 'gradle' is not recognized as the name of a cmdlet, function, script file, or
operable program. Check the spelling of the name, or if a path was included, verify that the path
is correct and try again.
Evidence 8.2:
The runtime dependency graph was inspected using:
gradle dependencies --configuration runtimeClasspath
The dependency graph shows jackson-databind:2.22.2 as the direct dependency.
jackson-annotations:2.22 and jackson-core:2.22.2 are transitive dependencies required by jackson-databind.
The dependency graph also contains jackson-bom:2.22.2 as a dependency constraint.
Changing from Maven to Gradle did not fundamentally change the required Jackson dependency hierarchy. Gradle resolves the direct dependency and its required transitive dependencies automatically.
Evidence 8.3:
FleetCheck 1.0
Vehicles loaded: 4
Vehicles requiring service: 1
Average mileage: 37000 km
Evidence 8.4:
The Gradle Wrapper was generated using:
gradle wrapper
The project now contains gradlew, gradlew.bat and the gradle/wrapper directory.
The build as then executed using:
.\gradlew.bat clean build
The Gradle Wrapper removes the assumption that Gradle must be globally installed and configured on the developer's machine. It allows the project to use its configured Gradle version consistently.