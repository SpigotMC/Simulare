Simulare
========

Maven plugin which converts Java 7 classes back to Java 6.

Example Configuration
---------------------

```xml
<plugin>
    <groupId>net.md-5</groupId>
    <artifactId>simulare</artifactId>
    <version>0.1</version>
    <executions>
        <execution>
            <phase>process-classes</phase>
            <goals>
                <goal>transform</goal>
            </goals>
        </execution>
    </executions>
</plugin>
<plugin>
    <groupId>org.codehaus.mojo</groupId>
    <artifactId>animal-sniffer-maven-plugin</artifactId>
    <version>1.13</version>
    <executions>
        <execution>
            <phase>process-classes</phase>
            <goals>
                <goal>check</goal>
            </goals>
        </execution>
    </executions>
    <configuration>
        <ignores>
            <ignore>java.lang.Throwable</ignore>
        </ignores>
        <signature>
            <groupId>org.codehaus.mojo.signature</groupId>
            <artifactId>java16</artifactId>
            <version>1.1</version>
        </signature>
    </configuration>
</plugin>
```
