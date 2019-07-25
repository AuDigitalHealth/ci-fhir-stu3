### Summary of an Encounter for an Event *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

##### Implementation guidance

For the overarching usage scenarios in this implementation guide:

* It is expected that the status will be 'finished'. 
* The following elements are not expected to be provided but are encouraged if the sending system has this capability:
  * class
  * type
  * reason
* If provided, type is expected to support categorisation of the event from which the medicines list was generated, for example a code indicating a 'home medicines review' or 'pharmacist medicines review'.
* Period is expected to be equal to or prior to the Composition date and the List date.

For the expected usage scenario of a PSML document the following guidance applies:

* It is expected that type with one of the following values will be provided: 'Home medicine review', 'Community pharmacy medicine review', 'Hospital pharmacy medicine review', 'Non-dispensing pharmacy medicine review', 'Medicine review at discharge', 'Residential care medicine review' and 'DAA packing pharmacy medicine review'. 


