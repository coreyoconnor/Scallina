
### Introductory paper:
*[A Coq-based synthesis of Scala programs which are correct-by-construction](http://dl.acm.org/citation.cfm?doid=3103111.3104041)*

### Quick start guide:

First, download the Scala Build Tool (SBT) from http://www.scala-sbt.org/download.html

Then, in the project's main directory run the command ```sbt assembly```

Finally, the below command:

```scala target/scala-2.12/scallina-assembly-<scallina-version>.jar <path-to-coq-source-file.v>```

can be executed from the project's main directory in order to run Scallina.

Also, the below command should also work:

```java -jar target/scala-2.12/scallina-assembly-<scallina-version>.jar <path-to-coq-source-file.v>```

### Usage Examples

Packaged examples are available under [```packaged-examples```](./packaged-examples)

Additional examples of Coq ```.v``` files that can be translated to Scala are available under [```src/test/resources/```](./src/test/resources/)

### Compiling the Generated Scala Files
The generated files can be compiled with the ```scalac``` Scala compiler provided that the [Scallina Standard Library](./packaged-examples/v0.5.0/scallina-standard-library-assembly-0.5.jar) is included in the classpath.

For a practical example, see the ```compile-scala-code.sh``` scripts in [```packaged-examples/v0.5.0/list-queue/```](./packaged-examples/v0.5.0/list-queue/) and [```packaged-examples/v0.5.0/selection-sort/```](./packaged-examples/v0.5.0/selection-sort/).

The source code of the Scallina Standard Library is available under [```src/main/resources/scala/of/coq/lang```](./src/main/resources/scala/of/coq/lang/).
