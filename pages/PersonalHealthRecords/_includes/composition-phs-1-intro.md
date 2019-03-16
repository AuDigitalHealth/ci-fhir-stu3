This profile defines a representation of a Personal Health Summary document for a patient in an Australian healthcare context. 

##### **Usage Scenarios**
The following are the usage scenarios expected:
* An individual or their authorised representative authors a personal health summary document to be exchanged with the My Health Record system

##### **Profile-specific implementation guidance**
* For the usage scenarios for this profile it is required that the composition include only the specified top-level sections; additional sections to handle local content not covered by the primary design can be included as a child section if necessary.
* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
* For each section included in the composition it is important to differentiate between affirmatively stating a patient has no relevant findings (e.g. no history of immunisation) versus a finding that a patient does not have a specific condition (e.g. no latex allergy) versus not including findings in the record (e.g. not applicable or unknown).
* In Allergies section:
    * Where a sending system does not have any clinical data to provide in that section it is expected that section.emptyReason is used
    * Where a sending system can state that a patient does not have an allergy or category of allergies it is expected that an AllergyIntolerance resource is sent with the appropriate negation code (e.g. 160244002 &#124;No Known Allergies&#124;) is sent as the code
* In Medications section:
    * Where a sending system does not have any clinical data to provide in that section it is expected that section.emptyReason is used
    * Where a sending system can state that a patient is known not to have current medications  (relevant to Medications) it is expected an observation of assertion of no relevant finding is sent with the appropriate code (e.g. 1234391000168107 &#124;No known current medications&#124;)

##### **Examples**

[Personal Health Summary example 1](Composition-426e957a-3c4c-4780-98f3-8339cc1e6f7c.html)

[Personal Health Summary example 2](Composition-dc32838b-faf3-4102-9c78-27186ac32e20.html)

[Personal Health Summary example 3](Composition-fb584f29-e4cc-4f55-ba2e-7bdf03c7a5ee.html)

[Personal Health Summary example 4](Composition-340fcbec-f501-4582-9be1-4627618119e3.html)

[Personal Health Summary example 5](Composition-28d02fcf-6b64-49c1-8870-6533059b8129.html)
