## Summary Statement of Administered Vaccine

The purpose of this profile is to provide a summary statement for an administration of a vaccine. It is intentional that detailed information has not been included; this is intended to be a short summary.

#### Must Support
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.

The system SHALL be able to store and retrieve the following elements:
* status
* notGiven
* vaccineCode
* patient
* date
* primarySource
* vaccinationProtocol
* vaccinationProtocol.doseSequence
* vaccinationProtocol.doseStatus

#### Implementation guidance

* For the usage scenario for this profile, it is expected that status will be ‘completed’.
* For the usage scenario for this profile, it is expected that primarySource will be ‘true’.
* Where an authoring system does not have the dose status available as a distinct element it is expected that Dose Status Not Available will be sent {"system":"http://hl7.org/fhir/v3/NullFlavor","code":"NAVU","display":"Not available"}