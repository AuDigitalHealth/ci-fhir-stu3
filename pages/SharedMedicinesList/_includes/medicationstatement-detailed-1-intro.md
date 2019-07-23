#### Detailed Statement of Known Medicine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Implementation guidance

For the overarching usage scenarios in this implementation guide:
* A medicine item that has not yet been taken or has never been taken should be represented with taken ‘n’.
* A medicine item the patient is currently taking or has taken in the past should be represented with taken ‘y’.

MedicationStatement status should be consistent with the value of List flag. A flag value of type recommendation is not directly linked to a MedicationStatement status. The status should represent the current state of the medicine item for the patient (active, completed, new) not the recommendation:

<table class="list" width="100%">
    <tr>
        <th>Item</th>
        <th>List flag</th>
        <th>MedicationStatement status</th>
    </tr>
    <tr>
        <td>new medicine item</td>
        <td>‘new’ or ‘prescribed’</td>
        <td>Will be represented with a status of ‘intended’</td>
    </tr>
    <tr>
        <td>existing unchanged medicine item</td>
        <td>‘nochange’</td>
        <td>Will be represented with a status of ‘active’ or ‘completed’ depending if the patient is currently (active) taking the medicine item</td>
    </tr>
    <tr>
        <td>existing changed medicine item</td>
        <td>‘amended’</td>
        <td>Will be represented with a status of ‘active’</td>
    </tr>
    <tr>
        <td>ceased medicine item</td>
        <td>‘ceased’</td>
        <td>Will be be represented with a status of ‘stopped’ or ‘completed’</td>
    </tr>   
    <tr>
        <td>withheld medicine item</td>
        <td>‘suspended’</td>
        <td>Will be represented with a status of ‘on-hold’</td>
    </tr>               
</table>

The datetime in effective[x] is to be interpreted in regards to the combination of status and/or taken values:
<table  class="list" width="100%">
    <tr>
        <th>taken</th>
        <th>status</th>
        <th>Intepretation</th>
    </tr>
    <tr>
        <td>'n'</td>
        <td>‘active’ ‘on-hold’ or ‘intended’</td>
        <td>effective[x] is the interval of time during which it is being asserted the patient intends to take or is instructed to take a medicine item</td>
    </tr>
    <tr>
        <td>'n'</td>
        <td>‘completed’</td>
        <td>effective[x] is the interval of time during which it is being asserted that the patient was not taking a medicine</td>
    </tr>
    <tr>
        <td>'y'</td>
        <td>‘active’, ‘on-hold’ or ‘intended’</td>
        <td>effective[x] is the interval of time during which it is being asserted that the patient is taking a medicine. The end date of the period is expected to be omitted; if included, the end date represents the date the patient is expected to stop taking a medicine item.</td>
    </tr>   
    <tr>
        <td>'y'</td>
        <td>‘completed’</td>
        <td>effective[x] is the interval of time during which it is being asserted that the patient was taking a medicine.</td>
    </tr>               
</table>



  