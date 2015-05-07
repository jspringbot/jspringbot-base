jspringbot-base [![Build Status](https://buildhive.cloudbees.com/job/jspringbot/job/jspringbot-base/badge/icon)](https://buildhive.cloudbees.com/job/jspringbot/job/jspringbot-base/)
===============

Use this as parent module project for your test project.

### Quick Start

To use this jspringbot-base you have to do the following:

1. Ensure to add the following `repository` and `pluginRepository` on `~/.m2/settings.xml`
```xml
    <repository>
      <id>sonatype-nexus-snapshots</id>
      <name>Sonatype Nexus Snapshots</name>
      <url>https://oss.sonatype.org/content/repositories/snapshots</url>
      <releases><enabled>false</enabled></releases>
      <snapshots>
        <enabled>true</enabled>
        <updatePolicy>always</updatePolicy>
      </snapshots>
    </repository>
```
```xml
    <pluginRepository>
      <id>sonatype-nexus-snapshots</id>
      <name>Sonatype Nexus Snapshots</name>
      <url>https://oss.sonatype.org/content/repositories/snapshots</url>
      <releases><enabled>false</enabled></releases>
      <snapshots>
        <enabled>true</enabled>
        <updatePolicy>always</updatePolicy>
      </snapshots>
    </pluginRepository>
```

2. Add the following parent tag to test modules on `pom.xml`.
```xml
    <parent>
      <groupId>org.jspringbot</groupId>
      <artifactId>jspringbot-base</artifactId>
      <version>1.2</version>
    </parent>
```

3. When adding jspringbot dependencies no need to include `version`. Should be managed by `jspringbot-base` parent module.
```xml
    <dependency>
      <groupId>org.jspringbot</groupId>
      <artifactId>jspringbot-selenium</artifactId>
    </dependency>
```


