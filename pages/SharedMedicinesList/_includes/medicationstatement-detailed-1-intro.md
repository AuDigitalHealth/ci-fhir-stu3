#### Detailed Statement of Known Medicine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Implementation guidance

For the supported scenarios in this implementation guide:

* MedicationStatement status should be consistent with the value of List flag:
    * A medicine item ceased during this event should be represented with a status of 'stopped' or 'completed'.
    * A medicine item introduced during this event should be represented with a status of 'intended'.
    * An existing unchanged medicine item should be represented with a status of 'active' or 'completed' depending if the patient is currently (active) taking the medicine item.
    * A medicine item changed during this event should be represented with a status of 'active'.
    * Recommendation to make a change may not directly result in a similar status unless it is a recommendation to introduce a medicine item. The status should represent the current state of the medicine item for the patient (active, completed, new) not the recommendation.

* MedicationStatement taken should be consistent with the value of List flag:
    * A medicine item that has not yet been taken or has never been taken should be represented with taken 'n'.
    * A medicine item the patient is currently taking or has taken should be represented with taken 'y'.

* MedicationStatement effective should be interpreted in regards to the combination of status and/or taken values:
    * When taken is 'n' and status is 'active' 'on-hold' or 'intended', the effective[x] is the interval of time during which it is being asserted  the patient intends to take or is instructed to take a medicine item
    * When taken is 'y' and status is 'active', 'on-hold' or 'intended', the effective[x] is the interval of time during which it is being asserted that the patient is taking a medicine. The end date of the period is expected to be omitted; if included, the end date represents the date the patient is expected to stop taking a medicine item.
    * When taken is 'n' and status is 'completed', the effective[x] is the interval of time during which it is being asserted that the patient was not taking a medicine.
    * When taken is 'y' and status is 'completed', the effective[x] is the interval of time during which it is being asserted that the patient was taking a medicine. 

* If structured dosage is included, 

* Additinal information about a medicine item that cannot be included in one of the existing elements is expected to be included in note.

  