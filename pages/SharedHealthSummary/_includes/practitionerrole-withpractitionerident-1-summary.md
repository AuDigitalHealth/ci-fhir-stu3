
This profile contains the following variations from [AU Base PractitionerRole](http://hl7.org.au/fhir/StructureDefinition/au-practitionerrole):

* Exactly one `practitioner` as [Practitioner with Mandatory Identifier](StructureDefinition-practitioner-ident-1.html)
* `organization` as [Base Organization](StructureDefinition-organization-dh-base-1.html)
* `code.coding` slice, Open by value:system
    * Zero or more `code.coding` slice'ANZSCO codes'
    * Zero or more `code.coding` slice 'SNOMED CT Practitioner Role codes'   
