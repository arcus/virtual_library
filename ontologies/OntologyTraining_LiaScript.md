<!--
title: Ontologies

@comment

Labeling, the process for adding annotations to data, helps us understand data in a more meaningful way by allowing us to better analyze and use it for our purposes. Consistent and correct data annotation preserves information integrity across different datasets and makes them interoperable with other AI systems, reducing errors that lead to misclassification or misinterpretation of data by AI algorithms. Utilizing an existing or creating your own ontology is a key component of the best practices to follow in the creation of labeled data.

This training is a supplemental training to the Checklist for Creating a Gold-Standard Annotated Dataset for your Research Project focusing specifically on ontologies. It is encouraged to be taken if, after completing the Checklist training, you need additional information on ontologies. 

@end


@learning_objectives  

At the end of this module, you will emerge with the knowledge of: 

- What an ontology is, and why it should be used instead of a taxonomy
- Three existing ontologies that are available for use
- How to create and manage your own ontology

@end

language: en
mode: Textbook

link:  https://cdn.jsdelivr.net/gh/arcus/virtual_library@main/assets/styles.css
import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros.md
-->

## Ontologies

![Side-by-side comparison of taxonomy and ontology structures: taxonomy shown as a strict hierarchical tree, ontology shown as a network of concepts connected through multiple relationship types.](media/Ontologies_OntovsTax.png)

Ontologies are a foundational component of the annotation process. While taxonomies and ontologies are both used to organize knowledge, they differ significantly in how they represent information and relationships between concepts. Understanding these differences is important when selecting or creating terminology for labels as part of the development of annotation guidelines. 
In this module, you will learn: 
- How ontologies extend beyond simple hierarchical classification,
- Why ontologies are preferred for annotation projects,
- Three existing ontologies that are available for use, and
- The key considerations involved in creating and maintaining your own ontology.

### What is a Taxonomy?

A taxonomy is a hierarchical classification system used to categorize and organize information into groups and sub-groups. It is often thought of as a structured way of grouping entities based on shared characteristics represented as a tree-like structure where each note is a category or subcategory.

_Key Characteristics:_

- Hierarchical Structure: Tree structure with parent-child relationships.
- Simple Relationships: Captures broad to narrow terms, not usually capturing complex interrelationships between categories.
- Fixed Vocabulary: Can be less flexible in accommodating new or unforeseen concepts.

_Generic Taxonomy Diagram_

![Example Diagram of a Taxonomy](media/Ontology_TaxonomyDesign.png)

### What is an Ontology?

An ontology is a complex, flexible framework used to model the relationships between entities and their properties, providing a rich, formal representation of knowledge within a domain, capturing not only the hierarchy, but also the various relationships between concepts. An ontology essentially connects taxonomies, capturing the interrelationships among entities to provide rich information.

_Key Characteristics:_

- Rich Relationships: Multiple types of relationships between concepts represented (parent-child, part-whole, etc.) in addition to including properties and constraints that define how entities interact.
- Formal Representation: Often use formal languages to provide precise definitions and infer logical relationships.
- Dynamic Vocabulary: Adaptable to allow for the inclusion of new concepts and relationships.

_Generic Ontology Chart_

![Example Diagram of an Ontology Chart](media/Ontology_OntologyChart.png)

### What is a Knowledge Graph?

A knowledge graph is a graph-based data representation connecting real-world entities through explicitly modeled relationships that humans and systems can naturally understand. The core parts of the graph consist of: 
- Nodes: The entities, concepts, or classes of the graph.
- Edges: The relationship or connection between the nodes, indicating ownership, membership, dependency, interaction, etc.
- Properties: The property keys that describe nodes or relationships, allowing the graph to store both facts and contextual attributes, reflecting how information is naturally connected. 

**Why is this important when we are talking about taxonomies and ontologies? Because knowledge graphs act as the operational layer, bringing taxonomies and ontologies to life by defining how the graph data is organized and interpreted.**

A knowledge graph can capture taxonomies using nodes and relationships that represent hierarchical structures. It can also capture ontologies using semantic nodes, relationships, and properties to provide meanings and logic. They become the organizing principles that provide meaning and structure to the knowledge graph.

The "Generic Ontology Chart" seen on the **What is an Ontology** page is an example of an Ontology being represented as a knowledge graph. Here is another example of a knowledge graph: 

![Example Diagram of a Knowledge Graph](media/Ontology_KnowledgeGraph.png)
A knowledge graph captures instance data as nodes, relationships, and properties, while using taxonomies and ontologies as organizing principles.

### Why Ontology and Not Taxonomy

An ontological approach captures connections naturally as most knowledge and concepts do not exist in isolation as they do in most taxonomies.

- Ontologies adapt easily to evolving ideas without rebuilding the system
- Relationships are clearly defined
- Connections revealed that might otherwise be missed via a taxonomy
- AI thrives on interconnected data

### So What?

As determining key terms for labels is one of the first steps in creating Annotation Guidelines, it is important to know if you will be utilizing an existing ontology or creating your own for the project. Below is information on three existing ontologies that you can utilize as well as information on creating your own ontology if the existing ones do not meet your needs. HPO and SNOMED are already available in the BRAT annotation tool within Arcus labs. For a larger listing of existing Biomedical Ontologies, [see this resource](https://guides.lib.umich.edu/ontology/ontologies#:~:text=ICD%20-%20International%20Classification%20of%20Diseases,Nomenclature%20of%20Medicine-Clinical%20Terms) from the University of Michigan.

**Important note to remember when considering utilizing an existing ontology versus creating your own: Building a custom ontology for data annotation often leads to isolated data that cannot connect with global health records. On the other hand, using a standard ontology like SNOMED CT or the Human Phenotype Ontology (HPO) saves time, ensures consistency, and helps other researchers understand the annotated data easier and fosters more collaborations.**

### Knowledge Check: Ontologies

1. Which statement best distinguishes an ontology from a taxonomy?

[( )] A. A taxonomy can express multiple relationship types, while an ontology cannot  
[(X)] B. An ontology is a richer formal model that can express multiple relationship types and constraints; a taxonomy is typically a simple hierarchical classification  
[( )] C. Taxonomies always include inference capabilities and OWL semantics  
[( )] D. Ontologies are always flat lists of terms  
***

<div class = "answer">

While taxonomies are hierarchical and relatively simple, ontologies are more complex, essentially modeling connections between taxonomies. Therefore, they cannot be merely a flat list of terms! And _ontologies_ have inference capabilities, not taxonomies.   

</div>

*** 

2. True or false: Ontologies improve computability and interoperability by providing formal definitions, relationships, and constraints.

[(X)] True  
[( )] False  
***

<div class = "answer">

Ontologies model relationships in a rich, complex, interconnected way that can be greatly leveraged by machines. 

</div>

***

3. You should prefer an ontology over a simple label list when: (Select all that apply.)

[[X]] A. Relationships between concepts (e.g., is-a, part-of) are important to downstream analysis  
[[X]] B. You need computable definitions to support reasoning or mapping across vocabularies  
[[ ]] C. The project only requires a short, fixed hierarchical label list with no relationships  
[[X]] D. Reuse and interoperability with other datasets or EHR systems are goals  
***

<div class = "answer">

If you have a simple project that only requires a short, fixed hierarchical label list with no relationships, a taxonomy could be sufficient. In all of these other cases, an ontology would be more appropriate. 

</div>

***

## Existing Ontologies
![Three cards detailing existing ontologies used in biomedical research: HPO, SNOMED and UMLS. EAch has its own card with matching icon](media/Ontologies_Exisisting.png)

Building a custom ontology for data annotation often leads to isolated data that cannot connect with global health records. On the other hand, using a standard ontology like SNOMED CT or the Human Phenotype Ontology (HPO) saves time, ensures consistency, and helps other researchers understand the annotated data easier and fosters more collaborations.

Detailed here are three existing ontologies that you could use as the ontology for the key terms for your labels in your annotation project: HPO, SNOMED CT, and the Unified Medical Language System (UMLS). Keep in mind when reviewing these ontologies on their websites, they are not shown in a knowledge graph format. However, that graph representation can be applied to capture the nodes, edges, and properties, to help you better understand the structure of the ontology being used in your project. 

### HPO

The [Human Phenotype Ontology (HPO)](https://hpo.jax.org/) project provides an ontology of medically relevant phenotypes, disease-phenotype annotations, and the algorithms that operate on these. The HPO can be used to support differential diagnostics, translational research, and a number of applications in computational biology by providing the means to _compute_ over the clinical phenotype. The HPO is being used for computational deep phenotyping and precision medicine as well as integration of clinical data into translational research. [Deep phenotyping](https://www.ncbi.nlm.nih.gov/pubmed/22504886) can be defined as the precise and comprehensive analysis of phenotypic abnormalities in which the individual components of the phenotype are observed and described. The HPO is being increasingly adopted as a standard for phenotypic abnormalities by diverse groups such as international rare disease organizations, registries, clinical labs, biomedical resources, and clinical software tools and will thereby contribute toward nascent efforts at global data exchange for identifying disease etiologies.

The HPO currently contains over 18,000 terms arranged in a directed acyclic graph and are connected by is-a (subclass-of) edges, such that a term represents a more specific or limited instance of its parent term(s). All relationships in the HPO are is-a relationships, i.e. simple class-subclass relationships. For instance, [_Abnormal lens morphology_](https://hpo.jax.org/browse/term/HP:0000517) is-a [_Abnormal eye morphology_](https://hpo.jax.org/browse/term/HP:0012372). The relationships are transitive, meaning that they are inherited up all paths to the root. [_Phenotypic abnormality_](https://hpo.jax.org/browse/term/HP:0000118) is the main subontology of the HPO and contains descriptions of clinical abnormalities. Additional subontologies are provided to describe inheritance patterns, onset/clinical course, and modifiers of abnormalities.

### SNOMED

[SNOMED International](https://www.snomed.org/) is a not-for-profit organization that owns, administers, and develops [SNOMED CT](https://snomedbrowser.org/?). SNOMED CT is a comprehensive, multilingual clinical healthcare terminology resource with scientifically validated clinical content, enabling consistent representation of clinical content in the electronic health records.

The SNOMED CT logical model defines the way in which each type of SNOMED CT component and derivative is related and represented. The core component types in SNOMED CT are concepts, relationships, and descriptions.

**_Concepts_**

Every concept represents a unique clinical meaning, which is referenced using a unique, numeric, and machine-readable SNOMED CT identifier. The identifier provides an unambiguous unique reference to each concept and does not have any ascribed human interpretable meaning.

**_Relationships_**

A relationship represents an association between two concepts. Relationships are used to logically define the meaning of a concept in a way that can be processed by a computer. A third concept, called a relationship type (or attribute), is used to represent the meaning of the association between the source and destination concepts. There are different types of relationships available within SNOMED CT.

**_Descriptions_**

Descriptions are the human readable terms that are associated with clinical ideas. Each description has a description type and may be marked "preferred for use" in particular languages or dialects. A fully specified name (FSN) is a type of description which uniquely and fully captures the meaning of the clinical idea. Synonyms are descriptions that allow the same concept to be expressed in different ways, each of which are associated with the same concept ID.

### UMLS

The [Unified Medical Language System (UMLS)](https://www.nlm.nih.gov/research/umls/index.html) is a collection of files and software developed by the National Library of Medicine that enables interoperability across biomedical computer systems. At its core, is the UMLS Metathesaurus, a large biomedical thesaurus organized by concept, which serves as a bridge connecting over [200 source vocabularies](https://www.nlm.nih.gov/research/umls/sourcereleasedocs/), including SNOMED CT, HPO, ICD-10, RxNORM, etc., by linking synonymous terms to shared concepts. This means a clinician's SNOMED CT code, and a geneticist's HPO term can be recognized as referring to the same underlying concept, allowing seamless traversal across vocabularies. The Metathesaurus preserves each vocabulary's original meanings, concept meanings and relationships while surfacing cross vocabulary connections through a unified concept identifier (CUI) system. The [UMLS Metathesaurus Browser](https://uts.nlm.nih.gov/uts/umls/home) is a web interface for searching and exploring these linked concepts and their relationships interactively.

If you have not already done so, you need to submit a license request to the UMLS Metathesaurus in order to access it. You can do this by: 
1. Visiting the [login page](https://uts.nlm.nih.gov/uts/signup-login) and selecting "Research Organization" under the identity provider list
2. Searching for "Children's Hospital of Philadelphia"
3. Accepting the Terms & Conditions for the License Agreement
4. Filling out the required fields on the License form

You will receive an email once access has been granted.  

### Knowledge Check: Existing Ontologies

4. Which resource aggregates many biomedical vocabularies and provides mappings across them via unified concept identifiers?

[( )] A. HPO  
[( )] B. SNOMED CT  
[(X)] C. UMLS  
[( )] D. Protégé  
***

<div class = "answer">

UMLS serves as a bridge across more than 200 biomedical vocabularies by linking synonymous concepts through a unified concept identifier (CUI) system. This allows concepts from systems such as HPO and SNOMED CT to be mapped together. Protégé is an ontology editing tool, not a vocabulary resource. 

</div>

***

5. Which of the following describe the relationships in the HPO? Select all that apply. 

[[X]] A. Is-a
[[ ]] B. Part-of
[[X]] C. Class-subclass
[[X]] D. Transitive
***

<div class = "answer">

HPO relationships are simple "is-a"/class-subclass relationships which are also transitive (inherited up all paths to the root). While "part-of" relationships exists in many ontologies, they do not exist in the HPO. 

</div>

***

6. True or false: SNOMED CT is primarily designed as a comprehensive clinical terminology for EHR interoperability.

[(X)] True  
[( )] False


## Creating an Ontology 

There is no one-way or comprehensive methodology that you can always use that covers everything you could need when developing an ontology. Generally speaking, you can follow the below steps to guide you through the process:

1. Determine the domain and scope of the ontology

    - To determine the domain and scope, start with a few basic questions such as:

      - What is the domain of the ontology?
      - What are we using the ontology for?
      - What answers should the ontology provide us with?
      - Who will use this ontology?

2. Consider reusing existing ontologies

    - In some cases, you have the benefit of reusing an existing ontology that was developed by someone else for similar purposes to your own, in these cases you could simply extend those ontologies to better suit your needs.

3. Enumerate important terms in the ontology

    - You need to understand the scope of the ontology in terms of what you want to define and work with. To this end, you need to come up with terms that you would like to make statements about or explain to users.

4. Define the classes and class hierarchy

    - A class is a collection of instances.
    - For the creation of a class hierarchy, there are three choices:
      
      - Top-down: Identify most general classes first and then work to specifics
      - Bottom-up: Identify specifics first and then work to general classes
      - Combination
  
5. Define the properties of classes

    - Now that classes and high-level concepts have been defined, they need detail.
    - By using properties, you are able to describe the internal structure of your classes
    - Example: 


<img src="media/Ontology_ClassProperties.png" style="width: 40%; margin-right: 4%; display: inline-block; vertical-align: top;" alt="Classes and their properties/slots." />


6. Define the facts of the properties (Properties can also be referred to as slots)

    - Important aspects to consider regarding the properties include:

      - Value Type: Is it a string, number, Boolean, enumeration, instance of another class?
      - Property cardinality: How many values does the property have?
      - Range: Instance properties are when an instance of another class is used as a property in another class; these properties often only allow certain instances of another class, and these instances are specified in a range. 
      - Domain: Refers to the classes to which a property is attached or classes which a property describes.

    - Example:

![Properties](media/Ontology_Properties.png)

7. Create Instances

    - Create individual instances of the classes that were previously defined:

      - Choose a class
      - Create an individual instance of that class
      - Fill in the property values

    - Example:

![Instances of classes](media/Ontology_ClassInstances.png)

_Note: In ontologies, properties and classes form a hierarchy and inherit the properties/slots of the classes above them._

For more detailed information on the steps outlined, view [Ontology Development 101: A Guide to Creating Your First Ontology](https://protege.stanford.edu/publications/ontology_development/ontology101.pdf).

### Knowledge Check: Creating an Ontology 

7. Before building a new ontology, it is recommended to consider reusing or ______ an existing ontology.

[[extending]]
<script>
let input = "@input".trim().toLowerCase()

input == "extending" || input == "extend"
</script>
***

<div class = "answer">

Given their complexity, building a new ontology requires a significant investment of time and effort. Therefore, where possible, extending an existing ontology to meet your needs can be more efficient. 

</div>

***

8. Which steps are important when creating a practical ontology for annotation projects? (Select all that apply.)

[[X]] A. Define domain and scope  
[[ ]] B. Omit documentation to keep the ontology compact  
[[X]] C. Enumerate terms and build class hierarchy  
[[X]] D. Define properties (domain, range, cardinality) and document semantics  
***

<div class = "answer">

When creating an ontology, define your domain and scope (why are you building the ontology?), defining your terms and building your class hierarchy, and defining the properties of your classes are all steps in the ontology creation process. Omitting documentation might make the ontology compact, but will ultimately make it more difficult to understand, maintain, reuse, and share. 

</div>

***

9. When constructing classes and properties, top-down, bottom-up, or ______ approaches are commonly used (one word).

[[combination]]
<script>
let input = "@input".trim().toLowerCase()

input == "combination"
</script>
***

<div class = "answer">

A combination approach to constructing classes and properties incorporates elements of both top-down and bottom-up approaches. 

</div>

***

## Managing an Ontology 

![Three circles depicting the three steps in managing an ontology: Adding the term, editing is, and deprecating it when needed. Each has corresponding icon.](media/Ontologies_Managing.png)

Managing an ontology is an important part of the process whether you are utilizing an existing ontology or creating your own. Detailed here are widely used tools, including Protégé, PoolParty, and BRAT, to help you do this, in addition to noting the importance of adding, editing, and deprecating Terms.

### Tools

Several ontology editing tools are available to support the creation and management of ontologies, with [Protégé](https://protege.stanford.edu/) and [PoolParty](https://www.poolparty.biz/) being among the most widely used. Both tools provide a visual interface for defining classes, relationships, and hierarchies, and support standard ontology formats such as [OWL](https://www.w3.org/TR/owl2-overview/) and [SKOS](https://www.w3.org/TR/skos-reference/). Protégé is a free, open-source option well suited to building and editing ontologies from scratch, while PoolParty offers additional enterprise features such as taxonomy management, version control, and integration with data pipelines.

If you are using an ontology for clinical note annotation within an Arcus lab, you will need to integrate it with the [BRAT annotation tool](https://brat.nlplab.org/). BRAT provides a visual interface for annotating text spans with ontology terms and defining relationships between them. Your ontology terms and relationship types are managed through BRAT's configuration files, which must be updated whenever terms are added or changed in your ontology. [See this guide](https://forum.arcus.chop.edu/t/note-annotator-guidelines/221) for more information about using BRAT with clinical notes in Arcus.

### Adding, Editing, and Deprecating Terms

Managing ontology terms over time involves three core activities: adding new terms, updating existing ones, and deprecating those that are no longer needed. New terms should only be added when they represent a clearly defined concept not already covered by the ontology, and should follow a consistent naming and definition convention established by your team. Updates to existing terms, such as revised definitions or relationships, should be documented with a rationale to maintain transparency. Rather than deleting outdated terms, deprecated terms should be marked as obsolete and retained in the ontology to preserve the integrity of any existing annotations that reference them.

Within Arcus labs, it is recommended to maintain your ontology terms, relationships, and definitions in GitHub, a web-based platform that uses Git to track changes to files over time, including files edited collaboratively by a team. GitHub is particularly well suited to ontology management because every change is automatically recorded in the repository history, eliminating the need to manually number or rename files to track versions. When making changes, it is helpful to distinguish between major updates (such as significant restructuring of classes or relationships) and minor updates (such as small definition edits) noting these differences in your commit messages. Consistent file naming conventions should be established from the outset within GitHub that is useful, consistent and well documented, [see this resource](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/fileNaming_bestPractices_MIT.pdf) for more information.

### Knowledge Check: Managing an Ontology

10. Which of the following is the best practice when removing or changing terms that have already been used in annotations?

[( )] A. Delete the old term immediately to prevent future use  
[(X)] B. Mark the term obsolete/deprecated, retain it in version history, and document the change  
[( )] C. Rename silently without notifying annotators  
[( )] D. Remove all annotations that used the term  
***

<div class = "answer">

Marking a removed or changed term and documenting the change preserves the integrity of existing annotations and the historical record. Deleting the old term can break existing annotations and can "change history". If this removal is silent, it can also confuse other annotators. Removing all annotations that used the old term will eliminate "broken" annotations, but at the cost of potentially valuable data. 

</div>

***

11. Version control (e.g., GitHub) and clear commit messages are recommended for managing ontology files and changes.

[(X)] True  
[( )] False  
***

<div class = "answer">

Version control allows changes to the ontology to be preserved in the historical record, with supports transparency. Clear commit messages ensure that changes are well-documented and able to be understood by collaborators, now and in the future. 

</div>

***

12. Which free/open-source tool is recommended for building and editing OWL ontologies?

[( )] A. Excel  
[(X)] B. Protégé  
[( )] C. Photoshop  
[( )] D. ArcGIS  
***

<div class = "answer">

Protégé a free, open-source ontology editor that supports standard ontology formats such as OWL and is well suited for creating and editing ontologies.

</div>

***

## Sources

Bice, B. (2025, July 28). Why ontology and not taxonomy. _International Legal Technology Association_. <https://www.iltanet.org/blogs/william-bice/2025/07/28/why-ontology-and-not-taxonomy>

De Jager, B. (2024, July 23). Ontology engineering for beginners - Part 1. _Medium_. <https://medium.com/@brucedej/ontology-engineering-for-beginners-part-1-69a01df66caa>

De Jager, B. (2024, August 3). Ontology engineering for beginners - Part 2. _Medium_. <https://medium.com/@brucedej/ontology-engineering-for-beginners-part-2-f0cdac19ab16>

Doubleday, K. (2024, September 4). Taxonomies versus ontologies: A short guide. _Fluree_. <https://flur.ee/fluree-blog/taxonomies-versus-ontologies-a-short-guide/>

Earley Information Science. (n.d.). _What is the difference between taxonomy and ontology?_ <https://www.earley.com/insights/what-difference-between-taxonomy-and-ontology-it-matter-complexity>

Gargano, M.A., Matentzoglu, N., Coleman, B., Addo-Lartey, E.B., Anagnostopoulos, A.V., Anderton, J., Avillach, P., Bagley, A.M., Bakštein, E., Balhoff, J.P., Baynam, G., Bello, S.M., Berk, M., Bertram, H., Bishop, S., Blau, H., Bodenstein, D.F., Botas, P., Boztug, K., Cady, J., ... Robinson, P.N.. (2024). The Human Phenotype Ontology in 2024: phenotypes around the world. _Nucleic Acids Res, 52_(D1), D1333-D1346. <https://doi.org/10.1093/nar/gkad1005>

Graph.Build. (n.d.). _Ontologies explained_. <https://graph.build/resources/ontology>

Kempe, S. (2017, October 17). Taxonomy vs ontology: Machine learning breakthroughs. _Dataversity_. <https://www.dataversity.net/articles/taxonomy-vs-ontology-machine-learning-breakthroughs/>

Laubheimer, P. (2022, July 3). Taxonomy 101: Definition, best practices, and how it complements other IA work. _Nielsen Norman Group_. <https://www.nngroup.com/articles/taxonomy-101/>

Noy, N.F., & McGuinness, D.L. (n.d.). Ontology development 101: A guide to creating your first ontology. _Stanford University_. <https://protege.stanford.edu/publications/ontology_development/ontology101.pdf>

OBO Foundry. (n.d.). _Principles: Overview_. <https://obofoundry.org/principles/fp-000-summary.html>

Ontology (information science). (2026, May 4). In Wikipedia. <https://en.wikipedia.org/wiki/Ontology\_(information_science]>

SNOMED International. (n.d.). _SNOMED_. <https://www.snomed.org/>

Stegeman, J. (2026, June 16). Taxonomy vs. ontology vs. knowledge graph: What's the difference? _Neo4j_. <https://neo4j.com/blog/knowledge-graph/taxonomy-vs-ontology-vs-knowledge-graph/>

University of Michigan Library. (2026, April 17). Biomedical ontologies and controlled vocabularies. _Library Research Guides_. <https://guides.lib.umich.edu/ontology/ontologies>

Wu, H. (2025, December 29). Knowledge graph vs ontology: Know the difference. _PuppyGraph_. <https://www.puppygraph.com/blog/knowledge-graph-vs-ontology>
