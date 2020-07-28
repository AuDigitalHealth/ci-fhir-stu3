#### My Health Record Patient *[[Active](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*


#### Implementation guidance
For the overarching usage scenarios in this implementation guide it is expected that:
<ul>
  <li>country of birth is sent in <a href="StructureDefinition-patient-ident-1-definitions.html#Patient.extension:birthPlace">extension:birthPlace</a></li>
  <li>a local identifier is sent with a <a href="http://ns.electronichealth.net.au/id/hpio-scoped/service-provider-individual/1.0/index.html">HPI-O scoped</a> or <a href="http://ns.electronichealth.net.au/id/abn-scoped/service-provider-individual/1.0/index.html">ABN-scoped</a> identifier namespace if there isn't a local namespace available (see the <a href="https://github.com/AuDigitalHealth/ci-fhir-r4/wiki/Frequently-Asked-Questions">FAQ</a> for more information)</li>
</ul> 

This profile is referenced by [Shared Medicines List Authored by Practitioner](StructureDefinition-composition-sml-prac-1.html),
and [List of Medicine Items with Change Information Authored by Practitioner](StructureDefinition-list-sml-pracchanges-1.html).