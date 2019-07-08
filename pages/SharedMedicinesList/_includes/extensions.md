# {{ page.title }}

The following extensions form part of this implementation guide:

<table class="list" width="100%">
  <tr >
    <th>Extension</th>
    <th>id</th>
    <th>Type</th>
    <th>Context</th>
  </tr>
  <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-indigenous-status.html">Australian Indigenous Status</a></td>
   <td>indigenous-status</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Coding">Coding</a></td>
  <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
 <tr>
   <td><a href="http://hl7.org/fhir/STU3/extension-birthplace.html">Birth Place</a></td>
   <td>birthPlace</td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Address">Address</a></td>
    <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
 <tr>
   <td><a href="http://hl7.org/fhir/STU3/extension-patient-birthtime.html">birthTime</a></td>
   <td>patient-birthTime</td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#dateTime">dateTime</a></td>
    <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient.birthDate</a></td>
  </tr>
  <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-change-description.html">Change Description</a></td>
   <td>change-description</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#string">string</a></td>
   <td><a href="http://hl7.org/fhir/stu3/list.html">List.entry</a></td>
  </tr>
  <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-closing-the-gap-registration.html">Closing the Gap Registration</a></td>
    <td>closing-the-gap-registration</td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#boolean">boolean</a></td>
   <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
  <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-composition-author-role.html">Authoring Practitioner Role</a></td>
   <td>composition-author-role</td>
   <td><a href="http://hl7.org/fhir/stu3/references.html#Reference">Reference</a></td>
    <td><a href="http://hl7.org/fhir/stu3/composition.html">Composition</a></td>
  </tr>
  <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-date-accuracy-indicator.html">Date Accuracy Indicator</a></td>
   <td>date-accuracy-indicator</td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Coding">Coding</a></td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#date">date</a>, <a href="http://hl7.org/fhir/stu3/datatypes.html#dateTime">dateTime</a> </td>
  </tr>
   <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-information-recipient.html">Information Recipient</a></td>
   <td>information-recipient</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Reference">Reference</a></td>
   <td><a href="http://hl7.org/fhir/STU3/composition.html">Composition</a></td>
  </tr> 

  <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-author-role.html">Authoring PractitionerRole</a></td>
   <td>author-role</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Reference">Reference</a></td>
   <td><a href="http://hl7.org/fhir/stu3/resourcelist.html">Resource</a></td>
  </tr> 
      
   <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-medication-brand-name.html">Medication Brand Name</a></td>
   <td>medication-brand-name</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#string">string</a></td>
   <td><a href="http://hl7.org/fhir/STU3/Medication">Medication</a>, <a href="http://hl7.org/fhir/STU3/MedicationRequest">MedicationRequest</a>, <a href="http://hl7.org/fhir/STU3/MedicationDispense">MedicationDispense</a>, <a href="http://hl7.org/fhir/STU3/MedicationStatement">MedicationStatement</a></td>
  </tr>
  
 <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-medication-generic-name.html">Medication Generic Name</a></td>
   <td>medication-generic-name</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#string">string</a></td>
   <td><a href="http://hl7.org/fhir/STU3/Medication">Medication</a>, <a href="http://hl7.org/fhir/STU3/MedicationRequest">MedicationRequest</a>, <a href="http://hl7.org/fhir/STU3/MedicationDispense">MedicationDispense</a>, <a href="http://hl7.org/fhir/STU3/MedicationStatement">MedicationStatement</a></td>
  </tr>  
  <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-medication-type.html">Medication Type</a></td>
   <td>medication-type</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Coding">Coding</a></td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Coding">Coding</a></td>
  </tr>
 <tr>
   <td><a href="http://hl7.org/fhir/STU3/extension-patient-mothersmaidenname.html">Mother's Maiden Name</a></td>
   <td>patient-mothersMaidenName</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#string">string</a></td>
   <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
<tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3//StructureDefinition-author-related-person.html">Author as a RelatedPerson</a></td>
   <td>author-related-person</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Reference">Reference</a></td>
     <td><a href="http://hl7.org/fhir/stu3/resourcelist.html">Resource</a></td>
  </tr>
 </table> 
