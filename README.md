# Budi's Personal Maven Repository

## Install Maven JAR
```bash
mvn install:install-file
 -DgroupId=[group-id]
 -DartifactId=[artifact-id]
 -Dversion=[version]
 -Dpackaging=[packaging-format]
 -Dfile=[path-to-file]
 -DlocalRepositoryPath=[path-to-git-repo]
```

* [group-id],[artifact-id],[version] and [packaging-format] define the Maven properties of the file to install
* [path-to-file] is the path to the JAR file to install
* [path-to-git-repo] is the path to the local Git repository on your computer

Or you can use project pom file to define groupId, artifactId, groupId, version and packaging format using this command:

```sh
mvn install:install-file 
    -Dfile=[path-to-file] 
    -DpomFile=[path-to-pom-file] 
    -DlocalRepositoryPath=[path-to-git-repo]
```

Commit & push to your github repo

Documentation about maven install-file plugin can be found [here](http://maven.apache.org/plugins/maven-install-plugin/install-file-mojo.html).

## Use
Add this to projects pom.xml:

```xml
<repositories>
    <repository>
        <id>git-[username]</id>
        <name>[username]'s Git based repo</name>
        <url>https://github.com/[username]/[repo-name]/raw/master/</url>
    </repository>
</repositories>
```

[username] is your github username
[repo-name] is the name of the github repo you created
