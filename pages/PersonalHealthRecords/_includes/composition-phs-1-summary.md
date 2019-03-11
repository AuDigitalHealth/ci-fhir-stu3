This structure is derived from the [Agency Consumer Entered Information Document Header profile](StructureDefinition-composition-docheader-cei-1.html)

This profile introduces the following variations from the above profile:
1. One `meta.profile` is "http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/composition-phs-1"
1. `type` with fixed value system="https://healthterminologies.gov.au/fhir/CodeSystem/nctis-data-components-1", code="100.16685" 
1. `title` is "Personal Health Summary"
1. At least one `section`, sliced Unordered, Closed by value:code
1. slice `section:allergies`
    * exactly one
    * invariant such that 'The section shall at least have one entry or an empty reason'
    * exactly one `title` with fixed value 'Allergies and Adverse Reactions'
    * exactly one `code` with fixed coding system='http://loinc.org' and code='48765-2'
    * exactly one `text`
    * `mode` fixed to 'snapshot'
    * `entry` sliced Unordered, Open by profile:resolve()
    * `entry` invariant such that 'At least one allergy statement shall be present'
    * `entry:allergyIntolerance` slice as Summary Statement of Allergy or Intolerance
    * `emptyReason` [required](http://hl7.org/fhir/STU3/terminologies.html#code) binding to [Health Summary Non-Clinical Empty Reason](https://healthterminologies.gov.au/fhir/ValueSet/health-summary-non-clinical-empty-reason-1) value set
1. slice `section:medications`
    * exactly one
    * invariant such that 'The section shall at least have one entry or an empty reason'
    * exactly one `title` with fixed value 'Current Medications'
    * exactly one `code` with fixed coding system='https://healthterminologies.gov.au/fhir/CodeSystem/nctis-data-components-1' and code='101.32009'
    * exactly one `text`
    * `mode` fixed to 'snapshot'
    * `entry` sliced Unordered, Open by profile:resolve()
    * `entry` invariant such that 'At least one allergy statement shall be present'
    * `entry:medication` slice as Summary Statement of Known Medication
    * `entry:noRelevantFindingMedication` slice as Assertion of No Relevant Finding
    * `emptyReason` [required](http://hl7.org/fhir/STU3/terminologies.html#code) binding to [Health Summary Non-Clinical Empty Reason](https://healthterminologies.gov.au/fhir/ValueSet/health-summary-non-clinical-empty-reason-1) value set