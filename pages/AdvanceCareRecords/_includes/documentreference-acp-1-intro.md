## Advance Care Planning Document Reference

The purpose of this profile is to define a representation of an attached Advance Care Planning document with some metadata. 

#### Usage Scenarios
The following are the usage scenarios expected:

* A clinical information system (CIS) sends or receives an Advance Care Plan with the My Health Record system
* A clinical information system (CIS) sends or receives an Advance Care Document Reference with the My Health Record system
* A contracted service provider (CSP) sends or receives an Advance Care Plan with the My Health Record system
* A contracted service provider (CSP) sends or receives an Advance Care Document Reference with the My Health Record system
* A CIS sends or receives an Advance Care Plan with another CIS or CSP
* A CIS sends or receives an Advance Care Document Reference with another CIS or CSP
* A CSP sends or receives an Advance Care Plan with a CIS or another CSP
* A CSP sends or receives an Advance Care Document Reference with a CIS or another CSP
* A registered repository or registered portal receives an Advance Care Plan
* A registered repository or registered portal receives an Advance Care Document Reference
* A system may be a producer by attaching the Advance Care Plan document to the Document Reference and sending that Document Reference.

#### Profile specific implementation guidance

* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
