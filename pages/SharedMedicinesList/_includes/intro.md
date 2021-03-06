# {{ site.data.fhir.igName }} FHIR Implementation Guide
<h3>Approved for external trial use</h3>
{:.no_toc}

{% include publish-box.html %}
<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->
* Do not remove this line (it will not be displayed)
{:toc}
<!-- end TOC -->

## Introduction

This implementation guide is an HL7<sup>TM</sup> FHIR<sup>&reg;</sup> specification to represent a shared medicines list, including Pharmacist Shared Medicines List (PSML). A shared medicines list is a list of medicines, at a point in time, that describes the medicines an individual is taking.

This [implementation guide](http://hl7.org/fhir/STU3/implementationguide.html#scope) is based on [FHIR Release 3 (STU) [HL7FHIR3]](#HL7FHIR3).

## Document purpose and scope

The primary aim of this implementation guide is to support implementing a shared medicines list in [FHIR Release 3 (STU) [HL7FHIR3]](#HL7FHIR3). The resulting FHIR can be used for the electronic exchange of shared medicines list information between healthcare providers.

This implementation guide is not to be used as a guide to presentation (or rendering) of the data. It contains no information as to how the data described by it should be displayed and no such guidance should be inferred.

This implementation guide does not describe transport or persistence mechanism of the resources described by it.

Reference has been made to International and Australian Standards, and to Standards from Health Level Seven. The following standards are referred to in the text in such a way that some or all of its content constitutes requirements for the purposes of this specification:
* [FHIR Release 3 (STU) [HL7FHIR3]](#HL7FHIR3)
* [Australian Base Implementation Guide (AU Base 1.1.1) [HL7AUF3B2]](#HL7AUF3B2)

Wherever possible, material in this specification is based on existing standards. All efforts have been made to minimise divergence from the HL7 Australia profiles of HL7 International standards ([Australian Base Implementation Guide (AU Base 1.1.1) [HL7AUF3B2]](#HL7AUF3B2)) to provide for system interoperability and compatibility with other profiles. Issues of an editorial nature in the source material (such as spelling or punctuation errors) are intentionally reproduced.

This implementation guide is the basis for the corresponding [{{site.data.fhir.igName}} CDA implementation guide [DH2020b]](#DH2020b). The profiles referenced by this FHIR implementation guide are the 'models' that are mapped into CDA.

This implementation guide makes reference to the set of profiles and extensions (StructureDefinitions) that form part of this implementation guide. Some profiles and extensions are described by this implementation guide, and some are described by other published sources such as the [Australian Base Implementation Guide (AU Base 1.1.1) [HL7AUF3B2]](#HL7AUF3B2) or [FHIR Release 3 (STU) [HL7FHIR3]](#HL7FHIR3). The profiles described in this implementation guide do not include profile-specific mappings to another format as part of their description. Any profile-specific mappings to another format is the subject of an implementation guide for that particular format, e.g. a corresponding CDA implementation guide. The base FHIR® STU3 mapping content for each of the resources referenced in this implementation guide can be found on the applicable resource documentation in the [FHIR Release 3 (STU) [HL7FHIR3]](#HL7FHIR3).

## Context and use
A FHIR implementation guide is part of a package of documents and files that support the development of software to exchange a type of clinical document, an end-product clinical specification package.

An Agency end-product clinical specification package supports software developers to create and interpret instances of a clinical document. The core of each package is a specification of the information content of instances of the clinical document.

Supplementary contents of the package include statements of scenarios for which the specification is appropriate, guidance on implementing the specification, and guidance on testing purported instances.

The contents may include:
* statement of requirements
* CDA implementation guide (CDA IG) – a statement of constraints and custom extensions on [HL7 Clinical Document Architecture [HL7CDAR2]](#HL7CDAR2)
* FHIR implementation guide (FHIR IG) - a statement of constraints and custom extensions on [HL7 FHIR [HL7FHIR3]](#HL7FHIR3)
* template package library – a set of Schematron schema to test conformance of CDA documents with the specification
* conformance profile – a statement of conformance requirements for exchanging documents within a particular scenario such as the My Health Record
* release notes

Clinical specification packages contain only files relevant to the particular clinical document. Specifications that are common to many clinical documents and should be considered part of the specification package, as directed by the relevant release note and conformance profile, may be contained elsewhere.

## How to read this document
This implementation guide contains descriptions of both constraints on HL7 FHIR and, where necessary, custom extensions to HL7 FHIR, for the purposes of fulfilling the requirements for Australian implementations of shared medicines lists. These descriptions are defined as a set of FHIR [profiles](http://hl7.org/fhir/stu3/profiling.html).  

For implementers interested in a practitioner authored medicines list as a document, such as a pharmacist shared medicines list, the starting point is the [Shared Medicines List Authored by Practitioner](StructureDefinition-composition-sml-prac-1.html) profile, which references the additional profiles necessary to assert [conformance](conformance.html).

For implementers interested in representing a practitioner authored medicines list as a list, and not a document, the starting point is the [List of Medicine Items with Change Information Authored by Practitioner](StructureDefinition-list-sml-pracchanges-1.html) profile, which references the additional profiles necessary to assert [conformance](conformance.html).

## Intended audience
This implementation guide is aimed at software development teams, architects, designers, clinicians and informatics researchers who are responsible for the delivery of clinical applications, infrastructure components and messaging interfaces, and also for those who wish to evaluate the clinical suitability of the Agency-endorsed specifications.

This implementation guide and related artefacts are technical in nature and the audience is expected to be familiar with the language of health data specifications and to have some familiarity with health information standards and specifications, such as [HL7 FHIR [HL7FHIR3]](#HL7FHIR3) and Standards Australia IT-014 documents. Definitions and examples are provided to clarify relevant terminology usage and intent.

## Document Information

### Key Information

<table class="list" width="100%" cellspacing="6">
    <tbody>
        <tr>
            <td><b>Owner</b></td>
            <td>National Health Chief Information Officer, Infrastructure Operations</td>
        </tr>
        <tr>
            <td><b>Contact for enquiries</b></td>
            <td>
                <p>Australian Digital Health Agency Help Centre <br />
                t:   1300 901 001<br />
                e:  <a href ="mailto:help@digitalhealth.gov.au">help@digitalhealth.gov.au</a></p>    
            </td>
        </tr>
    </tbody>
</table> 

### Product Version History
<table class="list" width="100%" cellspacing="6">
	<col style="width:15%"/>
	<col style="width:15%"/>
	<col style="width:70%"/>
    <tbody>
        <tr>
            <th>Product version</th>
            <th>Date</th>
            <th>Release comments</th>
        </tr>
        <tr>
            <td>1.0.0</td>
            <td><span style="padding-left: 3px; padding-right: 3px">29 Jan 2020</span></td>
            <td>Initial public release at approved for external trial use. Implemented in FHIR Release 3 (STU).<br/>This version of the Shared Medicines List FHIR implementation guide supports the exchange of practitioner authored medicines lists, in an Australian healthcare context. Support is provided for the more constrained Pharmacist Shared Medicines List (PSML).</td>
        </tr>
                <tr>
            <td>1.1.0</td>
            <td><span style="padding-left: 3px; padding-right: 3px">17 Feb 2020</span></td>
            <td>Release at approved for external trial use. Implemented in FHIR Release 3 (STU). <br/>This version includes a minor update to <a href="StructureDefinition-list-sml-pracchanges-1.html">List of Medicine Items with Change Information Authored by Practitioner</a>, see <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/74">ci-fhir-stu3/issues/74</a>.<br/>This implementation guide supports the exchange of practitioner authored medicines lists in an Australian healthcare context. Support is provided for the more constrained Pharmacist Shared Medicines List (PSML).</td>
        </tr>
        <tr>
            <td>1.2.0</td>
            <td><span style="padding-left: 3px; padding-right: 3px">29 Jul 2020</span></td>
            <td>Release at approved for external trial use. Implemented in FHIR Release 3 (STU).<br/>This version includes changes to relax MedicationStatement.dosage cardinality to support recording information about ceased medicines items in PSML, addition of Dose Administration Aid Medicines Indicator in the List profile to support recording information that that a PSML includes items packed in a dose administration aid, and improvements to the Composition invariants.</td>
        </tr>
    </tbody>
</table> 

## Known issues
This table lists known issues with this specification at the time of publishing. We are working on solutions to these issues and encourage comments to help us develop these solutions.

<table border="1" cellpadding="1" valign="middle">
<tbody>
  <tr bgcolor="#DCDCDC">
    <th>Reference</th>
    <th>Description</th>
  </tr>
    <tr>
        <td>Source material errors</td>
        <td>Material in this specification is based on existing standards and all efforts have been made to minimise divergence. Issues of an editorial nature in the source material (such as spelling or punctuation errors) are intentionally reproduced.</td>
    </tr>
    <tr>
        <td>Non-resolving profile URLs</td>
        <td>Canonical URLs with the prefix of <span style="font-family:courier;">http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/</span> do not resolve. All profiles have an associated <a href="http://hl7.org/fhir/STU3/structuredefinition-definitions.html#StructureDefinition.url">canonical URL</a> that is used to uniquely identify that structure definition (i.e. profile) and is expected to be an address at which that structure definition is (or will be) published. Work is underway to ensure that these URLs resolve or redirect to a meaningful end point in the future.</td>
    </tr>
    <tr>
        <td>SML FHIR implementation guide roadmap</td>
        <td>The profiles that form part of this implementation guide are in transition to a FHIR Release 4 representation in collaboration with HL7 Australia.<br/><br/>
		This move has normative implications that are expected to result in major version incrementation to accommodate backwards incompatible changes. Widespread changes to terminology and the removal or renaming of some elements are expected to make up the bulk of the backwards incompatible changes.<br/><br/>
        The profiles described in this implementation guide only support practitioner authoring usage scenarios. Future releases of this implementation guide are expected to provide support for additional usage scenarios including other authoring entities.
        </td>
     </tr>
 </tbody>
</table> 

## References

|[<a name="DH2020b">DH2020b</a>]| Australian Digital Health Agency, Shared Medicines List CDA Implementation Guide, Version 1.0.0.|

|[<a name="DH2020m">DH2020m</a>]| Australian Digital Health Agency, Pharmacist Shared Medicines List Scenarios and business requirements, Version 2.0.|

|[<a name="DH2020n">DH2020n</a>]| Australian Digital Health Agency, Pharmacist Shared Medicines List Information Requirements, Version 2.0.|

|[<a name="DH2020o">DH2020o</a>]| Australian Digital Health Agency,31 March 2020, Common - Clinical Document, Version 1.5.4.|
||[https://developer.digitalhealth.gov.au/specifications/clinical-documents/ep-3149-2020](https://developer.digitalhealth.gov.au/specifications/clinical-documents/ep-3149-2020)|

|[<a name="HL7AUF3B2">HL7AUF3B2</a>]| HL7 Australia, Australian Base Implementation Guide (AU Base 1.1.1), build version 1.1.1 21 January 2020.|
| |[http://hl7.org.au/fhir/base/aubase1.1/index.html](http://hl7.org.au/fhir/base/aubase1.1/index.html)|

|[<a name="HL7CDAR2">HL7CDAR2</a>]|Health Level Seven, Inc., January 2010, HL7 Clinical Document Architecture, Release 2.|
| |[http://www.hl7.org/implement/standards/product_brief.cfm?product_id=7](http://www.hl7.org/implement/standards/product_brief.cfm?product_id=7)|

|[<a name="HL7FHIR">HL7FHIR</a>]| Health Level Seven, Inc., FHIR - HL7Wiki, accessed 2 October 2019.|
| |[http://wiki.hl7.org/index.php?title=FHIR](http://wiki.hl7.org/index.php?title=FHIR)|

|[<a name="HL7FHIR3">HL7FHIR3</a>]| Health Level Seven, Inc., 24 October 2019, FHIR Release 3 (STU).|
| |[http://hl7.org/fhir/STU3/](http://hl7.org/fhir/STU3/)|

|[<a name="HL7FHIR4">HL7FHIR4</a>]|Health Level Seven, Inc., 30 October 2019, FHIR R4.|
||[http://hl7.org/fhir/R4/](http://hl7.org/fhir/R4/)|
