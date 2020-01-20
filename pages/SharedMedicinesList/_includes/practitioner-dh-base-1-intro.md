#### Base Practitioner *[[Active](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance
For the overarching usage scenarios in this implementation guide it is recommended that:
* an Australian address conforms to [AU Base Address](http://hl7.org.au/fhir/base/aubase1.1/StructureDefinition-au-address.html)
* an employee identifier local to an organisation, e.g. a hospital or lab, be sent with:
  * a type code of 'EI' 'http://terminology.hl7.org/CodeSystem/v2-0203'
  * the system will be filled with a namespace specific to the organisation, e.g. 'https://territorymedicalcentre.example.com/provider' or 'http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0/51824753556'
  * the value is the actual employee identifier in the organisation's system, e.g. 'frankburns27' or '123456'
  
This profile is referenced by [Base Patient](StructureDefinition-patient-dh-base-1.html), [My Health Record Patient](StructureDefinition-patient-mhr-1.html), [Patient with Mandatory Identifier](StructureDefinition-patient-ident-1.html),
[Base PractitionerRole](StructureDefinition-practitionerrole-dh-base-1.html), [Shared Medicines List Authored by Practitioner](StructureDefinition-composition-sml-prac-1.html), 
[Summary Statement of Allergy or Intolerance](StructureDefinition-allergyintolerance-summary-1.html),
[Assertion of No Relevant Finding](StructureDefinition-observation-norelevantfinding-1.html),
and [Medicine Item Statement](StructureDefinition-medicationstatement-detailed-1.html).
