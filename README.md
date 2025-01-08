DEMO for an OpenRewrite issue specifically with the Maven tool. 
The RemoveDuplicateDependencies rule removes a dependency that should not be deleted.
After the dependency is removed, the Maven build naturally fails.

I know this is not a clean Maven project, but this is how it exists.

```
mvnw org.openrewrite.maven:rewrite-maven-plugin:5.47.3:run
  -Drewrite.recipeArtifactCoordinates=org.openrewrite.recipe:rewrite-migrate-java:LATEST
  -Drewrite.activeRecipes=org.openrewrite.maven.RemoveDuplicateDependencies
```
