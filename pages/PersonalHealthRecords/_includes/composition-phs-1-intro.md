#### Personal Health Summary *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]* 

#### Usage Scenarios
The following are the usage scenarios expected:

* An individual or their authorised representative authors a personal health summary document to be exchanged with the My Health Record system

#### Implementation guidance
For the overarching usage scenarios in this implementation guide it is expected that:
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
  </table> 
  
This profile is referenced by TBD