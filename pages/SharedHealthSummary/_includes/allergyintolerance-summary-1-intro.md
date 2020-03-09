#### Summary Statement of Allergy or Intolerance *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is expected that:
* verificationStatus will be 'unconfirmed' (including where a sending system does not clearly have this element) or 'confirmed' depending on the level of certainty
* clinicalStatus will be 'active'
* where a sending system can state that a patient does not have an allergy or category of allergies, an appropriate negation code (e.g. 716186003 \|No known allergy\| or 716184000 \|No known latex allergy\|) will be sent in AllergyIntolerance.code
* refutation is not expected to be handled except as above - an appropriate negation code in AllergyIntolerance.code and clinicalStatus of 'confirmed'
* where a sending system only has a substance available (e.g. 111088007 \|Latex\|) and not a statement of allergy or intolerance (e.g. 300916003 \|Allergy to latex\|), the substance will be sent in AllergyIntolerance.code and optionally in reaction.substance

This profile is referenced by [Shared Health Summary](StructureDefinition-composition-shs-1.html).
