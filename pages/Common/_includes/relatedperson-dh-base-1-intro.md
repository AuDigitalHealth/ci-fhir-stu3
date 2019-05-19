## Base Related Person

This profile builds on the patient administration details that have been defined by the HL7 Australia Australian Releated Person profile.

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
* patient
* relationship
* name
* telecom
* gender
* birthDate
* address
* photo
* period

#### Profile specific implementation guidance
* Medical Record Number: identifier system can be completed using the [HPI-O based Medical Record Identifier](http://ns.electronichealth.net.au/id/local/provider/1.0) namespace if an organisation does not have its own namespace and has an HPI-O. An example of the syntax using this namespace is "http://ns.electronichealth.net.au/id/local/medicalrecord/1.0/8003620000000000". The dummy HPI-O should be replaced with the assigning entity's own HPI-O.

#### Examples
The following examples have been added:
