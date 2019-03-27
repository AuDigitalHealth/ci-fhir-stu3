# {{ page.title }}

The following extensions form this implementation guide:

<table class="list">
  <tr >
    <th>Extension</th>
    <th>id</th>
    <th>Type</th>
    <th>Context</th>
  </tr>
 <tr>
   <td><a href="http://hl7.org/fhir/STU3/extension-birthplace.html">Birth Place</a></td>
   <td>birthPlace</td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Address">Address</a></td>
    <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
 <tr>
   <td><a href="http://hl7.org/fhir/extension-patient-birthtime.html">birthTime</a></td>
   <td>patient-birthTime</td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#dateTime">dateTime</a></td>
    <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient.birthDate</a></td>
  </tr>
    <tr>
   <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-closing-the-gap-registration.html">Closing the Gap Registration</a></td>
    <td>closing-the-gap-registration</td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#boolean">boolean</a></td>
   <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
  <tr>
   <td><a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-composition-author-role.html">Authoring Practitioner Role</a></td>
   <td>composition-author-role</td>
   <td><a href="http://hl7.org/fhir/stu3/references.html#Reference">Reference</a></td>
    <td><a href="http://hl7.org/fhir/stu3/composition.html">Composition</a></td>
  </tr>
  <tr>
   <td><a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-date-accuracy-indicator.html">Date Accuracy Indicator</a></td>
   <td>date-accuracy-indicator</td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Coding">Coding</a></td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#date">date</a>, <a href="http://hl7.org/fhir/stu3/datatypes.html#dateTime">dateTime</a> </td>
  </tr>
    <tr>
   <td><a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-indigenous-status.html">Indigenous Status</a></td>
   <td>indigenous-status</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Coding">Coding</a></td>
  <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
    <tr>
   <td><a href="http://hl7.org/fhir/STU3/extension-patient-mothersmaidenname.html">Mother's Maiden Name</a></td>
   <td>patient-mothersMaidenName</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#string">string</a></td>
   <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
<tr>
   <td><a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-recorder.html">Recorder</a></td>
   <td>recorder</td>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Reference">Reference</a></td>
     <td><a href="http://hl7.org/fhir/stu3/condition.html">Condition</a></td>
  </tr>
<tr>
   <td><a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-recorder-related-person.html">Recorder as a RelatedPerson</a></td>
   <td>recorder-related-person</td>
   <td><a href="http://hl7.org/fhir/stu3/references.html#Reference">Reference</a></td>
   <td><a href="http://hl7.org/fhir/STU3/allergyintolerance.html">AllergyIntolerance</a></td>
  </tr>
 </table> 
