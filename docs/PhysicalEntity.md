---
parent: Entities
title: biolink:PhysicalEntity
grand_parent: Classes
layout: default
---

# Class: PhysicalEntity


An entity that has material reality (a.k.a. physical essence).

URI: [biolink:PhysicalEntity](https://w3id.org/biolink/vocab/PhysicalEntity)


---

![img](http://yuml.me/diagram/nofunky;dir:TB/class/[PhysicalEssence],[BiologicalProcessOrActivity]-%20enabled%20by%200..%2A%3E[PhysicalEntity%7Cid(i):string;name(i):label_type;category(i):category_type%20%2B],[PhysicalEntity]uses%20-.-%3E[PhysicalEssence],[PhysicalEntity]%5E-[MaterialSample],[NamedThing]%5E-[PhysicalEntity],[NamedThing],[MaterialSample],[BiologicalProcessOrActivity])

---


## Parents

 *  is_a: [NamedThing](NamedThing.md) - a databased entity or concept/class

## Uses Mixins

 *  mixin: [PhysicalEssence](PhysicalEssence.md) - Semantic mixin concept.  Pertains to entities that have physical properties such as mass, volume, or charge.

## Children

 * [MaterialSample](MaterialSample.md) - A sample is a limited quantity of something (e.g. an individual or set of individuals from a population, or a portion of a substance) to be used for testing, analysis, inspection, investigation, demonstration, or trial use. [SIO]

## Referenced by class

 *  **[BiologicalProcessOrActivity](BiologicalProcessOrActivity.md)** *[enabled by](enabled_by.md)*  <sub>0..*</sub>  **[PhysicalEntity](PhysicalEntity.md)**

## Attributes


### Inherited from named thing:

 * [id](id.md)  <sub>REQ</sub>
    * Description: A unique identifier for a thing. Must be either a CURIE shorthand for a URI or a complete URI
    * range: [String](types/String.md)
    * in subsets: (translator_minimal)
 * [name](name.md)  <sub>REQ</sub>
    * Description: A human-readable name for a thing
    * range: [LabelType](types/LabelType.md)
    * in subsets: (translator_minimal)
 * [category](category.md)  <sub>1..*</sub>
    * Description: Name of the high level ontology class in which this entity is categorized. Corresponds to the label for the biolink entity type class.
 * In a neo4j database this MAY correspond to the neo4j label tag.
 * In an RDF database it should be a biolink model class URI.
This field is multi-valued. It should include values for ancestors of the biolink class; for example, a protein such as Shh would have category values `bl:Protein`, `bl:GeneProduct`, `bl:MolecularEntity`, ...
In an RDF database, nodes will typically have an rdf:type triples. This can be to the most specific biolink class, or potentially to a class more specific than something in biolink. For example, a sequence feature `f` may have a rdf:type assertion to a SO class such as TF_binding_site, which is more specific than anything in biolink. Here we would have categories {bl:GenomicEntity, bl:MolecularEntity, bl:NamedThing}
    * range: [CategoryType](types/CategoryType.md)
    * in subsets: (translator_minimal)