#### Detailed Statement of Known Medicine *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Implementation guidance

For the supported scenarios in this implementation guide:

* MedicationStatement status should be consistent with the value of List flag:
    * A medicine item ceased during this event should be represented with a status of 'stopped' or 'completed'.
    * A medicine item introduced during this event should be represented with a status of 'intended'.
    * An existing unchanged medicine item should be represented with a status of 'active' or 'completed' depending if the patient is currently (active) taking the medicine item.
    * A medicine item changed during this event should be represented with a status of 'active'.
    * recommendation to make a change may not directly result in a similar status unless it is a recommendation to introduce a medicine item. The status should represent the current state of the medicine item for the patient (active, completed, new) not the recommendation.

* MedicationStatement taken should be consistent with the value of List flag:
    * medicine item that has not yet been taken or has never been taken should be represented with taken 'n'.
    * medicine item the patient is currently taking or has taken should be represented with taken 'y'.



