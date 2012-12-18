jspringbot-base
===============

Use this as parent module project for your test project.

### Quick Start

To use this jspringbot-base you have to do the following:

1. Ensure to add the following on `~/.m2/settings.xml`
```
  <repositories>
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
      </repositories>
      <pluginRepositories>
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
  </pluginRepositories>
```

2. Add the following parent tag to test modules on `pom.xml`.
```
  <parent>
    <groupId>org.jspringbot</groupId>
    <artifactId>jspringbot-base</artifactId>
    <version>1.0-SNAPSHOT</version>
  </parent>
```

3. When adding jspringbot dependencies no need to include `version`. Should be managed by `jspringbot-base` parent module.
```
    <dependency>
      <groupId>org.jspringbot</groupId>
      <artifactId>jspringbot-selenium</artifactId>
    </dependency>
```


