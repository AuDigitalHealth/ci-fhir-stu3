#### Event Summary *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*


#### Usage scenarios 

The following are the overarching usage scenarios this profile is intended to support:

* A clinical information system (CIS) sends or receives an Event Summary with the My Health Record system
* A contracted service provider (CSP) sends or receives an Event Summary with the My Health Record system
* A CIS sends or receives an Event Summary with another CIS or CSP
* A CSP sends or receives an Event Summary with a CIS or another CSP
* A registered portal or registered repository receives an Event Summary


####  Implementation guidance
For the overarching usage scenarios in this implementation guide it is expected that all medicine items relevant to an event should be included in the list. All medicine items will have an associated flag according to the guidance in the following table.

<table class="list" width="100%">
  <tr>
    <th>Section</th>
    <th>Guidance</th>
    </tr>
  <tr>
   <td rowspan="1">Event Overview</td>
    <td>It is expected that section.text is populated from the Encounter Description element of the Encounter entry</td>
  </tr>
 <tr>
   <td rowspan="1">Allergies</td>
    <td>Where a sending system can state that a patient does not have an allergy or category of allergies it is expected that an AllergyIntolerance is sent with the appropriate negation code (e.g. 716186003 |No known allergy|) is sent as the code</td>
  </tr>
   <tr>
   <td rowspan="1">Medications</td>
    <td>Where a sending system can state that a patient is known not to have current medications it is expected an assertion of no relevant finding (Observation) is sent with the appropriate code (i.e. 1234391000168107 |No known current medications|)</td>
  </tr>
 <tr>
   <td rowspan="4">Medical History</td>
    <td>Where a sending system cannot classify a coded entry as a procedure or a condition it is expected that the code is sent as a code in Condition</td>
  </tr>
 <tr>
    <td>Where a sending system cannot make classification as it has free text entry only, it is expected that the entry is sent as a free text in Condition</td>
  </tr>
  <tr>
   <td>Where a sending system wants to include a information that cannot be directly included in a supported section entry resource the information may be included via a resource that is referenced from one of the supported section entries or by instantiating a child section to manage the additional information with a meaningful sub-section grouping</td>
  </tr>
  <tr>
    <td>Where a sending system can state that a patient does not have a specific condition it is expected that the appropriate negation code (e.g. 162028008 |No indigestion|) is sent as the code in Condition</td>
  </tr>
  
  <tr>
   <td rowspan="1">Immunisations</td>
    <td>Where a sending system can state that a patient has not been administered a vaccine during the encounter or that the patient has no relevant history of vaccination it is expected an assertion of no relevant finding  (Observation) is sent with the appropriate code (e.g. 1226591000168105 |No vaccine administered during encounter|)</td>
  </tr>
</table>  
When sending an event summary to the My Health Record system it is expected that all instances of patient will conform to [My Health Record Patient](StructureDefinition-patient-mhr-1.html).
  
