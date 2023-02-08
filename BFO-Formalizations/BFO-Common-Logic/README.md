# BFO Common Logic Implementation

In comformance with [ISO 21838-2:2020](https://www.iso.org/standard/74572.html), BFO classes and relations are represented in Common Logic - a First-Order Logic framework for a family of formal languages, specified in [ISO 24707:2007](https://www.iso.org/standard/39175.html). Representation of BFO in Common Logic facilitates interoperability with projects such as [COLORE](https://github.com/gruninger/colore), use with theorem prover tools such as the [Heterogeneous Tool Set](http://hets.eu/), and prolog libraries such as [cltools](https://github.com/cmungall/cltools). 

[ISO 21838-2:2020](https://www.iso.org/standard/74572.html) specifies three 'dialects' of Common Logic - Common Logic Interchange Format (CLIF), Conceptual Graph Interchange Format (CGIF), and XML Common Logic. Representation of BFO in Common Logic uses the CLIF dialect. 

### Directory Content

This directory consists of files containing axioms written in CLIF that reflect modules of BFO. For example, the file continuant-mereology.cl contains axioms characterizing BFO mereology relations defined over continuant entities in BFO. Of note is the file universal-declaration.cl which provides defines the hierarchical structure of BFO and formal identification of universals. 

Most users of BFO will likely not have a need for using the Common Logic representation. The content of this repository will likely be of most use to those interested in, say, using automated model checking tools, evaluating logical consistency of BFO, comparing the formal structure of BFO to other upper-level ontologies, or of course seeing confirmation that BFO satisfies the formal requirements for top-level ontologies outlined in [ISO 21838-1:2020](https://www.iso.org/standard/71954.html). 
