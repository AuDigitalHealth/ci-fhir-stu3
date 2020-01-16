#### Medicine Item Statement *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is expected that a sending system will set the value of taken as per the guidance in the Comments field of the [MedicationStatement](StructureDefinition-medicationstatement-detailed-1-definitions.html#MedicationStatement) element.

The value of status is expected to represent the current state of the medicine item for the patient (active, completed, new) and be consistent with the value of the List.entry.flag, as per the guidance in the following table.

<table class="list" width="100%">
	<col style="width:25%"/>
	<col style="width:50%"/>
	<col style="width:25%"/>
    <tr>
        <th>Item</th>
        <th>List.entry.flag</th>
        <th>MedicationStatement.status</th>
    </tr>
    <tr>
        <td>new medicine item</td>
        <td>‘new’ or ‘prescribed’</td>
        <td>'intended'</td>
    </tr>
    <tr>
        <td>existing unchanged medicine item</td>
        <td>‘nochange’</td>
        <td>'active' or 'completed'</td>
    </tr>
    <tr>
        <td>existing changed medicine item</td>
        <td>‘amended’</td>
        <td>'active'</td>
    </tr>
    <tr>
        <td>ceased medicine item</td>
        <td>‘ceased’</td>
        <td>'stopped' or 'completed'</td>
    </tr>
    <tr>
        <td>withheld medicine item</td>
        <td>‘suspended’</td>
        <td>'on-hold'</td>
    </tr>
    <tr>
        <td>recommended medicine item</td>
        <td>'new-recommended' or 'prescription-recommended'</td>
        <td>'intended'</td>
    </tr>
    <tr>
        <td>existing medicine item</td>
        <td>'review-recommended' or 'cessation-recommended' or 'suspension-recommended' or 'cancellation-recommended'</td>
        <td>'active'</td>
    </tr>
</table>

The datetime in effective[x] is to be interpreted in regards to the combination of status and/or taken values, as per the guidance in the following table.

<table  class="list" width="100%">
	<col style="width:25%"/>
	<col style="width:25%"/>
	<col style="width:50%"/>
    <tr>
        <th>MedicationStatement.taken</th>
        <th>MedicationStatement.status</th>
        <th>Interpretation</th>
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
        <td>effective[x] is the interval of time during which it is being asserted that the patient was taking a medicine</td>
    </tr>               
</table>

This profile is referenced by [List of Medicine Items with Change Information Authored by Practitioner](StructureDefinition-list-sml-pracchanges-1.html). 