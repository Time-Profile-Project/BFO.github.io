In natural language, descriptions of roles are often ambiguous between the occupants of roles and the roles themselves. For example, expressions like "Sam is a pharmacist" refer to both occupiers and role occupied. 

As discussed in the Design Pattern Hueristics document, as realizable entities, any instance of BFO _role_ should link an _independent continuant_ bearer (excepting _spatial region_) to a _process_. Sam's pharmacist role is to be defined in a manner that links Sam to processes one might expect of a pharmacist. More precisely and generally, for _role_ R, _independent continuant_ IC, and _process_ P, the bridge pattern is: 

IC bears R
R realized in P

Turning next to the occupants of roles, for an independent continuant that is an instance of a subclass B, the guidance is as follows: 

IC is a B that bears R

For example: 

Pharmacist =def Person that bears a pharmacist role.

Pharmacist Role =def Role that if realized, is realized in...

Adequate characterization of the relevant processes is often occupant dependent, in that some occupations are involved in more, and more nuanced, processes than others. 
