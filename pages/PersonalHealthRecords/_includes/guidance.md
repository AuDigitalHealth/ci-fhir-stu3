{:.no_toc}
<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->
* Do not remove this line (it will not be displayed)
{:toc}
# {{ page.title }}

## FHIR 

FHIR (Fast Healthcare Interoperability Resources) is a standard developed by Health Level Seven International (Hl7) for exchanging healthcare information electronically.

The standard describes data formats and elements, known as [Resources](http://hl7.org/fhir/stu3/resourcelist.html), and an application programming interface (API) for exchanging electronic records as messages, services and documents. 

The current FHIR specification is available on [http://hl7.org/fhir](http://hl7.org/fhir). The specification also includes a directory of past and current working versions, including the current build, on [http://www.hl7.org/fhir/directory.cfml](http://www.hl7.org/fhir/directory.cfml). 

[FHIR Release 4, First Normative content](http://hl7.org/fhir/R4/) is now published.

The following references are recommended to gain a better understanding of FHIR:
* [FHIR Release 3 (STU3)](https://www.hl7.org/fhir/STU3/index.html)
* [FHIR Overview](https://www.hl7.org/fhir/STU3/overview.html)
* [HL7 International FHIR Wiki page](http://wiki.hl7.org/index.php?title=FHIR)

 

### Profile representation and structure

Each profile in this implementation guide may include one or more usage scenarios supported by this implementation guide, implementation guidance specific to those usage scenarios and one or more examples that demonstrate the use. This content is informative; there may be valid reasons not to follow this guidance, but the full implications must be understood and carefully weighed before choosing a different course.

This information is included in profile and extensions pages, e.g. [Shared Health Summary] StructureDefinition-composition-shs-1.html).

The profile url is displayed in the [Formal Views of Profile Content](StructureDefinition-composition-shs-1.html#profile), followed by: 
* **Description**: A free text natural language description of the structure and its use that also includes the information on meaning of must support
* **Base Resource**: Base resource from which this profile is derived from; included in this implementation guide as "This profile builds on [base resource]"
* **Metadata**: A set of metadata that describes the version of the profile, publisher and the date of publishing; included as "This profile was published on [date]as a [status] by [publisher "Australian Digital Health Agency"]." 

Each profile in this implementation guide also has different representations of the rules on the element contents in a resource: 
* **Text Summary**: Informative description of the changes being made in the profile in regards to its base resource. While every effort has been taken to ensure that the text summary for a profile is consistent with the profile, where there are conflicts the profile definition will take precedence
* **Differential**: Shows details of what is being changed in the profile in regards to its base resource
* **Snapshot**: Shows computed outcome of applying the statements in the differential to the base resource. An instance claiming conformance to a profile needs to conform to the snapshot representation of the profile 



### Conformance conventions

#### Profile
This implementation guide specifies the FHIR [profiles](http://hl7.org/fhir/stu3/profiling.html) for implementing the document model that is the subject of this implementation guide, i.e. Shared Health Summary.

A FHIR profile is a set of constraints and/or extensions on a resource or a data type represented using the FHIR [StructureDefinition](FHIR http://hl7.org/fhir/stu3/structuredefinition.html) resource.

The profile is identified by its url (e.g.http://ns.electronichealth.net.au/ci/fhir/3.0/StructureDefinition/composition-shs-1). When valued in an instance, the url signals the imposition of a set of profile-defined constraints. The url value provides a unique identifier for the profile in question.


#### Slicing
FHIR allows an operation called 'slicing'. Slicing is usually done on resource elements that can appear more than once in a profile, or on elements that do not repeat but have a choice of data types, where each slice has a different definition of the element. For example, Composition.section in the SHS profile is sliced into a list of slices in order to give each slice a different definition in the profile; e.g. each section slice has title, code etc specific to the slice. 

Sliced element in a profile is described as a list of elements with the same path, where the first element describes the slicing rules (e.g. Slice: Unordered, Closed by value:code) and repeat elements describe rules specific to each slice.

Slicing rules are: 
* **Ordered**: describes whether the slices must come in the order they are defined (Ordered), or whether they can come in any order (Unordered)
* **Rules**: describes whether the profiles that are derived from this one are allowed to add additional slices (Open), or not allowed to add additional slices (Closed)
* **Discriminator**: an element or a list of elements used to discriminate the slices. When a discriminator is provided, the composite of the values of the elements designated in the discriminator is unique and distinct for each possible slice

Please refer to [Slicing](http://hl7.org/fhir/STU3/profiling.html#slicing) information in FHIR specification for more information on slicing and discrimination operations and processing rules.


#### Extensions
Any element in FHIR resource can carry one or more extensions in addition to its normal content.

An extension is identified by its url (e.g. http://hl7.org.au/fhir/StructureDefinition/indigenous-status), and it has a value that is one of the base FHIR data types.  

An extension, if present in this specification, will be included as an element in the Differential and Snapshot views of a profile, with the extension URL hyperlinked to the extension definition specified in the “Description & Constraints” column of the profile. 

Please refer to [Extensibility](http://hl7.org/fhir/STU3/extensibility.html) in FHIR specification for more information on defining and processing extensions.


#### Conformance verbs
The conformance verbs used in this implementation guide are defined in [FHIR Conformance Rules](http://hl7.org/fhir/STU3/conformance-rules.html#conflang).


#### Terminology binding
Terminology is specified in this implementation guide, in some cases binding an element to a value set or binding an attribute to a single fixed code. For guidance on coding common clinical concepts in FHIR resources see [Using Codes in Resources](http://hl7.org/fhir/stu3/terminologies.html).

A value set binding, if present in this specification, will be specified in the "Description & Constraints" column of a profile as the title of the value set (hyperlinked to its definition) followed by identification of the binding strength (hyperlinked to its definition), e.g. Health Summary Non-Clinical Empty Reason (required).


#### Cardinality
The cardinality range specifies the allowable occurrences within a document instance. Cardinality range is specified in the format "m..n" where m is the minimum allowed members of the set (lower bound) and n is the maximum allowed members of the set (upper bound). The allowed values for m and n are 0, any positive integer, and *.

The table below demonstrates a representative set of examples of cardinality range and how to interpret that cardinality range; p is positive integer greater than the minimum allowed members of the set.

<table border="1" cellpadding="1" valign="middle">
<tbody>
  <tr bgcolor="#DCDCDC">
    <th>Cardinality range</th>
    <th>Interpretation</th>
  </tr>
  <tr>
    <td>0..0</td>
    <td>zero (explicitly prohibited)</td>
  </tr>
 <tr>
    <td>0..1</td>
    <td>zero or one</td>
  </tr>
  <tr>
    <td>1..1</td>
    <td>exactly one</td>
  </tr>
  <tr>
    <td>0..*</td>
    <td>zero or more</td>
  </tr>
    <tr>
    <td>1..*</td>
    <td>at least one</td>
  </tr>
<tr>
    <td>2..*</td>
    <td>at least two</td>
  </tr>
<tr>
    <td>1..p</td>
    <td>at least one and not more than p</td>
  </tr>
  <tr>
    <td>2..p</td>
    <td>at least two and not more than p</td>
  </tr>
 </tbody>
</table>

The cardinality rules in FHIR are described in [FHIR Conformance Rules](http://hl7.org/fhir/STU3/conformance-rules.html#conflang).


#### Data types
The FHIR standard defines a set of data types that are used for the resource elements.  

Data types used in this implementation guide are defined in FHIR Release 3 (STU) [Data Types]( http://hl7.org/fhir/stu3/datatypes.html).


### Known issues with supporting and implementing FHIR

FHIR standard offers a number of tools for development and implementations of FHIR, e.g. IG Publisher tool used for producing and publishing this implementation guide, FHIR Validator used to validate examples in this implementation guide.

These tools are under continues development and as such may have issues that could affect development and implementation of FHIR. 

This section lists known issues with authoring and rendering content in this implementation guide. 

<table border="1" cellpadding="1" valign="middle">
<tbody>
  <tr bgcolor="#DCDCDC">
    <th>Reference</th>
    <th>Description</th>
    <th>gForge Change Request</th>
  </tr>
  <tr>
    <td>Validation of examples</td>
    <td>FHIR Validator does not yet fully support all expressions defined in FHIR specification and included in this implementation guide; i.e. conformsTo().</td>
    <td>-</td>
  </tr>
  <tr>
    <td>Rendering of examples</td>
    <td>IG publisher does nor render Composition narrative and section.text narrative nor any of the contained resources. Please refer to XML or JSON format of an example to view the whole example. </td>
    <td><a href="https://gforge.hl7.org/gf/project/fhir/tracker/?action=TrackerItemEdit&tracker_item_id=17401">Allow ig publisher to render documents as documents </a></td>
  </tr>
 </tbody>
</table> 

Please refer to [Implementation Support Module](http://hl7.org/fhir/implsupport-module.html) for more information about available tools, libraries and other similar resources.

The following references are available to raise issues and seek help:
* [FHIR Chat Channel Zulip](https://chat.fhir.org/)
* [FHIR Community Forum](http://community.fhir.org/)
* [StackOverflow](https://stackoverflow.com/questions/tagged/hl7_fhir)
* [gForge](https://gforge.hl7.org/gf/project/fhir/)



