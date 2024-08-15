# Steps to build Docker image using buildpack

1. Locate the pom.xml
2. Find the build tag and then plugins tag.
3. Add image tag to configuration tag with name tag in it like belows
4. 
        <plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
				<configuration>

                <!-- BELOW TAG TO BE ADDED -->
                <image>
                    <name>eazybytes/${project.artifactId}:s4</name>
                </image>
                <!-- TILL HERE -->


				</configuration>
			</plugin>
		</plugins>


# Steps to build Docker image using google jib

1. Locate the pom.xml
2. Find the build tag and then plugins tag.
3. Add to tag to configuration tag with name tag in it like belows

```
        <plugins>
			<plugin>
				<groupId>com.google.cloud.tools</groupId>
				<artifactId>jib-maven-plugin</artifactId>
				<version>3.4.2</version>
				<configuration>

                <!-- BELOW TAG TO BE ADDED -->
					<to>
						<image>vijaydahiya/${project.artifactId}:s6</image>
					</to>
                <!-- TILL HERE -->

				</configuration>
			</plugin>
		</plugins>
```