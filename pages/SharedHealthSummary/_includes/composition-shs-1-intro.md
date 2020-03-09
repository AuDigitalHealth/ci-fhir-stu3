#### Shared Health Summary *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios 

The following are the overarching usage scenarios this profile is intended to support:

* A clinical information system (CIS) sends or receives an Shared Health Summary with the My Health Record system
* A contracted service provider (CSP) sends or receives an Shared Health Summary with the My Health Record system
* A CIS sends or receives an Shared Health Summary with another CIS or CSP
* A CSP sends or receives an Shared Health Summary with a CIS or another CSP
* A registered portal or registered repository receives an Shared Health Summary


#### Implementation guidance 

For the overarching usage scenarios in this implementation guide it is expected that:
* composition author role will be a reference to a PractitionerRole resource that describes the author’s professional role, e.g. General Practitioner
* author will be a reference to a Practitioner resource that describes the author
* an empty section will be sent with an empty reason

<table class="list" width="100%">
  <tr>
    <th>Section</th>
    <th>Guidance</th>
   </tr>
 
 <tr>
   <td rowspan="1">Allergies</td>
    <td>Where a sending system can state that a patient does not have an allergy or category of allergies an AllergyIntolerance will be sent</td>
  </tr>
  
   <tr>
   <td rowspan="1">Medications</td>
    <td>Where a sending system can state that a patient is not currently taking medication an Observation will be sent</td>
  </tr>
 
 <tr>
   <td rowspan="4">Medical History</td>
    <td>Where a sending system cannot classify a coded entry as a procedure or a condition it is expected that the code is sent as a code in Condition</td>
  </tr>
 <tr>
    <td>Where a sending system cannot make classification as it has free text entry only, it is expected that the entry is sent as a free text in Condition</td>
  </tr>
    <tr>
    <td>Where a sending system can state that a patient has no relevant history of findings it is expected an assertion of no relevant finding (Observation) is sent with the appropriate code (i.e. 1224831000168103 |No relevant medical history|)</td>
  </tr>
  <tr>
    <td>Where a sending system can state that a patient does not have a specific condition it is expected that the appropriate negation code (e.g. 162028008 |No indigestion|) is sent as the code in Condition</td>
  </tr>
  
  <tr>
   <td>Immunisations</td>
    <td>Where a sending system can state that a patient has no relevant history of findings it is expected an assertion of no relevant finding (Observation) is sent with the appropriate code (i.e. 1234401000168109 |No history of vaccination|)</td>
  </tr>
</table>  
  
When sending a Shared Health Summary to the My Health Record system it is expected that all instances of patient will conform to [My Health Record Patient](StructureDefinition-patient-mhr-1.html).
   
