## Medicare Records FHIR Implementation Guide

### Approved for external use


{:.no_toc}

{% include publish-box.html %}


<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}

<!-- end TOC -->

This implementation guide is an Australian realm implementation guide of the HL7<sup>TM</sup> FHIR<sup>&reg;</sup> specification to represent atomic Medicare records in the My Health Record system and related applications.

This [implementation guide](http://hl7.org/fhir/STU3/implementationguide.html) is based on [FHIR<sup>&reg;</sup> version 3.0.1](http://hl7.org/fhir/STU3/index.html).

### Scope

#### Use Cases
The following is the expected scenario:
* DHS Medicare sends Medicare records to the My Health Record system

#### Profiles
The FHIR<sup>&reg;</sup> profiles that form part of this implementation guide are shown below. The profiles defined in this implementation guide do not include profile-specific mappings to another format. The base FHIR<sup>&reg;</sup> STU3 mapping content for each of the resources referenced in this implementation guide can be found on the applicable resource documentation in the [FHIR Release 3 (STU)](http://hl7.org/fhir/STU3/index.html).

Profiles that define representation of Pharmaceutical Benefits Schedule (PBS) claim items or Medicare Benefits Schedule (MBS) claim items: 
* [Explanation of Benefit Medicare](StructureDefinition-explanationofbenefit-medicare.html)
* [Medication Request Pharmaceutical Benefits Scheme](StructureDefinition-medicationrequest-pbs.html)
* [Medication Pharmaceutical Benefits Scheme](StructureDefinition-medication-pbs.html)
* [Referral Request Medicare Benefits Schedule Department of Veterans’ Affairs](StructureDefinition-referralrequest-mbsdva.html)

Profiles that define representation of donation decision information from the Australian Organ Donor Register:
* [Consent Australian Organ Donor Register](StructureDefinition-consent-aodr.html)
* [BodySite Australian Organ Donor Register](StructureDefinition-bodysite-aodr.html)

Profile that defines the representation of vaccination information from the Australian Immunisation Register:
* [Immunization Australian Immunisation Register](StructureDefinition-immunization-air.html)








