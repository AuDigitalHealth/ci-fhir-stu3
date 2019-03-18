# {{ page.title }}

The following extensions form this implementation guide:

<table border="1">
  <tr bgcolor="#DCDCDC">
    <th>Implementation guide extension</th>
    <th>Type</th>
    <th>Context</th>
  </tr>
 <tr>
   <th><a href="http://hl7.org/fhir/STU3/extension-birthplace.html">Birth Place</a></th>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Address">Address</a></td>
    <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
 <tr>
   <th><a href="http://hl7.org/fhir/extension-patient-birthtime.html">birthTime</a></th>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#dateTime">dateTime</a></td>
    <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient.birthDate</a></td>
  </tr>
    <tr>
   <th><a href="https://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-closing-the-gap-registration.html"> Closing the Gap Registration</a></th>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#boolean">boolean</a></td>
   <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
  <tr>
   <th><a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-composition-author-role.html">Authoring Practitioner Role</a></th>
   <td><a href="http://hl7.org/fhir/stu3/references.html#Reference">Reference</a></td>
    <td><a href="http://hl7.org/fhir/stu3/composition.html">Composition</a></td>
  </tr>
  <tr>
   <th><a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-date-accuracy-indicator.html">Date Accuracy Indicator</a></th>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Coding">Coding</a></td>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#date">date</a>, <a href="http://hl7.org/fhir/stu3/datatypes.html#dateTime">dateTime</a> </td>
  </tr>
    <tr>
   <th><a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-indigenous-status.html">Indigenous Status</a></th>
    <td><a href="http://hl7.org/fhir/stu3/datatypes.html#string">string</a></td>
  <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
    <tr>
   <th><a href="http://hl7.org/fhir/STU3/extension-patient-mothersmaidenname.html">Mother's Maiden Name</a></th>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Coding">Coding</a></td>
   <td><a href="http://hl7.org/fhir/stu3/patient.html">Patient</a></td>
  </tr>
<tr>
   <th><a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-recorder.html">Recorder</a></th>
   <td><a href="http://hl7.org/fhir/stu3/datatypes.html#Reference">Reference</a></td>
     <td><a href="http://hl7.org/fhir/stu3/condition.html">Condition</a></td>
  </tr>
<tr>
   <th><a href="http://build.fhir.org/ig/hl7au/au-fhir-base/StructureDefinition-recorder-related-person.html">Recorder as a RelatedPerson</a></th>
   <td><a href="http://hl7.org/fhir/stu3/references.html#Reference">Reference</a></td>
   <td><a href="http://hl7.org/fhir/STU3/allergyintolerance.html">AllergyIntolerance</a></td>
  </tr>
 </table> 
