# gitflows

- Create develop, production, hotfix, feature branches 
```
git branch -a
  develop
  feature
  hotfix
* master
  release
```

- Change default branch to `develop`
- Protect `master` branch 
  - Require pull request reviews before merging
  - Include administrators

#
https://start.spring.io/

Install STS

#
### Tomcat initial users

```
tail tomcat-users.xml 
-->

  <role rolename="tomcat"/>
  <role rolename="manager-gui"/>
  <role rolename="manager-script"/>
  <user username="tomcat" password="tomcat" roles="tomcat"/>
  <user username="manager" password="tomcat" roles="tomcat,manager-gui"/>
  <user username="jenkins" password="jenkins" roles="manager-script"/>

</tomcat-users>
```

# 
### Artifactory
- Create maven repo, skip other options
- Default credentials `admin:password`

#
### Maven setting

```
# set java softlink
export JAVA_HOME=$(/usr/libexec/java_home)

export M2_HOME=/users/path/apache-maven-3.5.6
export M2=$M2_HOME/bin
export PATH=$M2:$PATH
```

```
~/.m2/settings-security.xml
~/.m2/settings.xml
```

Generate maven master password and password used to connect to artifactiry

- `mvn -emp` -> `~/.m2/settings-security.xml`
- `mvn -ep` -> `~/.m2/settings.xml`

#
### Jenkins plugins
- Javadoc
- Maven integration plugin
- Ant plugin
- Run Condition Plugin
- Conditional BuildStep
- Deploy to container Plugin


