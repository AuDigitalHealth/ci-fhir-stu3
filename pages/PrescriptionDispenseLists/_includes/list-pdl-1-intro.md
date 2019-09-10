### List of Prescription and or Dispense Records *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios

* A clinical information system (CIS) sends or receives a prescription and or a dispense record list with the My Health Record system
* A contracted service provider (CSP) sends or receives a prescription and or a dispense record list with the My Health Record system
* A CIS sends or receives a prescription and or a dispense record list with another CIS or CSP
* A CSP sends or receives a prescription and or a dispense record list with a CIS or another CSP
* A registered portal or registered repository receives a prescription and or a dispense record list

Expected usage scenarios, further scoping the above overarching scenarios are:

* Prescription and dispense view (PDV) exchanged with the My Health Record as a list
* Prescription and dispense view (PDV) exchanged with the My Health Record as a document

This profile does not support sending medicines change information (e.g. indicating cancellation or newly prescribed items) or event-specific information; in this case it is recommended that information is supplied as a shared medicines list.  

#### Implementation guidance

For the above overarching scenarios in this implementation guide:

* with a List.code of ‘100.32014’ Dispense List will be sent with only dispensed medicine items
* with a List.code of ‘57828-6’ Prescription list will be sent with only prescribed medicine items
* although an allowed type of list item is MedicationStatement its use is discouraged 

When the list is a PDV
* The source will be a Device, and is expected to be the My Health Record system
* The date will be the time the PDV is generated

#### When the list is part of a document
When the list is sent as part of a document (referenced in Composition.section.entry) rather than as a standalone resource the following guidance applies:
<table class="list" width="100%">
  <tr>
    <th>Item</th>
    <th>Guidance</th>
   </tr>
     <tr>
        <td>author role</td>
        <td>Will reference the same PractitionerRole as in Composition.composition-author-role</td>
    </tr>
     <tr>
        <td>author related person</td>
        <td>Will reference the same RelatedPerson as in Composition.author</td>
    </tr>
    <tr>
        <td>code</td>
        <td>Will have the same value as in the referencing Composition.section.code</td>
    </tr>
    <tr>
        <td>subject</td>
        <td>Will reference the same Patient as in Composition.subject</td>
    </tr>
    <tr>
        <td>date</td>
        <td>Will hold the same value as Composition.date</td>
    </tr>
    <tr>
        <td>source</td>
        <td>Will reference the same resource as in Composition.author</td>
    </tr>
    <tr>
        <td>title</td>
        <td>Will not be provided</td>
    </tr>
    </table>
    