## List of Medicine Changes from an Event *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

The purpose of this profile is to provide a list of medicines that have specifically changed as a result of an event or those medicines directly relevant to an event. The list is intended to be suited to handling and exchange as a referenced entry in a Composition.

### Usage scenarios
* A medicine list exchanged as a referenced entry in a Composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing Composition profile.


#### Must Support

In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.

The system SHALL be able to store and retrieve the following elements: 
* status
* code
* date
* entry
* entry.change-description
* entry.flag
* entry.item
* source

The system SHALL be able to take the following elements into account when performing processing:
* subject

## Profile specific implementation guidance:

* Where additional content beyond that flagged with must support is provided it:

    * shall not qualify or negate content described by this profile as must support

    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content

* When date is provided, it is expected to be the same as the date of the referencing Composition
* When source is provided, it is expected to be the same as the author of the referencing Composition
* All medicine items relevant to an event should be included in the list
    * For existing unchanged medicine items, the flag  will be 'unchanged' and change description is not expected to be provided
    * For new and changed medicine items, change description is expected to be provided

