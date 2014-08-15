# Budi's Personal Maven Repository

## Install Maven JAR
mvn install:install-file
 -DgroupId=[group-id]
 -DartifactId=[artifact-id]
 -Dversion=[version]
 -Dpackaging=[packaging-format]
 -Dfile=[path-to-file]
 -DlocalRepositoryPath=[path-to-git-repo]

* [group-id],[artifact-id],[version] and [packaging-format] define the Maven properties of the file to install
* [path-to-file] is the path to the JAR file to install
* [path-to-git-repo] is the path to the local Git repository on your computer

Commit & push to your github repo

## Use
Add this to projects pom.xml:

```xml
<repository>
    <id>git-[username]</id>
    <name>[username]'s Git based repo</name>
    <url>https://github.com/[username]/[repo-name]/raw/master/</url>
</repository>
```

[username] is your github username
[repo-name] is the name of the github repo you created
