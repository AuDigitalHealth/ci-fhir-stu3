# {{ page.title }}

This informative section provides mapping from the data items (i.e. requirements) in [NEHTA Personal Health Notes Information Requirements](https://www.digitalhealth.gov.au/implementation-resources/clinical-documents/EP-2282-2016/NEHTA-0955-2011) [] and [NEHTA Personal Health Summary Information Requirements](https://www.digitalhealth.gov.au/implementation-resources/clinical-documents/personal-health-summary/NEHTA-0950-2011) [].

### Personal Health Notes
The table below matches the data items to the corresponding supported element in the Personal Health Notes (PHN) profile or referenced profile (e.g. Organization with Mandatory Identifier). The hierarchy column demonstrates the path to that supported element from the root Composition. 

<table class="list" width="100%">
<!-- Table 1 : Personal Health Notes --> 
               <thead>
                    <tr>
						<th>Data Item</th>						
						<th>Req. No**</th>
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
<!-- Component: Individual --> 
					<tr>
						<td>Individual</td>					
						<td></td>
						<td>Patient</td>
						<td>Composition.subject(Patient as Patient with Mandatory IHI).Patient</td>
					</tr>
					<tr>
						<td>Person Name</td>
						<td></td>
						<td>Patient.name</td>
						<td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.name</td>
					</tr>
					<tr>
						<td>Person Identifier</td>
						<td></td>
						<td>Patient.identifier</td>
						<td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.identifier</td>
					</tr>
<!-- Component: Author's Name (Authorised Representative) --> 
<!-- 					<tr>
						<td rowspan="2">Author's Name (Authorised Representative)</td>
						<td></td>
						<td>Patient.name</td>
						<td>Composition.author(Patient as Patient with Mandatory IHI).Patient.name</td>
					</tr>  --> 
					  <tr>
						<td>Author's Name (Authorised Representative)</td>						
						<td></td>
						<td>RelatedPerson.name</td>
						<td>Composition.author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.name</td>
					</tr> 
<!-- Component: Notes --> 
<!--					<tr>
						<td>Notes</td>					
						<td></td>
						<td>Composition</td>
						<td>Composition</td>
					</tr>  -->
					<tr>
						<td>Date Information Entered</td>
						<td></td>
						<td>date</td>
						<td>Composition.date</td>
					</tr>
					<tr>
						<td>Issue Title</td>
						<td></td>
						<td>section.title</td>
						<td>Composition.section.title</td>
					</tr>
					<tr>
						<td>Issue Description</td>
						<td></td>
						<td>section.text</td>
						<td>Composition.section.text</td>
					</tr>
<!-- Component: Document Control --> 
					<tr>
						<td>DateTime Completed</td>					
						<td></td>
						<td>Incomplete: Please see note below*</td>
						<td>Incomplete: Please see note below*</td>
					</tr>
			   </tbody>
 </table>
  
    
     
    
	
### Personal Health Summary
The table below matches the data items to the corresponding supported element in the Personal Health Summary profile or referenced profile (e.g. Organization with Mandatory Identifier). The hierarchy column demonstrates the path to that supported element from the root Composition. 

<table class="list" width="100%">
<!-- Table 1 : Personal Health Summary --> 
               <thead>
                    <tr>
						<th>Data Item</th>						
						<th>Req. No**</th>
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
 <!-- Component: Individual --> 
                <tr>
                    <td>Individual</td>					
                    <td></td>
                    <td>Patient</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient</td>
                </tr>
                <tr>
                    <td>Person Name</td>
                    <td></td>
                    <td>Patient.name</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.name</td>
                </tr>
                <tr>
                    <td>Person Identifier</td>
                    <td></td>
                    <td>Patient.identifier</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.identifier</td>
                </tr>
                <tr>
                    <td>Date of Birth</td>
                    <td></td>
                    <td>Patient.birthDate</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.birthDate</td>
                </tr>
                <tr>
                    <td>Sex</td>
                    <td></td>
                    <td>Patient.gender</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.gender</td>
                </tr>
                <tr>
                    <td>Address</td>
                    <td></td>
                    <td>Patient.address</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.address</td>
                </tr>
                <tr>
                    <td>Communication Details</td>
                    <td></td>
                    <td>Patient.contact</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.contact</td>
                </tr>
                <tr>
                    <td>Indigenous Status</td>
                    <td></td>
                    <td>Patient.indigenous-status</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.indigenous-status</td>
                </tr>
<!-- Component: Author's Name (Authorised Representative) --> 
				<tr>
					<td>Author's Name (Authorised Representative)</td>						
					<td></td>
					<td>RelatedPerson.name</td>
					<td>Composition.author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.name</td>
				</tr>  
				<tr>
					<td>Person Identifier</td>						
					<td></td>
					<td>RelatedPerson.identifier</td>
					<td>Composition.author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.identifier</td>
				</tr>  
				<tr>
					<td>Address</td>						
					<td></td>
					<td>RelatedPerson.address</td>
					<td>Composition.author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.address</td>
				</tr> 
				<tr>
					<td>Communication Details</td>						
					<td></td>
					<td>RelatedPerson.telecom</td>
					<td>Composition.author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.telecom</td>
				</tr>
<!-- Component: Allergies and Adverse Reactions -->              
                <tr>
                    <td rowspan="4">Allergies and Adverse Reactions</td>
                    <td rowspan="3"></td>
                    <td>section(Allergies)</td>
                    <td>Composition.section(Allergies)</td>
                </tr>
                <tr>
                    <td>section(Allergies).entry</td>
                    <td>Composition.section(Allergies).entry</td>
                </tr>
                <tr>
                    <td>section(Allergies).emptyReason</td>
                    <td>Composition.section(Allergies).emptyReason</td>
                </tr>
                <tr>
                    <td rowspan="1"></td>
                    <td>section(Allergies).text</td>
                    <td>Composition.section(Allergies).text</td>
                </tr>             
                <tr>
                    <td rowspan="2">Agent Description</td>
                    <td></td>
                    <td>AllergyIntolerance.code</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.code</td>
                </tr>
                <tr>
                    <td></td>
                    <td>AllergyIntolerance.reaction.substance</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.substance</td>
                </tr>              
<!--                <tr>
                    <td rowspan="2">Reaction Type</td>
                    <td></td>
                    <td>AllergyIntolerance.type</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.type</td>
                </tr>
                <tr>
                    <td></td>
                    <td>AllergyIntolerance.type</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.type</td>
                </tr>    -->           
                <tr>
                    <td>Reaction Description</td>
                    <td></td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.manifestation</td>
                </tr>
<!-- Component: Medicines -->               
               <tr>
                    <td rowspan="3">Medications</td>
                    <td></td>
                    <td>section(Medications)</td>
                    <td>Composition.section(Medications)</td>
                </tr>
                <tr>
                    <td></td>
                    <td>section(Medications).entry</td>
                    <td>Composition.section(Medications).entry</td>
                </tr>
                <tr>
                    <td></td>
                    <td>section(Medications).emptyReason</td>
                    <td>Composition.section(Medications).emptyReason</td>
                </tr>                
                <tr>
                    <td>Item Description</td>
                    <td></td>
                    <td>MedicationStatement</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement</td>
                </tr>               
<!--            <tr>
                    <td rowspan="2">Status</td>
                    <td></td>
                    <td>MedicationStatement.status</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.status</td>
                </tr> -->                            
                <tr>
                    <td>Dose Information</td>
                    <td></td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.dosage</td>
                </tr>                              
                <tr>
                    <td>Reason for Medicine</td>
                    <td></td>
                    <td>MedicationStatement.reasonCode</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.reasonCode</td>
                </tr>                              
                <tr>
                    <td>Additional Comments</td>
                    <td></td>
                    <td>MedicationStatement.note</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.note</td>
                </tr>
<!-- Component: Document Control -->  
				<tr>
                    <td>DateTime Input</td>
                    <td></td>
                    <td>attester.time</td>
                    <td>Composition.attester.time</td>
                </tr>
            </tbody>
        </table>
<p>*Note 1: The design of this section is incomplete. The intended structure mapping is not yet available.</p>
<p>**Note 2: The requirement numbers are not available in the information requirements.</p>