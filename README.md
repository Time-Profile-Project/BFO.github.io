# BFO-Official

```mermaid
graph TD
    A(Entity) --> B(Continuant)
    A(Entity) --> C(Occurrent)
    B(Continuant) --> D(Specifically Dependent<br> Continuant)
    B(Continuant) --> E(Generically Dependent<br> Continuant)
    B(Continuant) --> F(Independent Continuant)
    F(Independent Continuant) --> G(Material Entity)
    F(Independent Continuant) --> H(Immaterial Entity)
    D(Specifically Dependent<br> Continuant) --> I(Quality)
    D(Specifically Dependent<br> Continuant) --> J(Realizable Entity)
    I(Quality) --> K(Relational Quality)
    J(Realizable Entity) --> L(Role)
    J(Realizable Entity) --> M(Disposition)
    M(Disposition) --> N(Function)
    H(Immaterial Entity) --> O(Site)
    H(Immaterial Entity) --> P(Spatial Region)
    H(Immaterial Entity) --> Q(Continuant Fiat Boundary)
    Q(Continuant Fiat<br> Boundary) --> R(Fiat Point)
    Q(Continuant Fiat<br> Boundary) --> S(Fiat Surface)
    Q(Continuant Fiat<br> Boundary) --> T(Fiat Line)
    P(Spatial Region) --> U(One-Dimensional<br> Spatial Region)
    P(Spatial Region) --> V(Two-Dimensional<br> Spatial Region)
    P(Spatial Region) --> W(Three-Dimensional<br> Spatial Region)
    G(Material Entity) --> X(Fiat Object Part)
    G(Material Entity) --> Y(Object Aggregate)
    G(Material Entity) --> Z(Object)
    C(Occurrent) --> AA(Process)
    C(Occurrent) --> AB(Process Boundary)
    C(Occurrent) --> AC(Temporal Region)
    C(Occurrent) --> AD(Spatiotemporal Region)
    AA(Process) --> AE(History)
    AC(Temporal Region) --> AF(Zero-Dimensional<br> Temporal Region)
    AC(Temporal Region) --> AI(One-Dimensional<br> Temporal Region)
    AF(Zero-Dimensional<br> Temporal Region) --> AG(Temporal Instant)
    AI(One-Dimensional<br> Temporal Region) --> AH(Temporal Interval)
   ```

This is the official repository for the Basic Formal Ontology (BFO) artifact specified in [ISO 21838-2:2020](https://www.iso.org/standard/74572.html), as well as the primary repository for the Basic Formal Ontology GitHub Organization. Here you will find the BFO User Guide, design patterns, implementations of BFO in formal languages, and artifacts used for validating BFO. 

BFO is a widely-used upper-level ontology that is conformant to the requirements specified in [ISO/IEC 21838‑1](https://www.iso.org/standard/71954.html) for top-level ontologies. Ontologies conformant to this standard promote interoperability among domain-level ontologies, thereby supporting the design and deployment of more specific ontology suites. 

### Directory Structure

    BFO User Guide - 
    BFO Design Patterns - 
    BFO Formalizations - 
    BFO Validation - 

### Taking Time Seriously
A long-standing issue among BFO users and developers has concerned how best to represent time. Importantly, issues concerning time in BFO stem from implementations of BFO in restricted formal languages. To see the issue, consider modeling a vehicle having an engine part at some time, but losing that engine part at another. 
Representing BFO using a language with the expressivity of, say, First-Order Logic, this could be expressed as - roughly:

    (1) has_part(vehicle, engine, time_1) & ~has_part(vehicle, engine, time_2)

In words, the vehicle has an engine part at time_1, but does not have an engine part at time_2. Here we have taken advantage of the fact that FOL allows using ternary relations; at most binary relations, however, are permitted in restrictive languages, such as the Web Ontology Language (OWL), in the interest of maintaining decidability of the language. This is to say, there is no straightfoward representation of the content of (1) in OWL. Given the need to represent time and change in many domains, proposals have been developed for representing such phenomena within the binary constraints of OWL. Examples include: 

    A. Temporalized Relations - 
    B. Temporally Qualified Continuants - 
    C. Temporal Stases - 
    D. Temporal Snapshots - 
    E. Temporal Annotations - 

For each proposal, there are benefits and costs worth investigating. Each is a plausible avenue of research in the interest of more rigorous representations of time in restricted formal languages. More detailed expositions and details on current advances in these research projects can be viewed in respective 'Temporal Profile' repositories contained in the BFO GitHub Organization. 

Motivation for Temporal Profiles of BFO stems in part from recognizing that rigorously representing time is more relevant to some domains than others, and more useful for researchers than to others. As an extreme example, consider than representing the domain of mathematics - rather than the practice - a careful formalizatin of time is arguably unnecessary. For a less extreme example, consider that while users in the [Open Biological and Biomedical Ontology Foundry](https://obofoundry.org/) have a need to represent time, and do so using a combination of BFO and the [Relations Ontology](https://obofoundry.org/ontology/ro.html), users have - for many years - employed a formally weak representation of time with great success. Indeed, a charitable reading of early [criticisms](https://github.com/cmungall/trel-crit/raw/master/trc.pdf) of the Temporalized Relations proposal is simply that rigorously formalizing time involves significant labor, OBO users do not have a need for such rigor, and so do not have a need to labor. On the other hand, consider that the [Industrial Ontology Foundry](https://www.industrialontologies.org/) which uses BFO as its top-level architecture, anticipates needing a rigorous formalization of time, and adopts the Temporalized Relations strategy for that reason. Moreover, given [recent work](https://pubmed.ncbi.nlm.nih.gov/36534832/) demonstrating the importance of rigorous axiomatization of ontologies to supplementing machine learning pipelines with minimal datasets, ontologies extending BFO used in such pipelines may find rigorous formalizations of time palatable. 

In summary then, it is not the case that all BFO users require a rigorous characterization of time. That nevertheless leaves an open question for users who do require an implementation of BFO characterizing time in restricted languages like OWL. At present, this is an open research project for BFO developers and collaborators. Alan Ruttenberg has produced an impressive formalization of the Temporalized Relations strategy, semi-[formal characterizations](https://jansenludger.github.io/home/Texte/TQC%20Freiburg8%20Proceedings.pdf) of the Temporally Qualified Continuants strategy have been developed, and members of the Relations Ontology have [endorsed](https://oborel.github.io/obo-relations/temporal-semantics/) the Temporal Snapshot strategy. 

Putting aside the varying relative maturity levels of each strategy, there is a further pressing question concerning interoperability. BFO is a top-level ontology designed to provide a common hierarchy across all scientific research; interoperability is its motivation. With this in mind, it is thus incumbent on developers to demonstrate not only that their preferred formalization of time conforms to BFO, but also that interpretations, formal mappings, or provable containments exists across strategies. This is, admittedly, a great deal of work, but it is a consequence of sustaining interoperability, a goal our community prizes. 


### Further Reading
For further information about the philosophical motivations for adopting terminological content represented in BFO, see [](). 
For further information about building ontologies using BFO artifacts and strategies, see [Building Ontologies with Basic Formal Ontology](https://mitpress.mit.edu/9780262527811/building-ontologies-with-basic-formal-ontology/). 
For information about upcoming and past events concerning BFO, see [NCOR](https://ncorwiki.buffalo.edu/index.php/Main_Page). 

### BFO Development Team
[Barry Smith](https://www.buffalo.edu/cas/philosophy/faculty/faculty_directory/smith-b.html), SUNY Distinguished Professor of Philosophy and Julian Park Chair, University at Buffalo, Department of Philosophy\
[Alan Ruttenberg](https://dental.buffalo.edu/faculty/home.html?ubit=alanrutt), Director of Clinical and Translational Data Exchange, University at Buffalo\
[John Beverley](https://www.buffalo.edu/cas/philosophy/faculty/faculty_directory/john-beverley.html), Assistant Professor, University at Buffalo
