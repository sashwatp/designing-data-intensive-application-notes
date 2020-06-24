# Relational Model vs Document Model



# Triple-Stores and SPARQL

1. All information is stored in the form `(Subject, Predicate, Object)`. Eg: `(Jim, likes, Banana)`
   1. Objects can either be a key value like `(lucy, age, 33)` or another vertex in the graph like `(lucy, marriedTo, alain)`
2. The Resource Description Framework (RDF) -> was intended to present data in a consistent format so that data from different websites can be combined into a graph. 
   1. Turtle (example below) is an example of RDF data. Similarly, XML can also be used for defining the graph. 
```
_:lucy a :Person; :name"Lucy"; :bornIn_:idaho
_:idaho a : Location; :name "Idaho"; :type "state";
```
