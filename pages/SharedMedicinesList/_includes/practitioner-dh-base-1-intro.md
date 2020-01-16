#### Base Practitioner *[[Active](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance
For the overarching usage scenarios in this implementation guide it is recommended that:
* an Australian address conforms to [AU Base Address](http://hl7.org.au/fhir/base/aubase1.1/StructureDefinition-au-address.html)
* an employee identifier local to an organisation, e.g. a hospital or lab, be sent with:
  * a type code of 'EI' 'http://terminology.hl7.org/CodeSystem/v2-0203'
  * the system will be filled with a namespace specific to the organisation, e.g. 'https://territorymedicalcentre.example.com/provider' or 'http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0/51824753556'
  * the value is the actual employee identifier in the organisation's system, e.g. 'frankburns27' or '123456'
  
This profile is referenced by [Base Patient](http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/patient-dh-base-1), [My Health Record Patient](http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/patient-mhr-1), [Patient with Mandatory Identifier](http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/patient-ident-1),
[Base PractitionerRole](http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/practitionerrole-dh-base-1), 
[Summary Statement of Allergy or Intolerance](http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/allergyintolerance-summary-1),
[Assertion of No Relevant Finding](http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/observation-norelevantfinding-1),
and [Medicine Item Statement](http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/medicationstatement-detailed-1).
