jspringbot-base [![Build Status](https://travis-ci.org/jspringbot/jspringbot-base.svg?branch=master)](https://travis-ci.org/jspringbot/jspringbot-base)
===============

Use this as parent module project for your test project.

### Quick Start

To use this jspringbot-base you have to do the following:

- Add the following parent tag to test modules on `pom.xml`.
```xml
    <parent>
      <groupId>org.jspringbot</groupId>
      <artifactId>jspringbot-base</artifactId>
      <version>1.5</version>
    </parent>
```

- When adding jspringbot dependencies no need to include `version`. Should be managed by `jspringbot-base` parent module.
```xml
    <dependency>
      <groupId>org.jspringbot</groupId>
      <artifactId>jspringbot-selenium</artifactId>
    </dependency>
```

### When using jspringbot snapshot version

- Ensure to add the following `repository` and `pluginRepository` on `pom.xml`
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

*Note:* You can copy the [settings.xml](https://github.com/jspringbot/jspringbot-base/blob/master/settings.xml) in your `~/.m2/` directory if you don't have one yet.


### Copyright and license

Copyright 2012 JSpringBot

Code licensed under [Apache License v2.0](http://www.apache.org/licenses/LICENSE-2.0).



