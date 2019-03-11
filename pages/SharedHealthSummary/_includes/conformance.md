{:.no_toc}
<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->
* Do not remove this line (it will not be displayed)
{:toc}
# {{ page.title }}

### Conformance requirements
This specification describes how a SHS is implemented in FHIR, Release 3 (STU) . Any FHIR resource that claims conformance to a profile in this implementation guide, or any derived profile, shall meet these base requirements:
* It shall be a valid HL7 FHIR instance. In particular:
    * It shall conform to the FHIR, Release 3 (STU) [HL7FHIR3] standard.
    * It shall conform to the profile it claims conformance to including:
        * conforming to the requirements described on the corresponding profile or extension page of this implementation guide
        * conforming to the requirements in the base resource as specified in FHIR, Release 3 (STU) [HL7FHIR3]
        * conforming to the requirements in the base profile where the profile described in this implementation guide is derived from a base profile 
    * It shall conform to the requirements specified in the Must Support section below.

Derived profiles of the profiles described in this implementation guide may make additional rules that override this implementation guide:
* A derived profile shall be derived in accordance with the rules on profiling
* A FHIR resource that is conformant to the derived profile shall be conformant to the profile in this implementation guide it was derived from


### Must Support
[Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) flag is used to specify if an element in a profile must be supported or not. The profile should also include information on what kind of support is required from systems and applications wanting to claim conformance 
to the profile.

A must support flag, when present in this specification, is displayed as letter "S" with red background in the Flag column of the Differential and Snapshot views of a profile.

In the context of this implementation guide, must support SHALL be interpreted as follows: 

* The system SHALL be able to include the element when authoring a resource where data is available
* The system SHALL be able to store and retrieve the element
* The system SHALL be able to process resources containing the element


