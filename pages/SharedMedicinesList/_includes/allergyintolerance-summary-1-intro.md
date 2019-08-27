#### Summary Statement of Allergy or Intolerance *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the overarching usage scenarios in this implementation guide:

* It is expected that verificationStatus will be ‘unconfirmed’ (where a sending system does not clearly have this element this should be the value sent), but may be ‘confirmed’
* It is expected that clinicalStatus will be ‘active’
* Where a sending system only has substance or agent available and not a statement of allergy or intolerance that substance should be sent in the code and optionally in reaction.substance
*  A refuted allergy or intolerance should be represented with an appropriate negation code (e.g. 716184000 \|No known latex allergy\|) and a verificationStatus of ‘unconfirmed’ or ‘confirmed’ depending on the level of certainty

