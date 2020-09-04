# Chapter-2: Data Models and Query Languages

## General

1. Schema can be 
   1. Explicit (Enforced at write) - Relational
   2. Implicit (handled at read) - Document & Graph

   
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
## Graph databases compared to Network Model

| Parameter | Network Model | Graph |
|----------|--------------|--------|
| Schema | Has Schema | No Schema|
| Reaching a record | Start with access path  | Using vertex uniqueId or use index to find vertices with a value |
| New record position | DB maintains order -> consequences | No ordering -> Require sorting during query|
| Query language| Imperative | Have both Imperative and Declarative | 


## Datalog 
1. Foundation language on which later query languages were build. 
2. `(Subject, Predicate, Object)` => `Predicate (Subject, Object)`

# Summary
1. 3 Types of widely adopted data model today
   1. Document
   2. Relational
   3. Graph
2. Each one has its own characterstics and application should choose 1 based on its need. 
3. Each data model provides its own query language. 
