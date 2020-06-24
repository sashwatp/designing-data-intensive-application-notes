# Chapter-2: Data Models and Query Languages

## Relational Model vs Document Model



## Triple-Stores and SPARQL

1. All information is stored in the form `(Subject, Predicate, Object)`. Eg: `(Jim, likes, Banana)`
   1. Objects can either be a key value like `(lucy, age, 33)` or another vertex in the graph like `(lucy, marriedTo, alain)`
2. The Resource Description Framework (RDF) -> was intended to present data in a consistent format so that data from different websites can be combined into a graph. 
   1. Turtle (example below) is an example of RDF data. Similarly, XML can also be used for defining the graph. 
```
_:lucy a :Person; :name"Lucy"; :bornIn_:idaho
_:idaho a : Location; :name "Idaho"; :type "state";
```

## The SPARQL query language
1. Query language for triple-stores using RDF data model. 
2. Much more consice compared to Cypher

```sql
SELECT ?personName WHERE {
    ?person:name ?personName.
    ?person :bornIn / :within / :name "United State"
    ?person :liveIn / :within / :name "Europe"
}
```
### Graph databases compared to Network Model

| Parameter | Network Model | Graph |
|----------|--------------|--------|
| Schema | Has Schema | No Schema|
| Reaching a record | Start with access path  | Using vertex uniqueId or use index to find vertices with a value |
| New record position | DB maintains order -> consequences | No ordering -> Require sorting during query|
| Query language| Imperative | Have both Imperative and Declarative | 
