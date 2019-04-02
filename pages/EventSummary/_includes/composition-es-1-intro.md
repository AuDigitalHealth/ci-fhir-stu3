### Event Summary *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*


#### Usage Scenarios 

The following are the usage scenarios expected:

* A clinical information system (CIS) sends or receives an Event Summary with the My Health Record system
* A contracted service provider (CSP) sends or receives an Event Summary with the My Health Record system
* A registered repository or registered portal receives an Event Summary from the My Health Record system


####  Implementation guidance 
* Where additional content beyond that flagged with a must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
* For each section included in the composition it is important to differentiate between affirmatively stating a patient has no relevant findings (e.g. no history of immunisation) versus a finding that a patient does not have a specific condition (e.g. no latex allergy) versus not including findings in the record (e.g. not applicable or unknown).

<table border="1">
  <tr bgcolor="#DCDCDC">
    <th>Section</th>
    <th>Guidance</th>
    </tr>
 
 <tr>
   <td rowspan="1">Event Overview</td>
    <td>It is expected that section.text is populated from the Encounter Description element of the Encounter entry</td>
  </tr>
 <tr>
   <td rowspan="2">Allergies</td>
    <td>Where a sending system does not have any clinical data to provide in that section it is expected that section.emptyReason is used</td>
  </tr>
 <tr>
    <td>Where a sending system can state that a patient does not have an allergy or category of allergies it is expected that an AllergyIntolerance is sent with the appropriate negation code (e.g. 160244002 &#124;No known allergies&#124;) is sent as the code</td>
  </tr>
  
   <tr>
   <td rowspan="3">Medications</td>
    <td>Where a sending system does not have any clinical data to provide in that section it is expected that section.emptyReason is used</td>
  </tr>
 <tr>
    <td>Where a sending system can state that a patient is known not to have current medications it is expected an assertion of no relevant finding (Observation) is sent with the appropriate code (i.e. 1234391000168107 &#124;No known current medications&#124;)</td>
  </tr>
  <tr>
    <td>Where a sending system wants to include an observation other than an assertion of no relevant finding, the observation will be outside the section and will be referred to from one of the entries in the section</td>
  </tr>
  
 <tr>
   <td rowspan="6">Medical History</td>
    <td>Where a sending system cannot classify a coded entry as a procedure or a condition it is expected that the code is sent as a code in Condition</td>
  </tr>
 <tr>
    <td>Where a sending system cannot make classification as it has free text entry only, it is expected that the entry is sent as a free text in Condition</td>
  </tr>
  <tr>
    <td>Where a sending system does not have any clinical data to provide in that section it is expected that section.emptyReason is used</td>
  </tr>
    <tr>
    <td>Where a sending system can state that a patient has no relevant history of findings it is expected an assertion of no relevant finding (Observation) is sent with the appropriate code (i.e. 1224831000168103 &#124;No relevant medical history&#124;)</td>
  </tr>
  <tr>
   <td>Where a sending system wants to include an observation other than an assertion of no relevant finding, the observation will be outside the section and will be referred to from one of the entries in the section</td>
  </tr>
  <tr>
    <td>Where a sending system can state that a patient does not have a specific condition it is expected that the appropriate negation code (e.g. 162028008 &#124;No indigestion&#124;) is sent as the code in Condition</td>
  </tr>
  
  <tr>
   <td rowspan="3">Immunisations</td>
    <td>Where a sending system does not have any clinical data to provide in that section it is expected that section.emptyReason is used</td>
  </tr>
  <tr>
    <td>Where a sending system can state that a patient has not been administered a vaccine during the encounter or that the patient has no relevant history of vaccination it is expected an assertion of no relevant finding  (Observation) is sent with the appropriate code (e.g. 1226591000168105 |No vaccine administered during encounter|). </td>
  </tr>
    <tr>
    <td>Where a sending system wants to include an observation other than an assertion of no relevant finding, the observation will be outside the section and will be referred to from one of the entries in the section</td>
  </tr>
 
</table>  
  
#### Known Issues

* Diagnostic Investigations section is in progress. It will be updated to reference appropriate Agency profiles in the future.
   
