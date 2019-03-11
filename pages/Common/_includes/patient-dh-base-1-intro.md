## Base Patient 

This profile builds on the patient administration details that have been defined by the HL7 Australia Australian Patient profile.

### Identifiers
#### HL7 AU defined identifiers
The following identifiers have been defined in the HL7 AU profile:
* Individual Healthcare Identifier (IHI)
* Medicare Number
* DVA (Department of Veterans' Affairs) Number
* Health Care Card Identifier (which utilises the Centrelink Reference Number (CRN))
* Pensioner Concession Card Identifier (which utilises the Centrelink Reference Number (CRN))
* Commonwealth Seniors Health Card Identifier (which utilises the Centrelink Reference Number (CRN))
* Medical Record Number
* Private Health Insurance Member Number

#### Yet to be defined within slices
* [Medicare Safety net number](StructureDefinition-identifier-safetynetnumber.html)

#### Must Support
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.

The system SHALL be able to store and retrieve the following elements:
* identifier
* active
* name
* telecom
* gender
* birthDate
* birthDate.accuracy-indicator
* birthDate.birthTime
* deceased
* deceased.deceasedBoolean
* deceased.deceasedDateTime
* address
* maritalStatus
* multipleBirth
* photo
* contact
* contact.relationship
* contact.name
* contact.telecom
* contact.address
* contact.gender
* contact.organization
* contact.period
* communication
* communication.language
* communication.preferred
* generalPractitioner
* managingOrganization
* birthPlace
* indigenous-status
* closing-the-gap-registration
* patient-mothersMaidenName

#### Profile specific implementation guidance
* Medical Record Number: identifier.system can be completed using the [HPI-O based Medical Record Identifier](http://ns.electronichealth.net.au/id/local/provider/1.0) namespace if an organisation does not have its own namespace and has an HPI-O. An example of the syntax using this namespace is "http://ns.electronichealth.net.au/id/local/medicalrecord/1.0/8003620000000000". The dummy HPI-O should be replaced with the assigning entity's own HPI-O.

#### Known Issues
* Patient.deceasedDateTime.date-accuracy-indicator: The must support flag is missing. When the must support is added to the "Patient.deceasedDateTime.date-accuracy-indicator" the IG Publisher breaks. This issue has been logged in Jira [CIFMM-1265](https://jira.nehta.net.au/browse/CIFMM-1265), Zulip [Seeking advice on troubleshooting error with IG Publisher](https://chat.fhir.org/#narrow/stream/99-IG-creation/topic/Seeking.20advice.20on.20troubleshooting.20error.20with.20IG.20Publisher) and with HL7 GForge [#17165](https://gforge.hl7.org/gf/project/fhir/tracker/?action=TrackerItemEdit&tracker_item_id=17165).