# {{ page.title }}
{% include publish-box.html %}
This informative section provides mapping from the data items (i.e. requirements) in [Consumer Entered Notes Information Requirements [NEHT2011ao]](index.html#NEHT2011ao) and  [Consumer Entered Health Summary Information Requirements [NEHT2011ar]](index.html#NEHT2011ar).

### Personal Health Notes
The table below matches the data items to the corresponding supported element in the Personal Health Notes profile or referenced profile (e.g. Organization with Mandatory Identifier). The hierarchy column demonstrates the path to that supported element from the root Composition. 

<table class="list" width="100%">
               <thead>
                    <tr>						
						<th>Requirement Section</th>
						<th>Data item</th>
						<th>Element</th>
						<th>Hierarchy</th>
					</tr>
               </thead>
               <tfoot>
					<tr>
						<td></td>
						<td></td>
						<td></td>
						<td></td>
					</tr>
               </tfoot> 
               <tbody>
					<tr>
						<td rowspan="6">Individual</td>					
						<td rowspan="2">Component</td>
						<td>Patient</td>
						<td>Composition(Personal Health Notes).subject(Patient as Patient with Mandatory IHI).Patient</td>
					</tr>
					<tr>
						<td>Patient</td>
						<td>Composition(Personal Health Notes).author(Patient as Patient with Mandatory IHI).Patient</td>
					</tr>
					<tr>
						<td rowspan="2">Person Name</td>
						<td>Patient.name</td>
						<td>Composition(Personal Health Notes).subject(Patient as Patient with Mandatory IHI).Patient.name</td>
					</tr>
					<tr>
						<td>Patient.name</td>
						<td>Composition(Personal Health Notes).author(Patient as Patient with Mandatory IHI).Patient.name</td>
					</tr>
					<tr>
						<td rowspan="2">Person Identifier</td>
						<td>Patient.identifier</td>
						<td>Composition(Personal Health Notes).subject(Patient as Patient with Mandatory IHI).Patient.identifier</td>
					</tr>
					<tr>
						<td>Patient.identifier</td>
						<td>Composition(Personal Health Notes).author(Patient as Patient with Mandatory IHI).Patient.identifier</td>
					</tr>
					<tr>
						<td rowspan="2">Author's Name (Authorised Representative)</td>					
						<td>Component</td>
						<td>RelatedPerson</td>
						<td>Composition(Personal Health Notes).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson</td>
					</tr>
					  <tr>				
						<td>Author's Name (Authorised Representative)</td>
						<td>RelatedPerson.name</td>
						<td>Composition(Personal Health Notes).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.name</td>
					</tr> 					
					<tr>
						<td rowspan="5">Notes</td>					
						<td>Component</td>
						<td>Composition.section</td>
						<td>Composition(Personal Health Notes).section</td>
					</tr>
					<tr>
						<td>Date Information Entered</td>
						<td>Composition.date</td>
						<td>Composition(Personal Health Notes).date</td>
					</tr>
					<tr>
						<td rowspan="2">Issue Title</td>
						<td>Composition.section.title</td>
						<td>Composition(Personal Health Notes).section.title</td>
					</tr>
					<tr>
						<td>Composition.section.text</td>
						<td>Composition(Personal Health Notes).section.text</td>
					</tr>
					<tr>
						<td>Issue Description</td>
						<td>Composition.section.text</td>
						<td>Composition(Personal Health Notes).section.text</td>
					</tr> 					
					<tr>
						<td rowspan="2">Document Control</td>					
						<td>Component</td>
						<td>n/a</td>
						<td>n/a</td>
					</tr>
					<tr>
						<td>DateTime Completed</td>	
						<td>n/a</td>
						<td>n/a</td>
					</tr>
			   </tbody>
 </table>
  
    
     
    
	
### Personal Health Summary
The table below matches the data items to the corresponding supported element in the Personal Health Summary profile or referenced profile (e.g. Organization with Mandatory Identifier). The hierarchy column demonstrates the path to that supported element from the root Composition. 

<table class="list" width="100%">
               <thead>
                    <tr>						
						<th>Requirement Section</th>
						<th>Data item</th>
						<th>Element</th>
						<th>Hierarchy</th>
					</tr>
               </thead>
               <tfoot>
					<tr>
						<td></td>
						<td></td>
						<td></td>
						<td></td>
					</tr>
               </tfoot> 
               <tbody>
					<tr>
						<td rowspan="14">Individual</td>					
						<td rowspan="2">Component</td>
						<td>Patient</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient</td>
					</tr>
					<tr>
						<td>Patient</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient</td>
					</tr>										
					<tr>
						<td rowspan="2">Person Name</td>
						<td>Patient.name</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.name</td>
					</tr>
					<tr>
						<td>Patient.name</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient.name</td>
					</tr>
					<tr>
						<td rowspan="2">Person Identifier</td>
						<td>Patient.identifier</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.identifier</td>
					</tr>
					<tr>
						<td>Patient.identifier</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient.identifier</td>
					</tr>
					<tr>
						<td>Date of Birth</td>
						<td>Patient.birthDate</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.birthDate</td>
					</tr>
					<tr>
						<td>Sex</td>
						<td>Patient.gender</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.gender</td>
					</tr>
					<tr>
						<td rowspan="2">Address</td>
						<td>Patient.address</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.address</td>
					</tr>
					<tr>
						<td>Patient.address</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient.address</td>
					</tr>
					<tr>
						<td rowspan="2">Communication Details</td>
						<td>Patient.telecom</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.telecom</td>
					</tr>
					<tr>
						<td>Patient.telecom</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient.telecom</td>
					</tr>
					<tr>
						<td rowspan="2">Indigenous Status</td>
						<td>Patient.indigenous-status</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.indigenous-status</td>
					</tr>
					<tr>
						<td>Patient.indigenous-status</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient.indigenous-status</td>
					</tr>					
					<tr>
						<td rowspan="5">Authorised Representative</td>					
						<td>Component</td>
						<td>RelatedPerson</td>
						<td>Composition(Personal Health Summary).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson</td>
					</tr>
					<tr>				
						<td>Author's Name (Authorised Representative)</td>
						<td>RelatedPerson.name</td>
						<td>Composition(Personal Health Summary).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.name</td>
					</tr>
					<tr>
						<td>Person Identifier</td>
						<td>RelatedPerson.identifier</td>
						<td>Composition(Personal Health Summary).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.identifier</td>
					</tr>  
					<tr>
						<td>Address</td>
						<td>RelatedPerson.address</td>
						<td>Composition(Personal Health Summary).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.address</td>
					</tr> 
					<tr>
						<td>Communication Details</td>
						<td>RelatedPerson.telecom</td>
						<td>Composition(Personal Health Summary).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.telecom</td>
					</tr>             
					<tr>
						<td rowspan="6">Allergies and Adverse Reactions</td>
						<td rowspan="3">Component</td>
						<td>Composition.section</td>
						<td>Composition(Personal Health Summary).section(Allergies)</td>
					</tr>
					<tr>
						<td>Composition.section.entry</td>
						<td>Composition(Personal Health Summary).section(Allergies).entry</td>
					</tr>
					<tr>
						<td>Composition.section.emptyReason</td>
						<td>Composition(Personal Health Summary).section(Allergies).emptyReason</td>
					</tr>           
					<tr>
						<td rowspan="2">Agent Description</td>
						<td>AllergyIntolerance.code</td>
						<td>Composition(Personal Health Summary).section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.code</td>
					</tr>
					<tr>
						<td>AllergyIntolerance.reaction.substance</td>
						<td>Composition(Personal Health Summary).section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.substance</td>
					</tr>           
					<tr>
						<td>Reaction Description</td>
						<td>AllergyIntolerance.reaction.manifestation</td>
						<td>Composition(Personal Health Summary).section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.manifestation</td>
					</tr>              
				   <tr>
						<td rowspan="7">Medicines</td>
						<td rowspan="3">Component</td>
						<td>Composition.section</td>
						<td>Composition(Personal Health Summary).section(Medications)</td>
					</tr>
					<tr>
						<td>Composition.section.entry</td>
						<td>Composition(Personal Health Summary).section(Medications).entry</td>
					</tr>
					<tr>
						<td>Composition.section.emptyReason</td>
						<td>Composition(Personal Health Summary).section(Medications).emptyReason</td>
					</tr>                
					<tr>
						<td>Item Description</td>
						<td>MedicationStatement.medication[x]</td>
						<td>Composition(Personal Health Summary).section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.medication[x]</td>
					</tr>                          
					<tr>
						<td>Dose Information</td>
						<td>MedicationStatement.dosage</td>
						<td>Composition(Personal Health Summary).section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.dosage</td>
					</tr>                              
					<tr>
						<td>Reason for Medicine</td>
						<td>MedicationStatement.reasonCode</td>
						<td>Composition(Personal Health Summary).section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.reasonCode</td>
					</tr>                              
					<tr>
						<td>Additional Comments</td>
						<td>MedicationStatement.note</td>
						<td>Composition(Personal Health Summary).section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.note</td>
					</tr> 					
					<tr>
						<td rowspan="2">Document Control</td>					
						<td>Component</td>
						<td>n/a</td>
						<td>n/a</td>
					</tr>
					<tr>
						<td>DateTime Input</td>	
						<td>n/a</td>
						<td>n/a</td>
					</tr>
            </tbody>
        </table>