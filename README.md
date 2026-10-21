# AWS DevOps Sample Project

A small Java + Maven project for practicing GitHub and Jenkins CI/CD.

## Project files
- `pom.xml`: Maven build configuration
- `src/main/java/App.java`: Java application
- `Jenkinsfile`: Jenkins pipeline to checkout, build, test, and package
- `scripts/deploy.sh`: Example deployment placeholder
- `scripts/install-jenkins.sh`: Ubuntu Jenkins installation helper (review before running)

## Build locally
Requires Java 17+ and Maven:
```bash
mvn clean test package
java -jar target/devops-demo-1.0-SNAPSHOT.jar
```

## GitHub upload
Upload the extracted files/folders to the root of your GitHub repository. Keep the directory structure.

## Safety
The scripts are examples. Review them before running. The deployment script does not deploy to AWS automatically; configure your target and credentials first. Never commit AWS keys, passwords, or tokens.
