# Maven-MCP
A Maven repo for my clients

```maven
 <properties>
        <maven.compiler.source>8</maven.compiler.source>
        <maven.compiler.target>8</maven.compiler.target>
        <kotlin.version>1.4.32</kotlin.version>
    </properties>

    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-shade-plugin</artifactId>
                <version>3.2.4</version>
                <configuration>
                    <createDependencyReducedPom>true</createDependencyReducedPom>
                </configuration>
                <executions>
                    <execution>
                        <phase>package</phase>
                        <goals>
                            <goal>shade</goal>
                        </goals>
                        <configuration>
                            <filters>
                                <filter>
                                    <artifact>*:*</artifact>
                                    <excludes>
                                        <exclude>META-INF/*.SF</exclude>
                                        <exclude>META-INF/*.DSA</exclude>
                                        <exclude>META-INF/*.RSA</exclude>
                                    </excludes>
                                </filter>
                            </filters>
                        </configuration>
                    </execution>
                </executions>
            </plugin>
            <plugin>
                <groupId>org.jetbrains.kotlin</groupId>
                <artifactId>kotlin-maven-plugin</artifactId>
                <version>1.4.32</version>
                <executions>
                    <execution>
                        <id>compile</id>
                        <phase>process-sources</phase>
                        <goals>
                            <goal>compile</goal>
                        </goals>
                    </execution>
                    <execution>
                        <id>test-compile</id>
                        <goals>
                            <goal>test-compile</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>

    <repositories>
        <repository>
            <name>Maven-MCP</name>
            <id>MCP</id>
            <url>https://github.com/CodedDevYT/Maven-MCP/raw/repository</url>
        </repository>
    </repositories>

    <dependencies>
        <dependency>
            <groupId>org.jetbrains.kotlin</groupId>
            <artifactId>kotlin-stdlib</artifactId>
            <version>1.4.32</version>
        </dependency>

        <dependency>
            <groupId>net.minecraft</groupId>
            <artifactId>minecraft</artifactId>
            <version>1.8.8</version>
        </dependency>

        <dependency>
            <groupId>oshi-project</groupId>
            <artifactId>oshi-core</artifactId>
            <version>1.1</version>
        </dependency>

        <dependency>
            <groupId>net.java.dev.jna</groupId>
            <artifactId>jna</artifactId>
            <version>3.4.0</version>
        </dependency>

        <dependency>
            <groupId>net.java.dev.jna</groupId>
            <artifactId>platform</artifactId>
            <version>3.4.0</version>
        </dependency>

        <dependency>
            <groupId>com.ibm.icu</groupId>
            <artifactId>icu4j</artifactId>
            <version>51.2</version>
        </dependency>

        <dependency>
            <groupId>net.sf.jopt-simple</groupId>
            <artifactId>jopt-simple</artifactId>
            <version>4.6</version>
        </dependency>

        <dependency>
            <groupId>com.paulscode</groupId>
            <artifactId>codecjorbis</artifactId>
            <version>20101023</version>
        </dependency>

        <dependency>
            <groupId>com.paulscode</groupId>
            <artifactId>codecwav</artifactId>
            <version>20101023</version>
        </dependency>

        <dependency>
            <groupId>com.paulscode</groupId>
            <artifactId>libraryjavasound</artifactId>
            <version>20101123</version>
        </dependency>

        <dependency>
            <groupId>com.paulscode</groupId>
            <artifactId>librarylwjglopenal</artifactId>
            <version>20100824</version>
        </dependency>

        <dependency>
            <groupId>com.paulscode</groupId>
            <artifactId>soundsystem</artifactId>
            <version>20120107</version>
        </dependency>

        <dependency>
            <groupId>io.netty</groupId>
            <artifactId>netty-all</artifactId>
            <version>4.0.23.Final</version>
        </dependency>

        <dependency>
            <groupId>com.google.guava</groupId>
            <artifactId>guava</artifactId>
            <version>17.0</version>
        </dependency>

        <dependency>
            <groupId>org.apache.commons</groupId>
            <artifactId>commons-lang3</artifactId>
            <version>3.3.2</version>
        </dependency>

        <dependency>
            <groupId>commons-io</groupId>
            <artifactId>commons-io</artifactId>
            <version>2.4</version>
        </dependency>

        <dependency>
            <groupId>commons-codec</groupId>
            <artifactId>commons-codec</artifactId>
            <version>1.9</version>
        </dependency>

        <dependency>
            <groupId>net.java.jinput</groupId>
            <artifactId>jinput</artifactId>
            <version>2.0.5</version>
        </dependency>

        <dependency>
            <groupId>net.java.jutils</groupId>
            <artifactId>jutils</artifactId>
            <version>1.0.0</version>
        </dependency>

        <dependency>
            <groupId>com.google.code.gson</groupId>
            <artifactId>gson</artifactId>
            <version>2.2.4</version>
        </dependency>

        <dependency>
            <groupId>org.apache.commons</groupId>
            <artifactId>commons-compress</artifactId>
            <version>1.8.1</version>
        </dependency>

        <dependency>
            <groupId>org.apache.httpcomponents</groupId>
            <artifactId>httpclient</artifactId>
            <version>4.3.3</version>
        </dependency>

        <dependency>
            <groupId>commons-logging</groupId>
            <artifactId>commons-logging</artifactId>
            <version>1.1.3</version>
        </dependency>

        <dependency>
            <groupId>org.apache.httpcomponents</groupId>
            <artifactId>httpcore</artifactId>
            <version>4.3.2</version>
        </dependency>

        <dependency>
            <groupId>org.apache.logging.log4j</groupId>
            <artifactId>log4j-api</artifactId>
            <version>2.0-beta9</version>
        </dependency>

        <dependency>
            <groupId>org.apache.logging.log4j</groupId>
            <artifactId>log4j-core</artifactId>
            <version>2.0-beta9</version>
        </dependency>

        <dependency>
            <groupId>org.lwjgl</groupId>
            <artifactId>lwjgl</artifactId>
            <version>2.9.4-nightly-20150209</version>
        </dependency>

        <dependency>
            <groupId>org.lwjgl</groupId>
            <artifactId>lwjgl_util</artifactId>
            <version>2.9.4-nightly-20150209</version>
        </dependency>

        <dependency>
            <groupId>com.mojang</groupId>
            <artifactId>authlib</artifactId>
            <version>1.5.21</version>
        </dependency>

        <dependency>
            <groupId>tv.twitch</groupId>
            <artifactId>twitch</artifactId>
            <version>6.5</version>
        </dependency>

        <dependency>
            <groupId>com.thealtening.auth</groupId>
            <artifactId>auth</artifactId>
            <version>3.0.2</version>
        </dependency>
    </dependencies>
```
