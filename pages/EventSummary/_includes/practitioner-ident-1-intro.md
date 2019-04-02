### Practitioner with Mandatory Identifier *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios
The following are the usage scenarios expected:

* Details of a practitioner with an identifier exchanged as referenced entry in a composition, list, or standalone record. 

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 


#### Implementation guidance
* Employee Number:
    * identifier.system can be completed using [HPI-O scoped Employee Number](http://ns.electronichealth.net.au/id/hpio-scoped/service-provider-individual/1.0) namespace if an organisation does not have its own namespace and has a HPI-O. An example of the syntax using this namespace is: "http://ns.electronichealth.net.au/id/hpio-scoped/service-provider-individual/1.0/8003620000000000/frankburns27". The dummy HPI-O and local identifier should be replaced with the organisation's HPI-O and the local identifier respectively. 
    * identifier.system can be completed using [ABN or ACN scoped Employee Number](http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0) namespace if an organisation does not have its own namespace and has a registered Australian Business Number (ABN) or Australian Company Number (ACN). An example of the syntax using this namespace is "http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0/51824753556/frankburns27". The dummy ABN and local identifier should be replaced with the organisation's ABN and the local identifier respectively.  

#### Known issues
* Due to a tolling issue the must support flag is missing for the below elements:
    * qualification.identifier
    * qualification.code
    * qualification.period
    * qualification.issuer 
 
#### Examples
This section provides examples that conform to the requirements specified within this implementation guide.

* [Practitioner example 1](Practitioner-40a94071-8373-4d53-a788-63b79c75a3c1.html)
* [Practitioner example 2](Practitioner-40a94071-8373-4d53-a788-63b79c75a3c1.html)

Sample instances are also included within [Shared Health Summary](StructureDefinition-composition-shs-1.html) example instances:
* [Composition SHS example 1 (with contained resources)](Composition-a0da969a-7956-439b-b390-8de071a2df7c.html)
* [Composition SHS example 2 (with contained resources)](Composition-bd06e981-ba86-4020-ba59-cd89f80e8712.html)
* [Composition SHS example 3 (with contained resources)](Composition-c53c6c39-3e1a-4038-9ad5-25be8c54481f.html)