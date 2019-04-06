---
layout: page
title:  "Consistency Rules"
permalink: "/consistencyrules/"
order: 2
---

{% capture folderpath %}
{{ site.url }}/{{ page.path | remove: page.name }}
{% endcapture %}

In this Section, we demonstrate the set of constraints for Ecore which we have yet defined and evaluated with ReVision. In the following, we represent the consistency rules and their descriptions by two kind of grammars: the Object Constraint Language (OCL) as defined by the [Object Managment Group](https://www.omg.org/spec/OCL/About-OCL/) and our First-Order Logic Language (FOL) that we've defined for ReVision.

* [The Attribute is not Transient So it must have a Data Type that is Serializable](#the-attribute-is-not-transient-so-it-must-have-a-data-type-that-is-serializable)
* [Two Features can not both be IDs](#two-features-can-not-both-be-ids)


### The Attribute is not Transient So it must have a Data Type that is Serializable

* An EAttribute of an EClass has an EDataType, e.g. volume : Integer
* An EAttribute has the property <transient>, which indicates (transient=true/false), if this EAttribute should be saved when saving the EClass.
* The EDataType (Integer) has a property <serializable>, which indicates (serializable=true/false), if values of this data type (e.g. 10, 30, …) can be saved in a XML file. 
* An EAttribute can only be not transient (transient=false), if the used data type is serializable (serializable=true).

<figure class="aligncenter">
	<a href="{{folderpath}}images/Folie2.PNG" target="_blank">
		<img style="width: 100%" src="{{folderpath}}images/Folie2.PNG"/>
	</a>
	<figcaption style="text-align: center">Example with Abstract Syntax Graph</figcaption>
</figure>

#### OCL Constraint

```
constraint TheAttributeIsNotTransientSoItMustHaveADataTypeThatIsSerializable
message 'The attribute is not transient so it must have a data type that is serializable'

context EAttribute

inv TheAttributeIsNotTransientSoItMustHaveADataTypeThatIsSerializable:
self.transient and self.eType.oclIsTypeOf(EDataType) implies (self.eType.oclAsType(EDataType).serializable)
```

#### FOL Constraint

```
constraint TheAttributeIsNotTransientSoItMustHaveADataTypeThatIsSerializable
message 'The attribute is not transient so it must have a data type that is serializable'

context EAttribute attribute : (
        isEqual(attribute.transient, false) and 
        isInstanceOf(attribute.eType, EDataType)
)
implies isEqual(attribute.eType.EDataType::serializable, true)
```

### Two Features can not both be IDs

* An EClass can have exactly one EAttribute which is defined as an ID property.

* (The same also applies for the set of all properties that will be passed down via inheritance!)


#### OCL Constraint




#### FOL Constraint



### A Class that is an Interface must also be Abstract

* An EClass has two boolean properties as flags: interface and abstract

* An EClass can be an interface: interface=true and abstract=true  in this case, both flags have to be true

* Or an abstract class: interface=false and abstract=true

* Or a concrete class: interface=false and abstract=false


#### OCL Constraint




#### FOL Constraint



### There may not be two Features named

* Two references or properties with the same name are not permitted in one EClass.

* (The same also applies for the set of all references or properties that will be passed down via inheritance!)


#### OCL Constraint




#### FOL Constraint



### A Container Reference must have UpperBound Of Not
 
* The containment references of an ecore (meta) model define the future syntax tree of a model instance.

* Optionally, to each containment reference, an opposed reference can be drafted.

* This opposed reference is called container reference.

* A container reference must always have a maximum upper bound of 1, because in a (syntax) tree a child 
    element may have maximum one parent element.


#### OCL Constraint




#### FOL Constraint



### A Containment or bidirectional Reference must be Unique if its UpperBound is different from 

* The property >unique< of an EReferenz indicates, that a list of references of a model instance must not contain duplicates. Within one model instance, an element may not be referenced repeatedly. 


#### OCL Constraint




#### FOL Constraint



### A Containment Reference of a Type with a Container Feature that requires Instances to be Contained elsewhere can not be populated

* An EClass with a unique container (container reference with upper bound = 1) can not have other alternate containers.

* (The same also applies for the set of all references that will be passed down via inheritance!)
    

#### OCL Constraint




#### FOL Constraint



### The Opposite Of a Containment Reference must not be a Containment Reference

* The containment references of an ecore (meta) model define the future syntax tree of a model instance.

* Optionally, to a containment reference an opposed reference can be drafted.

* This reference is called container reference.

* A container reference may not be defined as containment reference at the same time.

* In other words, opposed containment references may not exist.


#### OCL Constraint




#### FOL Constraint



### The Opposite of a Transient Reference must be Transient if it is Proxy Resolving

* The property >transient< of an EReference determine that references of a model instance will not be saved. 

* This property must be consistent for bidirectional references.



#### OCL Constraint




#### FOL Constraint



### The Opposite of the Opposite may not be a Reference different from this one

* A bidirectional reference in ecore always consists of a pair of references, not of a number of references!


#### OCL Constraint




#### FOL Constraint



### The Opposite may not be its own Opposite

* A bidirectional reference in ecore always consists of a pair of references, not of just one reference!

    

#### OCL Constraint




#### FOL Constraint


### The Default Value Literal must be a Valid Literal of the Attributes Type

* A default value can be defined for an EAttribute, e.g. state : PlayState = STOP.

* If the EDataType of a property is an EEnum (Enumeration: PlayState {PLAY, PAUSE, STOP}), then the default value has to match the name of an ELiterals (PLAY, PAUSE, STOP) of this EEnum.

* Alternatively, the default value can be empty (<null>).

* An empty string (<““>) is not permitted!

#### OCL Constraint




#### FOL Constraint



### There may not be two Operations and with the same Signature

* An Operation should always have unique specifications like: unique name, unique parameters and the other unique properties. Otherwise, It would be considered as an internal error or fault in the Ecore Framework which would be highlighted in red color.

* Another reason for this issue, is that each Operation should have a special purpose to be applied on a meta model or a part of it. So, The signature of an Operation is a very important issue to be considered, specially in the bigger and more complicated projects in which there are a lot of Operations a long side each other and some of them will probably have kind of overlapping based on their aims and they may look somehow similar. Thus, the signatures should be carefully defined to have kind of discrimination and not making any confusion or conflicts. 

* In addition, It is better to define an Operation based on the standards already referred in order to facilitate the readibility and scalability termics specially in the context of big projects . . .


#### OCL Constraint




#### FOL Constraint



### There may not be an Operation with the same Signature as an Accessor Method for Feature

* If an EClass has an EAttribute named e.g. “compression“, there may not be explicit EOperations which correlate the access methods for this EAttribute generated by ecore: setCompression, getCompression etc.

* Alternatively, the visibility of an operation can be suppressed for the generator by a special EAnnotation.

* (The same also applies for the set of all operations or properties that will be passed down via inheritance!) 





#### OCL Constraint




#### FOL Constraint



### There may not be two Parameters named

* Regarding the explanations depicted in the Operation context, An Operation should always have unique specifications like: unique name, unique parameters and the other unique properties. Otherwise, It would be considered as an internal error or fault in the Ecore Framework which would be highlighted in red color.

* Moreover, having multiple parameters with the same name is considered as a syntax error in EMF ecore models. 



#### OCL Constraint




#### FOL Constraint



### There may not be two Classifiers named

* It is also not permitted to have multiple Classifiers with the same name in EMF ecore models. Since the Classifiers are important model components to be instanciated or modified and stored in an arbitrary model in the model versioning systems such as git whenever needed, they should also be unique based on the standards of OMG like: having unique names, unique features, unique properties and so on, not to make any confusion or conflict. 


#### OCL Constraint




#### FOL Constraint



### The Typed Element must have a Type

* According to the ecore meta model standards, each EtypedElement must have an eType as the defined DataType like: EInt, EString, . . . Otherwise, It will be considered as a syntactic Error.


#### OCL Constraint




#### FOL Constraint



### The Required Feature of must be set

* According to the ecore meta model standards, each Feature (EAttribute) of an EClass should have a DataType. Otherwise, It will be considered as a syntactic Error.


#### OCL Constraint




#### FOL Constraint


### The Generic Type associated with the Classifier should have Type Arguments to match the number of Type Parameters of the Classifier

* According to the ecore meta model standards, each Generic Type associated with the Classifier should have Type Arguments to be matched with the number of the parameters of the Classifier.

* As it can be seen in the following diagram of the Ecore Generic Types meta model, the number of input Type Parameters of an Eoperation should be absolutely matched with the number of the input Type Parameters of a Classifier. Otherwise, a syntactic error will be appeared indicating the missing or redundant parameters of this Type Parameters sets comparison.



#### OCL Constraint




#### FOL Constraint


### The Generic Type associated with the Classifier must not have Arguments when the Classifier has Type Parameters

* According to the ecore meta model standards, each Generic Type associated with the Classifier should have Type Arguments to be matched with the number of the parameters of the Classifier. If the Type Parameters of a Classifier are not considered in accordance with the input parameters of an arbitrary Eoperation of that Classifier or in case of being null (Empty) for them, a syntactic error will be appeared indicating the missing or non-existent of the Parameters.

* As it can be seen in the following diagram of the Ecore Generic Types meta model, the number of input Type Parameters of an Eoperation should be absolutely matched with the number of the input Type Parameters of a Classifier. Otherwise, a syntactic error will be appeared indicating the missing or redundant parameters of this Type Parameters sets comparison.


#### OCL Constraint




#### FOL Constraint

