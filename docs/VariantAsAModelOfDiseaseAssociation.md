---
parent: Associations
title: biolink:VariantAsAModelOfDiseaseAssociation
grand_parent: Classes
layout: default
---

# Class: VariantAsAModelOfDiseaseAssociation




URI: [biolink:VariantAsAModelOfDiseaseAssociation](https://w3id.org/biolink/vocab/VariantAsAModelOfDiseaseAssociation)


---

![img](http://yuml.me/diagram/nofunky;dir:TB/class/[VariantToDiseaseAssociation],[SequenceVariant]%3Csubject%201..1-%20[VariantAsAModelOfDiseaseAssociation%7Crelation(i):uriorcurie;id(i):string;predicate(i):predicate_type;negated(i):boolean%20%3F],[VariantAsAModelOfDiseaseAssociation]uses%20-.-%3E[ModelToDiseaseAssociationMixin],[VariantAsAModelOfDiseaseAssociation]uses%20-.-%3E[ThingToDiseaseAssociationMixin],[VariantToDiseaseAssociation]%5E-[VariantAsAModelOfDiseaseAssociation],[ThingToDiseaseAssociationMixin],[SeverityValue],[SequenceVariant],[Publication],[OntologyClass],[Onset],[NamedThing],[ModelToDiseaseAssociationMixin],[FrequencyValue],[Agent])

---


## Parents

 *  is_a: [VariantToDiseaseAssociation](VariantToDiseaseAssociation.md)

## Uses Mixins

 *  mixin: [ModelToDiseaseAssociationMixin](ModelToDiseaseAssociationMixin.md) - This mixin is used for any association class for which the subject (source node) plays the role of a 'model', in that it recapitulates some features of the disease in a way that is useful for studying the disease outside a patient carrying the disease
 *  mixin: [ThingToDiseaseAssociationMixin](ThingToDiseaseAssociationMixin.md) - mixin class for any association whose object (target node) is a disease

## Referenced by class


## Attributes


### Own

 * [variant as a model of disease association➞subject](variant_as_a_model_of_disease_association_subject.md)  <sub>REQ</sub>
    * Description: A variant that has a role in modeling the disease.
    * range: [SequenceVariant](SequenceVariant.md)

### Inherited from association:

 * [association➞id](association_id.md)  <sub>REQ</sub>
    * Description: A unique identifier for an association
    * range: [String](types/String.md)
    * in subsets: (translator_minimal)
 * [association type](association_type.md)  <sub>OPT</sub>
    * Description: connects an association to the type of association (e.g. gene to phenotype)
    * range: [OntologyClass](OntologyClass.md)
 * [subject](subject.md)  <sub>REQ</sub>
    * Description: connects an association to the subject of the association. For example, in a gene-to-phenotype association, the gene is subject and phenotype is object.
    * range: [NamedThing](NamedThing.md)
 * [predicate](predicate.md)  <sub>REQ</sub>
    * Description: A high-level grouping for the relationship type. AKA minimal predicate. This is analogous to category for nodes.
    * range: [PredicateType](types/PredicateType.md)
 * [object](object.md)  <sub>REQ</sub>
    * Description: connects an association to the object of the association. For example, in a gene-to-phenotype association, the gene is subject and phenotype is object.
    * range: [NamedThing](NamedThing.md)
 * [relation](relation.md)  <sub>REQ</sub>
    * Description: The relation which describes an association between a subject and an object in a more granular manner. Usually this is a term from Relation Ontology, but it can be any edge CURIE.
    * range: [Uriorcurie](types/Uriorcurie.md)
 * [negated](negated.md)  <sub>OPT</sub>
    * Description: if set to true, then the association is negated i.e. is not true
    * range: [Boolean](types/Boolean.md)
 * [qualifiers](qualifiers.md)  <sub>0..*</sub>
    * Description: connects an association to qualifiers that modify or qualify the meaning of that association
    * range: [OntologyClass](OntologyClass.md)
 * [publications](publications.md)  <sub>0..*</sub>
    * Description: connects an association to publications supporting the association
    * range: [Publication](Publication.md)
 * [provided by](provided_by.md)  <sub>0..*</sub>
    * Description: connects an association to the agent (person, organization or group) that provided it
    * range: [Agent](Agent.md)

### Inherited from entity to feature or disease qualifiers mixin:

 * [severity qualifier](severity_qualifier.md)  <sub>OPT</sub>
    * Description: a qualifier used in a phenotypic association to state how severe the phenotype is in the subject
    * range: [SeverityValue](SeverityValue.md)
 * [onset qualifier](onset_qualifier.md)  <sub>OPT</sub>
    * Description: a qualifier used in a phenotypic association to state when the phenotype appears is in the subject
    * range: [Onset](Onset.md)

### Inherited from frequency qualifier mixin:

 * [frequency qualifier](frequency_qualifier.md)  <sub>OPT</sub>
    * Description: a qualifier used in a phenotypic association to state how frequent the phenotype is observed in the subject
    * range: [FrequencyValue](FrequencyValue.md)

### Inherited from variant to disease association:

 * [variant to disease association➞subject](variant_to_disease_association_subject.md)  <sub>REQ</sub>
    * Description: a sequence variant in which the allele state is associated in some way with the disease state
    * range: [NamedThing](NamedThing.md)
    * Example:    
 * [variant to disease association➞relation](variant_to_disease_association_relation.md)  <sub>REQ</sub>
    * Description: E.g. is pathogenic for
    * range: [Uriorcurie](types/Uriorcurie.md)
 * [variant to disease association➞object](variant_to_disease_association_object.md)  <sub>REQ</sub>
    * Description: a disease that is associated with that variant
    * range: [NamedThing](NamedThing.md)
    * Example:    

### Domain for slot:

 * [variant as a model of disease association➞subject](variant_as_a_model_of_disease_association_subject.md)  <sub>REQ</sub>
    * Description: A variant that has a role in modeling the disease.
    * range: [SequenceVariant](SequenceVariant.md)