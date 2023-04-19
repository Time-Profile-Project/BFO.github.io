Though Basic Formal Ontology is an upper-level architecture concerned with terms at the highest level of generality, several design heuristics have been identified for using this artifact effectively. 

Design patterns, for example, can be extracted from successful ontology development work using BFO. 

Here, we have curated general design heuristics that find use across specific BFO design patterns. The BFO design pattern documentation references these heuristics throughout. Additionally, in many cases these heuristics encapsulate general ontology design principles, which should be no surprise given the putative breadth of BFO. 

Lastly, in the interest of harmonizing with other efforts, observe that some of the general heuristic advice here overlaps with the very useful [OOPS!](https://oops.linkeddata.es/) ontology pitfall scanner.  

All-Some Rule
Adding axioms to classes in OWL imposes the following quantification structure: All x related to some y, by default. For example, to say that Mammal has the class restriction 'has organ' 'Lung' is to say that all instances of Mammal bear the object property 'has organ' to some instance of the class 'Lung'. Care should be taken to ensure such relationships are true. Consider, if the restriction was on 'Lung' to the effect that instances of this class were related by 'organ of' to Mammal, the result would be the claim that all instances of 'Lung' are organ of some instance of 'Mammal', whcih is false. 

Example: []()
Example: []()

Object Properties Only Relate Instances
To assert an object property holds between two classes is simply to assert it holds between instances of these classes. All object properties in OWL-DL relate instances to instances. 

This is of course not true when ascending to OWL-Full, where instances may be related to classes directly. Such modeling may be useful when, for example, one needs to represent that instances of a class are not ever related to instances of another class. One cannot simply use the OWL negative property assertion property, since this only asserts that two instances are not related. 

BFO ontology mdoeling is restricted to OWL-DL, but that does not mean we cannot capture the preceding use case, only that we need to appeal to tools other than OWL. In this case, a natural solution is to define a constraint using the Shapes Constraint Language (SHACL) enforcing that no instances of these classes stand in such a relation. From a graph-theoretic perspecive, this is just to say that BFO extended with instances never results in a model where these classes are bridged by that property. No need to extend beyond OWL-DL. 

Example: []()
Example: []()

Treating Classes as Instances and Vice Versa
Classes are repeatable; instances are not. Instances are data; classes are schema. 

As a rule of thumb, when reflecting on whether a resource should be a class or instance, ask how many of the entity there can be. There was only one Da Vinci, but many other painters. There is only one Armenia, but many countries. 

Example: Countries treated as classes []()
Example: Scales treated as instances []()

