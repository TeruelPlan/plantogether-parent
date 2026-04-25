# plantogether-parent

Parent POM for all PlanTogether microservices. Centralizes dependency versions, plugin configuration, and build conventions.

## Usage

All microservices declare this as their `<parent>`. Install locally before building any service:

```bash
mvn clean install
```

## Checking for dependency updates

The [Versions Maven Plugin](https://www.mojohaus.org/versions/versions-maven-plugin/) is configured to report outdated dependencies and plugins. Pre-release versions (alpha, beta, RC, M-builds, SNAPSHOT) are automatically excluded.

```bash
# List dependencies with newer stable versions
mvn versions:display-dependency-updates

# List plugins with newer stable versions
mvn versions:display-plugin-updates

# Update all version properties in pom.xml automatically
mvn versions:update-properties

# Revert pom.xml to its previous state (versions-maven-plugin creates a backup)
mvn versions:revert
```
