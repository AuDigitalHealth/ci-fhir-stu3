#### Patient with Mandatory Identifier *[[Active](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance
For the overarching usage scenarios in this implementation guide it is expected that:
<ul>
  <li>country of birth is sent in <a href="StructureDefinition-patient-ident-1-definitions.html#Patient.extension:birthPlace">extension:birthPlace</a></li>
  <li>a local identifier is sent with a <a href="http://ns.electronichealth.net.au/id/hpio-scoped/service-provider-individual/1.0/index.html">HPI-O scoped</a> or <a href="http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0/index.html">ABN-scoped</a> identifier namespace if there isn't a local namespace available (see the <a href="https://github.com/AuDigitalHealth/ci-fhir-r4/wiki/Frequently-Asked-Questions">FAQ</a> for more information)</li>
  <li>an IHI conforms to the <a href="StructureDefinition-patient-ident-1-definitions.html#Patient.identifier:ihiNumber">identifier:ihiNumber</a> slice and a maximum of one is sent</li>
  <li>an Australian address conforms to <a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-au-address.html">AU Base Address</a></li>
</ul>
 
This profile is referenced by [Shared Medicines List Authored by Practitioner](StructureDefinition-composition-sml-prac-1.html), 
[Summary of an Encounter for an Event](StructureDefinition-encounter-es-1.html), [List of Medicine Items with Change Information Authored by Practitioner](StructureDefinition-list-sml-pracchanges-1.html),
[Summary Statement of Allergy or Intolerance](StructureDefinition-allergyintolerance-summary-1.html), 
[Assertion of No Relevant Finding](StructureDefinition-observation-norelevantfinding-1.html), 
and [Medicine Item Statement](StructureDefinition-medicationstatement-detailed-1.html).