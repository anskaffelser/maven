# Maven repository

This repository is used to keep published Maven packages in one repository for convenience.

Please see the [GitHub Packages documentation](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry) on how to configure for usage.

## Example configuration

Inside `~/.m2/settings.xml`:
```xml
<repository>
    <id>anskaffelser</id>
    <url>https://maven.pkg.github.com/anskaffelser/maven</url>
    <snapshots>
        <enabled>true</enabled>
    </snapshots>
</repository>
```

```xml
<server>
    <id>anskaffelser</id>
    <username>[GITHUB USERNAME]</username>
    <password>[GITHUB TOKEN]</password>
</server>
```

Publishing information inside `pom.xml`:

```xml
<distributionManagement>
    <repository>
        <id>anskaffelser</id>
        <name>Anskaffelser Maven repository</name>
        <url>https://maven.pkg.github.com/anskaffelser/maven</url>
    </repository>
    <snapshotRepository>
        <id>anskaffelser</id>
        <name>Anskaffelser Maven repository</name>
        <url>https://maven.pkg.github.com/anskaffelser/maven</url>
    </snapshotRepository>
</distributionManagement>
```