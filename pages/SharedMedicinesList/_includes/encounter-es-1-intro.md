#### Summary of an Encounter for an Event *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

#### Implementation guidance

For the overarching usage scenarios in this implementation guide it is expected that:

* status will be 'finished' 
* the following elements are not likely to be sent but are encouraged:
  * class
  * reason
* type will support categorisation of the event from which the medicines list was generated, for example a code indicating a home medicines review
* period is equal to or prior to Composition date and List date

For the expected usage scenario of a PSML document the following guidance applies:

* type, if present, has one of the following values 1348931000168107 \|Home medicines review\|, 1348961000168104 \|Community pharmacy medicines review\|, 1348951000168101 \|Hospital medicines review\|, 1348921000168109 \|General practice medicines review\|, 1348941000168103 \|Hospital medicines review upon discharge\|, 1348851000168109 \|Residential care medicines review\| or 1364361000168101 \|Dose administration aid packing facility medicines review\|