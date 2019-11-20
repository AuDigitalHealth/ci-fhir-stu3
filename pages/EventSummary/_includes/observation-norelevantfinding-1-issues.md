<table class="list" width="100%">
<tbody>
  <tr>
    <th>Reference</th>
    <th>Description</th>
    <th>Issue No.</th>
  </tr>
  <tr>
        <td>code (incorrect use of fixedCodeableConcept)</td>
        <td>The HL7 AU <a href="http://hl7.org.au/fhir/base/aubase1.1/StructureDefinition-au-norelevantfinding.html">AU Assertion of No Relevant Finding profile</a>, from which this profile is derived, fixes the value on Observation.code by using <a href="https://github.com/hl7au/au-fhir-base-stu3/blob/master/resources/au-norelevantfinding.xml#L35-L40">fixedCodeableConcept</a>. The result of this is to prohibit CodeableConcept.text and CodeableConcept.coding.display (as well as other elements), which will inhibit the representation of realistic instances of data. An alternate method of fixing values has been devised (as is documented in an associated ticket shown to the right). This issue will be fixed in an R4 variant of this profile.</td>
        <td>See GitHub <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">Incorrect use of fixedCodeableConcept in various profiles, issue #48</a>.</td>
  </tr>  
 </tbody>
</table>