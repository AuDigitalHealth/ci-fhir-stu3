## Base Practitioner

This profile builds on the details that have been defined by the HL7 Australia Australian Practitioner profile.

### Identifiers
#### HL7 AU defined identifiers
The following identifiers have been defined in the HL7 AU profile:
* Healthcare Provider Identifier - Individual (HPI-I)
* Medicare Prescriber Number 

#### Agency defined identifiers
The following identifiers have been added into the Agency profile:
* Employee Number

#### Yet to be defined within slices
* (nil)

#### Must Support
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.

The system SHALL be able to store and retrieve the following elements:
* identifier
* active
* name
* telecom
* address
* gender
* birthDate
* photo
* qualification
* qualification.identifier
* qualification.code
* qualification.period
* qualification.issuer
* communication
	
### Profile specific implementation guidance
#### Employee Number:
* identifier.system can be completed using [HPI-O scoped Employee Number](http://ns.electronichealth.net.au/id/hpio-scoped/service-provider-individual/1.0) namespace if an organisation does not have its own namespace and has a HPI-O. An example of the syntax using this namespace is: "http://ns.electronichealth.net.au/id/hpio-scoped/service-provider-individual/1.0/8003620000000000/frankburns27". The dummy HPI-O and local identifier should be replaced with the organisation's HPI-O and the local identifier respectively. 
* identifier.system can be completed using [ABN or ACN scoped Employee Number](http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0) namespace if an organisation does not have its own namespace and has a registered Australian Business Number (ABN) or Australian Company Number (ACN). An example of the syntax using this namespace is "http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0/51824753556/frankburns27". The dummy ABN and local identifier should be replaced with the organisation's ABN and the local identifier respectively.  

#### Known Issues
The must support flag is missing for the below elements. When the must support is added to any of these elements the IG Publisher breaks. This issue has been logged in Jira [CIFMM-1580](https://jira.nehta.net.au/browse/CIFMM-1580).
* qualification.identifier
* qualification.code
* qualification.period
* qualification.issuer - This element will be constrained to Agency Organization Base profile after the issue is fixed.