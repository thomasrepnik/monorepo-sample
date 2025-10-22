```
docker run --rm -d -p 8081:8081 --name nexus -v nexus-data:/nexus-data sonatype/nexus3
mvn -s monorepo-settings.xml monorepo:plan-release
mvn -s monorepo-settings.xml monorepo:perform-release -DsettingsXmlFile=monorepo-settings.xml
mvn -s monorepo-settings.xml monorepo:build
```
