#### Shared Medicine List *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Usage scenarios 

The following are the usage scenarios expected:

* A clinical information system (CIS) sends or receives a shared medicines list with the My Health Record system
* A contracted service provider (CSP) sends or receives a shared medicines list with the My Health Record system
* A CIS sends or receives a shared medicines list with another CIS or CSP
* A CSP sends or receives a shared medicines list with a CIS or another CSP
* A registered portal or registered repository receives a shared medicines list


#####  Implementation guidance 

For the expected usage scenarios in this implementation guide:

* For each section included in the composition it is important to differentiate between affirmatively stating a patient has no relevant findings (e.g. no history of immunisation) versus a finding that a patient does not have a specific condition (e.g. no latex allergy) versus not including findings in the record (e.g. not applicable or unknown).
* Where a sending system wants to include information that cannot be directly included in a supported section entry resource, the information may be included via a resource that is referenced from one of the supported section entries or by instantiating a child section to manage the additional information with a meaningful sub-section grouping
<table class="list" width="100%">
  <tr>
    <th>Section</th>
    <th>Guidance</th>
    </tr>
 <tr>
   <td rowspan="2">Allergies</td>
    <td>Where a sending system does not have any clinical data to provide in that section it is expected that section.emptyReason is used</td>
  </tr>
 <tr>
    <td>Where a sending system can state that a patient does not have an allergy or category of allergies it is expected that an AllergyIntolerance is sent with the appropriate negation code (e.g. 716186003 |No known allergy|) is sent as the code</td>
  </tr>
  
   <tr>
   <td rowspan="3">Medications</td>
    <td>Where a sending system does not have any clinical data to provide in that section it is expected that section.emptyReason is used</td>
  </tr>
 <tr>
    <td>Where a sending system can state that a patient is known not to have current medications it is expected an assertion of no relevant finding (Observation) is sent with the appropriate code (i.e. 1234391000168107 |No known current medications|)</td>
  </tr>
</table>  

##### PSML implementation guidance

* The author is expected to be a pharmacist.
* It is expected that a list of medicines will be provided.


 
  
   
