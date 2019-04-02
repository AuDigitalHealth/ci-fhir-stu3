{:.no_toc}
<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->
* Do not remove this line (it will not be displayed)
{:toc}
### Summary Statement of Allergy or Intolerance *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Usage scenarios

The following are the usage scenarios expected:

* A summary statement for an allergy or intolerance exchanged as referenced entry in a composition.

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing profiles. 


#### Implementation guidance
* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content
* If an authoring system only has substance or agent available and not a statement of allergy intolerance that substance should be recorded in the code and optionally reaction.substance.
* For the usage scenario for this profile it is expected that verificationStatus will be ‘unconfirmed’ (where a sending system does not clearly have this element this should be the value sent), but may be ‘confirmed’. A ‘refuted’ allergy should be represented with an appropriate negation code.
* For the usage scenarios for this profile it is expected that the clinicalStatus will be ‘active’.


