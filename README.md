# xq-java-mvn-custom-repository

# How to use custom repository

Add a new profile and set the new profile as an active profile

Config a profile like the following code:

```xml
<settings>
    <activeProfiles>
        <activeProfile>custom-maven-center</activeProfile>
    </activeProfiles>
    <profiles>
        <profile>
            <id>custom-maven-center</id>
            <repositories>
                <repository>
                    <id>custom-mvn-center</id>
                    <name>Custom Maven Center</name>
                    <releases>
                        <enabled>true</enabled>
                        <updatePolicy>always</updatePolicy>
                        <checksumPolicy>warn</checksumPolicy>
                    </releases>
                    <snapshots>
                        <enabled>false</enabled>
                        <updatePolicy>never</updatePolicy>
                        <checksumPolicy>fail</checksumPolicy>
                    </snapshots>
                    <url>http://localhost:5000/repository/maven-central/</url>
                    <layout>default</layout>
                </repository>
            </repositories>
            <pluginRepositories>
                <pluginRepository>
                    <id>custom-mvn-center-plugin</id>
                    <name>Custom Maven Center Plugin</name>
                    <releases>
                        <enabled>true</enabled>
                        <updatePolicy>always</updatePolicy>
                        <checksumPolicy>warn</checksumPolicy>
                    </releases>
                    <snapshots>
                        <enabled>false</enabled>
                        <updatePolicy>never</updatePolicy>
                        <checksumPolicy>fail</checksumPolicy>
                    </snapshots>
                    <url>http://localhost:5000/repository/maven-central/</url>
                    <layout>default</layout>
                </pluginRepository>
            </pluginRepositories>
        </profile>
    </profiles>
</settings>
```
