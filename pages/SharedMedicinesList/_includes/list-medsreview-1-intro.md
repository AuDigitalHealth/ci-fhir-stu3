### List of Medicine Items for a Patient *[[Draft](http://hl7.org/fhir/stu3/valueset-publication-status.html)]*

<span style="color:red">*Usage scenarios, implementation guidance, known issues, profile title, url - to be updated*</span>

#### Usage scenarios

* A medicine list exchanged as a referenced entry in a Composition

Further scoping of applicable usage scenarios (e.g. point-to-point or point-to-share) is done at the referencing Composition profile.

#### Implementation guidance

For the expected usage scenarios in this implementation guide:

* When list is used in Composition
<table class="list" width="100%">
  <tr>
    <th>Element</th>
    <th>Guidance</th>
   </tr>
     <tr>
        <td>list source role</td>
        <td>Expected to be the same as the authoring role of the referencing Composition</td>
    </tr>
   <tr>
        <td>subject</td>
        <td>Expected to be the same as the subject of the referencing Composition</td>
    </tr>   
   <tr>
        <td>date</td>
        <td>Expected to be the same as the date of the referencing Composition</td>
    </tr>   
   <tr>
        <td>source</td>
        <td>Expected to be the same as the author of the referencing Composition</td>
    </tr>    
  </table> 


* 
* All medicine items that the patient is taking should be included in the list:

<table class="list" width="100%">
  <tr>
    <th>Item</th>
    <th>Guidance</th>
   </tr>
     <tr>
        <td>Existing unchanged medicine items</td>
        <td>flag  will be 'unchanged' and change description is not expected to be provided</td>
    </tr>
   <tr>
        <td>New medicine items</td>
        <td>Change description is expected to be provided</td>
    </tr>   
   <tr>
        <td>Changed medicine items</td>
        <td>Change description is expected to be provided</td>
    </tr>   
   <tr>
        <td>Ceased medicine item</td>
        <td>flag will be 'ceased' and change description is expected to be provided</td>
    </tr>    
  </table>
    


#### Known issues: 
*


