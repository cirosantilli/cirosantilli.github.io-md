# Jena SPARQL hello world

↑ **Parent:** [Apache Jena](apache-jena.md)  
🏷️ **Tags:** [Hello world](hello-world-program.md)

They have a tutorial at: [https://jena.apache.org/tutorials/sparql.html](https://jena.apache.org/tutorials/sparql.html)

Once you've done the [Apache Jena CLI tools setup](apache-jena-cli-tools-setup.md) we can query all users with Full Name (FN) "John Smith" directly fom the [rdf/vcard.ttl](rdf/vcard.ttl) [Turtle RDF](terse-rdf.md) file with the [rdf/vcard.rq](rdf/vcard.rq) [SPARQL](sparql.md) query:
```
sparql --data=rdf/vcard.ttl --query=rdf/vcard.rq
```
and that outputs:
```
---------------------------------
| x                             |
=================================
| <http://somewhere/JohnSmith/> |
---------------------------------
```

Bibliography:
- [https://stackoverflow.com/questions/41959550/cli-tool-ala-csvsql-for-sparql-and-ttl-n3-files-hello-world-example-for](https://stackoverflow.com/questions/41959550/cli-tool-ala-csvsql-for-sparql-and-ttl-n3-files-hello-world-example-for)

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

- [SPARQL tutorial](sparql-tutorial.md)
