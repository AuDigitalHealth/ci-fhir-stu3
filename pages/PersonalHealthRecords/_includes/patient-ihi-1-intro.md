### Patient with Mandatory IHI

#### Usage scenarios
The following are the usage scenarios expected:

* TBD


#### Implementation guidance
* Medical Record Number: identifier.system can be completed using the [HPI-O based Medical Record Identifier](http://ns.electronichealth.net.au/id/local/provider/1.0) namespace if an organisation does not have its own namespace and has an HPI-O. An example of the syntax using this namespace is "http://ns.electronichealth.net.au/id/local/medicalrecord/1.0/8003620000000000". The dummy HPI-O should be replaced with the assigning entity's own HPI-O.

#### Known issues
* Due to a tolling issue the must support flag is missing for the below elements:
    * Patient.deceasedDateTime.date-accuracy-indicator


#### Examples
This section provides examples that conform to the requirements specified within this implementation guide.

* TBD