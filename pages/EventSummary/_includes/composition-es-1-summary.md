This profile contains the following variations from [AU Base Composition](http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-au-composition.html):

* One `meta.profile` is 'http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/composition-shs-1'
* Exactly one `language` is 'en-AU'
* Exactly one `composition-author-role` as 'PractitionerRole with Practitioner with Mandatory Identifier'
* `type` is 'Patient summary Document' (Details : {LOINC code '60591-5'})'
* `subject` as [Patient with Mandatory IHI](StructureDefinition-patient-ihi-1.html) 
* `author` as [Practitioner wth Mandatory Identifier](StructureDefinition-practitioner-ident-1.html)
* none `confidentiality`
* At least one `attester` 
* `attester` is sliced on value:mode
    * Exactly one `attester` slice 'Legal attester'
        *  `attester.mode` is 'legal'
        *  Exactly one `attester.time`
        *  Exactly one `attester.party` as [Practitioner wth Mandatory Identifier](StructureDefinition-practitioner-ident-1.html)
* `custodian` as [Organization with Mandatory Identifier](StructureDefinition-organization-ident-1)
* At least one `section`
* `section` is sliced on value:code
* invariant: inv-dh-cmp-02: The section shall at least have one entry or an empty reason, but not both
    * Exactly one `section` slice `Allergies`
        * Exactly one `section.title` is 'Allergies and Adverse Reactions'
        * Exactly one `section.code` is 'Allergies and adverse reactions Document' (Details: {LOINC code '48765-2'})
        * Exactly one `section.text`
        * `section.mode` is 'snapshot'
        * `section.entry` as [Summary Statement of Allergy or Intolerance](StructureDefinition-allergyintolerance-summary-1)
        * `section.emptyReason` [required](http://hl7.org/fhir/STU3/terminologies.html#required) binding to [Health Summary Non-Clinical Empty Reason](https://healthterminologies.gov.au/fhir/ValueSet/health-summary-non-clinical-empty-reason-1)
    * Exactly one `section` slice  'Medications'
        * invariants: 
            * inv-dh-cmp-03: This section shall not contain both summary statement of known medication entries and assertion of no relevant finding entries
            * inv-dh-cmp-04: This section shall contain at most one assertion of no relevant finding entry and it shall assert no current medications    
        * Exactly one `section.title` is 'Current Medications'
        *  Exactly one `section.code` is 'Current Medicine' (Details: {NCTIS Data Components code '101.32009'})
        *  Exactly one `section.text`
        *  `section.mode` is 'snapshot'
        *  `section.entry` as [Summary Statement of Known Medication](StructureDefinition-medicationstatement-summary-1), [Assertion of No Relevant Finding](StructureDefinition-observation-norelevantfinding-1)
        *  `section.emptyReason` [required](http://hl7.org/fhir/STU3/terminologies.html#required) binding to [Health Summary Non-Clinical Empty Reason](https://healthterminologies.gov.au/fhir/ValueSet/health-summary-non-clinical-empty-reason-1)
    * Exactly one `section` slice  'Medical History'
        * invariants: 
            * inv-dh-cmp-05: This section shall not contain both summary statements of medical history entries (condition or procedure) and assertions of no relevant finding entries
            * inv-dh-cmp-06: This section shall contain at most one assertion of no relevant finding entry and it shall assert no relevant medical history  
        *  Exactly one `section.title` is 'Medical History'
        *  Exactly one `section.code` is 'Medical History' (Details: {NCTIS Data Components code '101.16117'})
        * Exactly one `section.text`
        *  `section.mode` is 'snapshot'
        * `section.entry` as [Summary Statement of Condition](StructureDefinition-condition-summary-1), [Summary Statement of Known Procedure](StructureDefinition-procedure-summary-1) | [Assertion of No Relevant Finding](StructureDefinition-observation-norelevantfinding-1)
        *  `section.emptyReason` [required](http://hl7.org/fhir/STU3/terminologies.html#required) binding to [Health Summary Non-Clinical Empty Reason](https://healthterminologies.gov.au/fhir/ValueSet/health-summary-non-clinical-empty-reason-1)
    * Exactly one `section` slice  'Immunisations'
        * invariants:
            * inv-dh-cmp-07: This section shall not contain both summary statements of administered vaccine entries and assertions of no relevant finding entries
            * inv-dh-cmp-08: This section shall contain at most one assertion of no relevant finding entry and it shall assert no previous immunisations
        *  Exactly one `section.title` is 'Immunisations'
        *  Exactly one `section.code` is 'History of Immunization Narrative)' (Details: {LOINC code '11369-6'})
        *  Exactly one `section.text`
        *  `section.mode` is 'snapshot'
        *  `section.entry` as [Summary Statement of Administered Vaccine](StructureDefinition-immunization-summary-administration-1), [Assertion of No Relevant Finding](StructureDefinition-observation-norelevantfinding-1)
        * `section.emptyReason` [required](http://hl7.org/fhir/STU3/terminologies.html#required) binding to [Health Summary Non-Clinical Empty Reason](https://healthterminologies.gov.au/fhir/ValueSet/health-summary-non-clinical-empty-reason-1)