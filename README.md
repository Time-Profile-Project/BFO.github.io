# Basic Formal Ontology
```mermaid
graph TD
    A(Entity) --> B(Continuant)
    A(Entity) --> C(Occurrent)
    B(Continuant) --> D(Specifically Dependent<br> Continuant)
    B(Continuant) --> E(Generically Dependent<br> Continuant)
    B(Continuant) --> F(Independent<br> Continuant)
    F(Independent<br> Continuant) --> G(Material Entity)
    F(Independent<br> Continuant) --> H(Immaterial<br> Entity)
    D(Specifically Dependent<br> Continuant) --> I(Quality)
    D(Specifically Dependent<br> Continuant) --> J(Realizable<br> Entity)
    I(Quality) --> K(Relational<br> Quality)
    J(Realizable<br> Entity) --> L(Role)
    J(Realizable<br> Entity) --> M(Disposition)
    M(Disposition) --> N(Function)
    H(Immaterial<br> Entity) --> O(Site)
    H(Immaterial<br> Entity) --> P(Spatial<br> Region)
    H(Immaterial<br> Entity) --> Q(Continuant Fiat<br> Boundary)
    Q(Continuant Fiat<br> Boundary) --> R(Fiat<br> Point)
    Q(Continuant Fiat<br> Boundary) --> S(Fiat<br> Surface)
    Q(Continuant Fiat<br> Boundary) --> T(Fiat<br> Line)
    P(Spatial<br> Region) --> U(One-Dimensional<br> Spatial Region)
    P(Spatial<br> Region) --> V(Two-Dimensional<br> Spatial Region)
    P(Spatial<br> Region) --> W(Three-Dimensional<br> Spatial Region)
    G(Material<br> Entity) --> X(Fiat Object Part)
    G(Material<br> Entity) --> Y(Object<br> Aggregate)
    G(Material<br> Entity) --> Z(Object)
    C(Occurrent) --> AA(Process)
    C(Occurrent) --> AB(Process<br> Boundary)
    C(Occurrent) --> AC(Temporal<br> Region)
    C(Occurrent) --> AD(Spatiotemporal<br> Region)
    AA(Process) --> AE(History)
    AC(Temporal<br> Region) --> AF(Zero-Dimensional<br> Temporal Region)
    AC(Temporal<br> Region) --> AI(One-Dimensional<br> Temporal Region)
    AF(Zero-Dimensional<br> Temporal Region) --> AG(Temporal<br> Instant)
    AI(One-Dimensional<br> Temporal Region) --> AH(Temporal<br> Interval)
   ```

This repository maintains the Basic Formal Ontology (BFO) artifact conformant to the requirements specified in [ISO/IEC 21838‑1](https://www.iso.org/standard/71954.html) for top-level ontologies. Ontologies conformant to this standard promote interoperability among domain-level ontologies, thereby supporting the design and deployment of more specific ontology suites. 

## Directory Structure

    BFO User Guide - 
    BFO Design Patterns - 
    BFO Formalizations - 
    BFO Validation - 
    BFO Temporal Extensions - 
    
## Versioning and Release Process


## Basic Formal Ontology Reading
For further information about building ontologies using BFO artifacts and strategies, see [Building Ontologies with Basic Formal Ontology](https://mitpress.mit.edu/9780262527811/building-ontologies-with-basic-formal-ontology/). \
For information about upcoming and past events concerning BFO, see [NCOR](https://ncorwiki.buffalo.edu/index.php/Main_Page). 

## Development Team
* [Barry Smith](https://www.buffalo.edu/cas/philosophy/faculty/faculty_directory/smith-b.html), SUNY Distinguished Professor of Philosophy and Julian Park Chair, University at Buffalo, Department of Philosophy
* [Alan Ruttenberg](https://dental.buffalo.edu/faculty/home.html?ubit=alanrutt), Director of Clinical and Translational Data Exchange, University at Buffalo
* [John Beverley](https://www.buffalo.edu/cas/philosophy/faculty/faculty_directory/john-beverley.html), Assistant Professor, University at Buffalo

