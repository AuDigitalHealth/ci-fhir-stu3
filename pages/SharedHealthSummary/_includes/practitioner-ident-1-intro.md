#### Practitioner with Mandatory Identifier *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is recommended that:
* an Australian address conforms to [AU Base Address](http://hl7.org.au/fhir/base/aubase1.1/StructureDefinition-au-address.html)
* an employee identifier local to an organisation, e.g. a hospital or lab, be sent with:
  * a type code of 'EI' 'http://terminology.hl7.org/CodeSystem/v2-0203'
  * the system will be filled with a namespace specific to the organisation, e.g. 'https://territorymedicalcentre.example.com/provider' or 'http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0/51824753556'
  * the value is the actual employee identifier in the organisation's system, e.g. 'frankburns27' or '123456'

When sending a shared medicines list to the My Health Record system it is expected that:
* an HPI-I will be sent

This profile is referenced by [Shared Health Summary](StructureDefinition-composition-shs-1.html)
and [PractitionerRole with Practitioner with Mandatory Identifier](StructureDefinition-practitionerrole-withpractitionerident-1.html).
