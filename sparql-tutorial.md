# SPARQL tutorial

↑ **Parent:** [SPARQL](sparql.md)

In this tutorial, we will use the [Jena SPARQL hello world](jena-sparql-hello-world.md) as a starting point. Tested on [Apache Jena](apache-jena.md) 4.10.0.

Basic query on [rdf/vcard.ttl](rdf/vcard.ttl) [RDF Turtle](web-ontology-language.md) data to find the person with full name "John Smith":
```
sparql --data=rdf/vcard.ttl --query=<( printf '%s\n' 'SELECT ?x WHERE { ?x <http://www.w3.org/2001/vcard-rdf/3.0#FN> "John Smith" }')
```
Output:
```
---------------------------------
| x                             |
=================================
| <http://somewhere/JohnSmith/> |
---------------------------------
```

To avoid writing `http://www.w3.org/2001/vcard-rdf/3.0#` a billion times as queries grow larger, we can use the `PREFIX` syntax:
```
sparql --data=rdf/vcard.ttl --query=<( printf '%s\n' '
PREFIX vc: <http://www.w3.org/2001/vcard-rdf/3.0#>
SELECT ?x
WHERE { ?x vc:FN "John Smith" }
')
```
Output:
```
---------------------------------
| x                             |
=================================
| <http://somewhere/JohnSmith/> |
---------------------------------
```

Bibliography:
- [UniProt](uniprot.md) contains some amazing examples runnable on their servers: [https://sparql.uniprot.org/.well-known/sparql-examples/](https://sparql.uniprot.org/.well-known/sparql-examples/)

## ↑ Ancestors (11)

1. [SPARQL](sparql.md)
2. [Semantic triple](semantic-triple.md)
3. [Resource Description Framework](resource-description-framework.md)
4. [Knowledge graph](knowledge-graph.md)
5. [Ontology](ontology.md)
6. [Machine learning](machine-learning-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
