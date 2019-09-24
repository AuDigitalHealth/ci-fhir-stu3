#### Personal Health Summary *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]* 

#### Usage Scenarios
The following are the usage scenarios expected:

* An individual or their authorised representative authors a personal health summary document to be exchanged with the My Health Record system

#### Implementation guidance
For the expected usage scenarios in this implementation guide:

* It is required that the composition include only the specified four top-level sections; additional sections to handle local content not covered by the primary design can be included as a child section if necessary.
* For each section included in the composition it is important to differentiate between affirmatively stating a patient has no relevant findings (e.g. no history of immunisation) versus a finding that a patient does not have a specific condition (e.g. no latex allergy) versus not including findings in the record (e.g. not applicable or unknown).

<table class="list" width="100%">
    <thead>
        <tr>
            <th>Section</th>
            <th>Guidance</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan="2">Allergies</td>
            <td>Where a sending system does not have any clinical data to provide in that section it is expected that section.emptyReason is used.</td>
        </tr>
        <tr>
            <td>Where a sending system can state that a patient does not have an allergy or category of allergies it is expected that an AllergyIntolerance is sent with the appropriate negation code (e.g. 716186003 |No known allergy|) is sent as the code.</td>
        </tr>
        <tr>
            <td rowspan="3">Medications</td>
            <td>Where a sending system does not have any clinical data to provide in that section it is expected that section.emptyReason is used.</td>
        </tr>
        <tr>
            <td>Where a sending system can state that a patient is known not to have current medications it is expected an assertion of no relevant finding (Observation) is sent with the appropriate code (i.e. 1234391000168107 |No known current medications|).</td>
        </tr>
        <tr>
        <td>Where a sending system wants to include an observation other than an assertion of no relevant finding, the observation will be outside the section and will be referred to from one of the entries in the section.</td>
        </tr>
    </tbody>
</table>