# BFO-Official
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

This is the official repository for the Basic Formal Ontology (BFO) artifact specified in [ISO 21838-2:2020](https://www.iso.org/standard/74572.html), as well as the primary repository for the Basic Formal Ontology GitHub Organization. Here you will find the BFO User Guide, design patterns, implementations of BFO in formal languages, and artifacts used for validating BFO. 

BFO is a widely-used upper-level ontology that is conformant to the requirements specified in [ISO/IEC 21838‑1](https://www.iso.org/standard/71954.html) for top-level ontologies. Ontologies conformant to this standard promote interoperability among domain-level ontologies, thereby supporting the design and deployment of more specific ontology suites. 

## Directory Structure

    BFO User Guide - 
    BFO Design Patterns - 
    BFO Formalizations - 
    BFO Validation - 
    
## Versioning and Release Process

## Basic Formal Ontology Reading
For further information about the philosophical motivations for adopting terminological content represented in BFO, see [](). \
For further information about building ontologies using BFO artifacts and strategies, see [Building Ontologies with Basic Formal Ontology](https://mitpress.mit.edu/9780262527811/building-ontologies-with-basic-formal-ontology/). \
For information about upcoming and past events concerning BFO, see [NCOR](https://ncorwiki.buffalo.edu/index.php/Main_Page). 

## Development Team
[Barry Smith](https://www.buffalo.edu/cas/philosophy/faculty/faculty_directory/smith-b.html), SUNY Distinguished Professor of Philosophy and Julian Park Chair, University at Buffalo, Department of Philosophy\
[Alan Ruttenberg](https://dental.buffalo.edu/faculty/home.html?ubit=alanrutt), Director of Clinical and Translational Data Exchange, University at Buffalo\
[John Beverley](https://www.buffalo.edu/cas/philosophy/faculty/faculty_directory/john-beverley.html), Assistant Professor, University at Buffalo


# Taking Time Seriously
A long-standing issue among BFO users and developers has concerned how best to represent time. Importantly, issues concerning time in BFO stem from implementations of BFO in restricted formal languages such as the Web Ontology Language (OWL). OWL does not allow for direct representation of relations with arity higher than two. To illustrate the issue, consider modeling a vehicle having an engine part at some time, but losing that engine part at another. An expressive language such as First-Order Logic (FOL) would permit the following representation: 

    (1) has_part(vehicle, engine, time_1) & ~has_part(vehicle, engine, time_2)

Since FOL allows using ternary relations. OWL's restriction to at most binary relations precludes expressions like (1); indeed, there is no simple, straightforward way
to represent the content of (1) in OWL. Given the need to represent time and change in many domains and the wide use of OWL in ontology circles, proposals have been offered by users of BFO for representing such phenomena within the binary constraints of OWL. Examples include: 

    A. Temporalized Relations - 
    B. Temporally Qualified Continuants - 
    C. Temporal Stases - 
    D. Temporal Snapshots - 
    E. Temporal Annotations - 
    F. Minimal Temporality - 

Each is a plausible avenue of research in the interest of more rigorous representations of time in restricted formal languages. Details for each research project can be viewed in respective 'Temporal Profile' repositories contained in the BFO GitHub Organization. 

## Temporal Profiles 
BFO is a top-level, domain-neutral ontology, designed to consist of terminological content that spans most scientific disciplines. Classes such as Temporal Region, Temporal Instant, Temporal Interval, etc., seem well within scope. There are, however, reasons to refrain from providing significant constraints on time in BFO:

> 1. Scientific domains do not treat time uniformly. Economists, for example, measure economic constructs using time series, i.e. presuming a model of discrete time, whereas physicists typically treat time as continuous. This observation speaks in favor of BFO remaining neutral on questions over the discreteness of continuity of time. 
> 2. Not all scientific domains require a robust characterization of time, e.g. the domain of mathematics has no obvious need for time. 
> 3. Given community goals, even if users need some characterization of time, they do not always need a robust characterization of time, e.g. [Open Biological and Biomedical Ontology Foundry](https://obofoundry.org/) users have, for many years, employed a formally weak representation of time with great success.
    
This last point is worth belaboring. Deploying a BFO-based, robust, formalization of time can be costly, involving re-educating users, updating existing ontologies, perhaps even rewriting portios of codebases, etc. OBO users have not often had a need for such rigor, and so do not have a need to bear such costs. A charitable reading of early [criticisms](https://github.com/cmungall/trel-crit/raw/master/trc.pdf) of the Temporalized Relations strategy - which provides a rather robust formalization of time in BFO - makes just this point.  

On the other hand, there are reasons that speak in favor of providing formal guidance for modeling time in BFO:

> 4. Other foundry efforts, such as the [Industrial Ontology Foundry](https://www.industrialontologies.org/) which uses BFO as its top-level architecture, anticipate the need for a rigorous formalization of time.
> 5. [Recent work](https://pubmed.ncbi.nlm.nih.gov/36534832/) demonstrating the importance of rigorous axiomatization of ontologies used to supplement machine learning pipelines with minimal datasets, suggests rigorous BFO formalizations of time ontologies may be useful in such contexts. 

What these observations suggest is that while there are strong motivations for BFO providing - perhaps significant - guidance to users who require a robust formalization of time, imposing any specific formalization of time - such as the A - F proposals - on all users would be in some cases unnecessarily onerous. To satisfy needs of the community then, the BFO development team encourages a strategy of developing and deploying Temporal Profiles which will provide users options for representing time in their domains.

## Temporal Profile Implementation
Temporal Profiles should be implemented in a decidable flavor of OWL, such as OWL2. While terminological content differs across temporal profiles, developers are encouraged to abide by the following design principles: 

> 

## Temporal Profile Artifacts
Temporal Profile Artifacts are artifacts designed to represent extensions of the OWL formalization of BFO that impose axiom constraints concerning time and change. Temporal Profile Artifacts should be represented in some flavor of RDF, e.g. ttl, owl. 

With respect to BFO, the scope of Temporal Profiles should include treatment of classes and relationships that includes: 

> Temporal Region and subclasses \
> Spatiotemporal Region \
> Object properties relating to time, whether explicit or implicit 

Motivating use cases often vary based on domain and user community. We recommend developers use, as a starting point, design patterns and use cases concerning time and change found in the article [Basic Formal Ontology: Case Studies](https://philpapers.org/archive/OTTBBF.pdf). There the authors present seven design patterns based on the FOL implementation of BFO. 

## Temporal Profile Integration
Putting aside the varying relative maturity levels of each Temporal Profile, there is a further pressing question concerning interoperability. BFO is a top-level ontology designed to provide a common hierarchy across all scientific research; interoperability is its motivation. With this in mind, it is thus incumbent on developers to demonstrate not only that their preferred formalization of time conforms to BFO, but also that interpretations, formal mappings, or provable containments exists across strategies. This is, admittedly, a great deal of work, but it is a consequence of sustaining interoperability, a goal our community prizes. 

### Temporal Profiles Further Reading
[Temporally Qualified Continuants](https://jansenludger.github.io/home/Texte/TQC%20Freiburg8%20Proceedings.pdf) \
[Temporal Snapshots](https://oborel.github.io/obo-relations/temporal-semantics/) 


