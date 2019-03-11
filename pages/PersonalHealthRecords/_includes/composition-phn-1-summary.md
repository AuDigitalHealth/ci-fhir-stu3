This structure is derived from the [Agency Consumer Entered Information Document Header profile](StructureDefinition-composition-docheader-cei-1.html)

This profile introduces the following variations from the above profile:
1. One `meta.profile` is "http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/composition-phn-1"
1. `type` with fixed value system="https://healthterminologies.gov.au/fhir/CodeSystem/nctis-data-components-1", code="100.16681" 
1. `title` is "Personal Health Notes"
1. Exactly one `section`
1. Exactly one `section.title`
1. Exactly one `section.code` with fixed value system="https://healthterminologies.gov.au/fhir/CodeSystem/nctis-data-components-1", code="102.15513"
1. Exactly one `section.text`
1. `mode` is "snapshot"
1. Zero `emptyReason` (explicitly prohibited)