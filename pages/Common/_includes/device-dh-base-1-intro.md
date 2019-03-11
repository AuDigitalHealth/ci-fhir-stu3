## Base Device

This profile builds on the details that have been defined by the HL7 Australia Australian Device profile.

### Identifiers
#### HL7 AU defined identifiers
The following identifiers have been defined in the HL7 AU profile:
* My Health Record (PCEHR) Assigned Identity for Devices (PAI-D)

#### Yet to be defined within slices
* (nil)

#### Must Support
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.

The system SHALL be able to store and retrieve the following elements:
* identifier
* udi
* udi.deviceIdentifier
* udi.name
* udi.jurisdiction
* udi.carrierHRF
* udi.carrierAIDC
* udi.issuer
* udi.entryType
* status
* type
* lotNumber
* manufacturer
* manufactureDate
* expirationDate
* model
* version
* patient
* owner
* contact
* location
* url
* note
* safety

#### Known Issues
* When the value of "Device.type" is any value other than "Example" i.e. "Required", "Preferred" or "Extensible", the IG Publisher produces an additional link of "(unbound)" in the "Differential Table" and "Snapshot Table" displays. This issue has been logged in Jira [CIFMM-1347](https://jira.nehta.net.au/browse/CIFMM-1347), Zulip  [Additional "(unbound)" link when not "Example"](https://chat.fhir.org/#narrow/stream/99-IG-creation/topic/Additional.20.22(unbound).22.20link.20when.20not.20.22Example.22) and with HL7 GForge [#17117](https://gforge.hl7.org/gf/project/fhir/tracker/?action=TrackerItemEdit&tracker_item_id=17117). 