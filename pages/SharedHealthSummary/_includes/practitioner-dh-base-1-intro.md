#### Base Practitioner *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Usage scenarios
The following are the usage scenarios expected:

* Details of a practitioner exchanged as a referenced entry in a composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 


##### Implementation guidance
* Employee Number:
    * identifier.system can be completed using [HPI-O scoped Employee Number](http://ns.electronichealth.net.au/id/hpio-scoped/service-provider-individual/1.0) namespace if an organisation does not have its own namespace and has a HPI-O. An example of the syntax using this namespace is: "http://ns.electronichealth.net.au/id/hpio-scoped/service-provider-individual/1.0/8003620000000000/frankburns27". The dummy HPI-O and local identifier should be replaced with the organisation's HPI-O and the local identifier respectively. 
    
    * identifier.system can be completed using [ABN or ACN scoped Employee Number](http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0) namespace if an organisation does not have its own namespace and has a registered Australian Business Number (ABN) or Australian Company Number (ACN). An example of the syntax using this namespace is "http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0/51824753556/frankburns27". The dummy ABN and local identifier should be replaced with the organisation's ABN and the local identifier respectively.  


##### Known issues
* Due to a tolling issue the must support flag is missing for the below elements:
    * qualification.identifier
    
    * qualification.code
    
    * qualification.period
    
    * qualification.issuer 


