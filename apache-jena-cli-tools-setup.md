# Apache Jena CLI tools setup

↑ **Parent:** [Apache Jena](apache-jena.md)

The [CLI](command-line-interface.md) tools don't appear to be packaged for [Ubuntu 23.10](ubuntu-23-10.md)? Annoying... There is a package `libapache-jena-java` but it doesn't contain any binaries, only [Java](java-programming-language.md) library files.

To run the CLI tools easily we can download the prebuilt:
```
sudo apt install openjdk-22-jre
wget https://dlcdn.apache.org/jena/binaries/apache-jena-4.10.0.zip
unzip apache-jena-4.10.0.zip
cd apache-jena-4.10.0
export JENA_HOME="$(pwd)"
export PATH="$PATH:$(pwd)/bin"
```
and we can confirm it works with:
```
sparql -version
```
which outputs:
```
Apache Jena version 4.10.0
```

If your [Java](java-programming-language.md) is too old then then running `sparql` with the prebuilts fails with:
```
Error: A JNI error has occurred, please check your installation and try again
Exception in thread "main" java.lang.UnsupportedClassVersionError: arq/sparql has been compiled by a more recent version of the Java Runtime (class file version 55.0), this version of the Java Runtime only recognizes class file versions up to 52.0
        at java.lang.ClassLoader.defineClass1(Native Method)
        at java.lang.ClassLoader.defineClass(ClassLoader.java:756)
        at java.security.SecureClassLoader.defineClass(SecureClassLoader.java:142)
        at java.net.URLClassLoader.defineClass(URLClassLoader.java:473)
        at java.net.URLClassLoader.access$100(URLClassLoader.java:74)
        at java.net.URLClassLoader$1.run(URLClassLoader.java:369)
        at java.net.URLClassLoader$1.run(URLClassLoader.java:363)
        at java.security.AccessController.doPrivileged(Native Method)
        at java.net.URLClassLoader.findClass(URLClassLoader.java:362)
        at java.lang.ClassLoader.loadClass(ClassLoader.java:418)
        at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:352)
        at java.lang.ClassLoader.loadClass(ClassLoader.java:351)
        at sun.launcher.LauncherHelper.checkAndLoadMain(LauncherHelper.java:621)
```

Build from source is likely something like:
```
sudo apt install maven openjdk-22-jdk
git clone https://github.com/apache/jena --branch jena-4.10.0 --depth 1
cd jena
mvn clean install
```
TODO test it.

If you make the mistake of trying to run the source tree without build:
```
git clone https://github.com/apache/jena --branch jena-4.10.0 --depth 1
cd jena
export JENA_HOME="$(pwd)"
export PATH="$PATH:$(pwd)/apache-jena/bin"
```
it fails with:
```
Error: Could not find or load main class arq.sparql
```
as per: [https://users.jena.apache.narkive.com/T5TaEszT/sparql-tutorial-querying-datasets-error-unrecognized-option-graph](https://users.jena.apache.narkive.com/T5TaEszT/sparql-tutorial-querying-datasets-error-unrecognized-option-graph)

## ↑ Ancestors (13)

1. [Apache Jena](apache-jena.md)
2. [SPARQL implementation](sparql-implementation.md)
3. [SPARQL](sparql.md)
4. [Semantic triple](semantic-triple.md)
5. [Resource Description Framework](resource-description-framework.md)
6. [Knowledge graph](knowledge-graph.md)
7. [Ontology](ontology.md)
8. [Machine learning](machine-learning-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Jena SPARQL hello world](jena-sparql-hello-world.md)
