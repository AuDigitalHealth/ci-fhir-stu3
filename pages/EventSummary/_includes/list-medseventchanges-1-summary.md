#### Normative changes in this profile
The following specific changes were made:
1. `List.status`
- fixed value: current
1. `List.mode`
- fixed value: snapshot
1. `List.code`
- fixed value: {"coding":[{"system":"http://loinc.org","code":"10160-0"}]}
1. `List.subject`
- constrained to the [Agency Patient with mandatory Identifier  profile](StructureDefinition-patient-ident-1.html).
1. `List.source`
- constrained to the [Agency Practitioner with mandatory Identifier  profile](StructureDefinition-practitioner-ident-1.html).
1. `List.entry.deleted`
- deleted cardinality changed from [0..1] to [0..0]
1. `List.emptyReason`
- emptyReason cardinality changed from [0..1] to [0..0]

