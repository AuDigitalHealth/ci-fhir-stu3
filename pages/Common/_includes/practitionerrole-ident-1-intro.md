## Practitioner Role with Mandatory Identifier

This profile builds on the details that have been defined by the HL7 Australia Australian Practitioner Role profile.

### Identifiers
#### HL7 AU defined identifiers
The following identifiers have been defined in the HL7 AU profile:
* Provider Number
* National Provider ATO Organisation Identifier
* Care Agency Employee Identifier
* Employee Number

#### An identifier is mandatory
* PractitionerRole.identifier is mandatory i.e. [1..*]

#### Yet to be defined within slices
* (nil)

#### Must Support
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.

The system SHALL be able to store and retrieve the following elements:
* identifier
* active
* period
* practitioner
* organization
* code
* specialty
* location
* healthcareService
* telecom
* availableTime
* availableTime.daysOfWeek
* availableTime.allDay
* availableTime.availableStartTime
* availableTime.availableEndTime
* notAvailable
* notAvailable.description
* notAvailable.during
* availabilityExceptions