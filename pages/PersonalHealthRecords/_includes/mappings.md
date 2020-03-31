# {{ page.title }}
{% include publish-box.html %}
{:.no_toc}
<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->
* Do not remove this line (it will not be displayed)
{:toc}

## Introduction

This informative section provides a mapping from the requirements of each end-product clinical specification to elements in a profiled FHIR resource.

The mapping from requirements table below demonstrates the logical decomposition of each requirement to the lowest possible element in an applicable profile. 

## Mapping from Personal Health Notes information requirements

The table below provides mapping from the requirements in [Consumer Entered Notes Information Requirements [NEHT2011ao]](index.html#NEHT2011ao) to the corresponding supported element in the [Personal Health Notes](StructureDefinition-composition-phn-1.html) profile, or referenced profile (e.g. [Organization with Mandatory Identifier](StructureDefinition-organization-ident-1.html)). 

See the [legend](mappings.html#legend-for-mapping-from-requirements) for information on the columns used to present the mapping content.


<table class="list" width="100%">
	<col style="width:20%"/>
	<col style="width:7%"/>
	<col style="width:20%"/>
	<col style="width:25%"/>
	<col style="width:28%"/>
               <thead>
                    <tr>						
						<th>Requirement Section</th>
						<th>Data item</th>
						<th>Element name</th>
						<th>Hierarchy</th>
						<th>Additional notes</th>
					</tr>
               </thead>
               <tfoot>
					<tr>
						<td></td>
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
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td>Patient</td>
						<td>Composition(Personal Health Notes).author(Patient as Patient with Mandatory IHI).Patient</td>
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td rowspan="2">Person Name</td>
						<td>Patient.name</td>
						<td>Composition(Personal Health Notes).subject(Patient as Patient with Mandatory IHI).Patient.name</td>
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td>Patient.name</td>
						<td>Composition(Personal Health Notes).author(Patient as Patient with Mandatory IHI).Patient.name</td>
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td rowspan="2">Person Identifier</td>
						<td>Patient.identifier</td>
						<td>Composition(Personal Health Notes).subject(Patient as Patient with Mandatory IHI).Patient.identifier</td>
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td>Patient.identifier</td>
						<td>Composition(Personal Health Notes).author(Patient as Patient with Mandatory IHI).Patient.identifier</td>
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td rowspan="2">Author's Name (Authorised Representative)</td>					
						<td>Component</td>
						<td>RelatedPerson</td>
						<td>Composition(Personal Health Notes).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson</td>
						<td></td>
						<td></td>
					</tr>
					  <tr>				
						<td>Author's Name (Authorised Representative)</td>
						<td>RelatedPerson.name</td>
						<td>Composition(Personal Health Notes).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.name</td>
						<td></td>
						<td></td>
					</tr> 					
					<tr>
						<td rowspan="5">Notes</td>					
						<td>Component</td>
						<td>Composition.section</td>
						<td>Composition(Personal Health Notes).section</td>
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td>Date Information Entered</td>
						<td>Composition.date</td>
						<td>Composition(Personal Health Notes).date</td>
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td rowspan="2">Issue Title</td>
						<td>Composition.section.title</td>
						<td>Composition(Personal Health Notes).section.title</td>
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td>Composition.section.text</td>
						<td>Composition(Personal Health Notes).section.text</td>
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td>Issue Description</td>
						<td>Composition.section.text</td>
						<td>Composition(Personal Health Notes).section.text</td>
						<td></td>
						<td></td>
					</tr> 					
					<tr>
						<td rowspan="2">Document Control</td>					
						<td>Component</td>
						<td>n/a</td>
						<td>n/a</td>
						<td></td>
						<td></td>
					</tr>
					<tr>
						<td>DateTime Completed</td>	
						<td>n/a</td>
						<td>n/a</td>
						<td></td>
						<td></td>
					</tr>
			   </tbody>
 </table>
  
    
     
    
	
## Mapping from Personal Health Summary information requirements

The table below provides mapping from the requirements in [Consumer Entered Health Summary Information Requirements [NEHT2011ar]](index.html#NEHT2011ar) to the corresponding supported element in the [Personal Health Summary](StructureDefinition-composition-phs-1.html) profile, or referenced profile (e.g. [Organization with Mandatory Identifier](StructureDefinition-organization-ident-1.html)). 

See the [legend](mappings.html#legend-for-mapping-from-requirements) for information on the columns used to present the mapping content.

<table class="list" width="100%">
	<col style="width:20%"/>
	<col style="width:7%"/>
	<col style="width:20%"/>
	<col style="width:25%"/>
	<col style="width:28%"/>
               <thead>
                    <tr>						
						<th>Requirement Section</th>
						<th>Data item</th>
						<th>Element name</th>
						<th>Hierarchy</th>
						<th>Additional notes</th>
					</tr>
               </thead>
               <tfoot>
					<tr>
						<td></td>
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
						<td></td>
					</tr>
					<tr>
						<td>Patient</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient</td>
						<td></td>
					</tr>										
					<tr>
						<td rowspan="2">Person Name</td>
						<td>Patient.name</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.name</td>
						<td></td>
					</tr>
					<tr>
						<td>Patient.name</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient.name</td>
						<td></td>
					</tr>
					<tr>
						<td rowspan="2">Person Identifier</td>
						<td>Patient.identifier</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.identifier</td>
						<td></td>
					</tr>
					<tr>
						<td>Patient.identifier</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient.identifier</td>
						<td></td>
					</tr>
					<tr>
						<td>Date of Birth</td>
						<td>Patient.birthDate</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.birthDate</td>
						<td></td>
					</tr>
					<tr>
						<td>Sex</td>
						<td>Patient.gender</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.gender</td>
						<td></td>
					</tr>
					<tr>
						<td rowspan="2">Address</td>
						<td>Patient.address</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.address</td>
						<td></td>
					</tr>
					<tr>
						<td>Patient.address</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient.address</td>
						<td></td>
					</tr>
					<tr>
						<td rowspan="2">Communication Details</td>
						<td>Patient.telecom</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.telecom</td>
						<td></td>
					</tr>
					<tr>
						<td>Patient.telecom</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient.telecom</td>
						<td></td>
					</tr>
					<tr>
						<td rowspan="2">Indigenous Status</td>
						<td>Patient.indigenous-status</td>
						<td>Composition(Personal Health Summary).subject(Patient as Patient with Mandatory IHI).Patient.indigenous-status</td>
						<td></td>
					</tr>
					<tr>
						<td>Patient.indigenous-status</td>
						<td>Composition(Personal Health Summary).author(Patient as Patient with Mandatory IHI).Patient.indigenous-status</td>
						<td></td>
					</tr>					
					<tr>
						<td rowspan="5">Authorised Representative</td>					
						<td>Component</td>
						<td>RelatedPerson</td>
						<td>Composition(Personal Health Summary).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson</td>
						<td></td>
					</tr>
					<tr>				
						<td>Author's Name (Authorised Representative)</td>
						<td>RelatedPerson.name</td>
						<td>Composition(Personal Health Summary).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.name</td>
						<td></td>
					</tr>
					<tr>
						<td>Person Identifier</td>
						<td>RelatedPerson.identifier</td>
						<td>Composition(Personal Health Summary).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.identifier</td>
						<td></td>
					</tr>  
					<tr>
						<td>Address</td>
						<td>RelatedPerson.address</td>
						<td>Composition(Personal Health Summary).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.address</td>
						<td></td>
					</tr> 
					<tr>
						<td>Communication Details</td>
						<td>RelatedPerson.telecom</td>
						<td>Composition(Personal Health Summary).author(RelatedPerson as Related Person with Mandatory IHI).RelatedPerson.telecom</td>
						<td></td>
					</tr>             
					<tr>
						<td rowspan="6">Allergies and Adverse Reactions</td>
						<td rowspan="3">Component</td>
						<td>Composition.section</td>
						<td>Composition(Personal Health Summary).section(Allergies)</td>
						<td></td>
					</tr>
					<tr>
						<td>Composition.section.entry</td>
						<td>Composition(Personal Health Summary).section(Allergies).entry</td>
						<td></td>
					</tr>
					<tr>
						<td>Composition.section.emptyReason</td>
						<td>Composition(Personal Health Summary).section(Allergies).emptyReason</td>
						<td></td>
					</tr>           
					<tr>
						<td rowspan="2">Agent Description</td>
						<td>AllergyIntolerance.code</td>
						<td>Composition(Personal Health Summary).section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.code</td>
						<td></td>
					</tr>
					<tr>
						<td>AllergyIntolerance.reaction.substance</td>
						<td>Composition(Personal Health Summary).section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.substance</td>
						<td></td>
					</tr>           
					<tr>
						<td>Reaction Description</td>
						<td>AllergyIntolerance.reaction.manifestation</td>
						<td>Composition(Personal Health Summary).section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.manifestation</td>
						<td></td>
					</tr>              
				   <tr>
						<td rowspan="7">Medicines</td>
						<td rowspan="3">Component</td>
						<td>Composition.section</td>
						<td>Composition(Personal Health Summary).section(Medications)</td>
						<td></td>
					</tr>
					<tr>
						<td>Composition.section.entry</td>
						<td>Composition(Personal Health Summary).section(Medications).entry</td>
						<td></td>
					</tr>
					<tr>
						<td>Composition.section.emptyReason</td>
						<td>Composition(Personal Health Summary).section(Medications).emptyReason</td>
						<td></td>
					</tr>                
					<tr>
						<td>Item Description</td>
						<td>MedicationStatement.medication[x]</td>
						<td>Composition(Personal Health Summary).section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.medication[x]</td>
						<td></td>
					</tr>                          
					<tr>
						<td>Dose Information</td>
						<td>MedicationStatement.dosage</td>
						<td>Composition(Personal Health Summary).section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.dosage</td>
						<td></td>
					</tr>                              
					<tr>
						<td>Reason for Medicine</td>
						<td>MedicationStatement.reasonCode</td>
						<td>Composition(Personal Health Summary).section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.reasonCode</td>
						<td></td>
					</tr>                              
					<tr>
						<td>Additional Comments</td>
						<td>MedicationStatement.note</td>
						<td>Composition(Personal Health Summary).section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.note</td>
						<td></td>
					</tr> 					
					<tr>
						<td rowspan="2">Document Control</td>					
						<td>Component</td>
						<td>n/a</td>
						<td>n/a</td>
						<td></td>
					</tr>
					<tr>
						<td>DateTime Input</td>	
						<td>n/a</td>
						<td>n/a</td>
						<td></td>
					</tr>
            </tbody>
        </table>
        
## Legend for mapping from requirements

A mappings from requirements table demonstrates the logical decomposition of each requirement to the lowest possible element in an applicable profile.

<table class="list" width="100%">
	<col style="width:20%"/>
	<col style="width:20%"/>
	<col style="width:20%"/>
	<col style="width:20%"/>
	<col style="width:20%"/>
            <thead>
                <tr>
                    <th>Data item</th>
                    <th>Req. No</th>
                    <th>Element name</th>
                    <th>Hierarchy</th>
                    <th>Additional notes</th>
                <td></td>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><p>The heading text of the requirement as taken from the requirements specification.</p></td>
                    <td><p>The requirement number as taken from the requirements specification.</p></td>
                    <td>
                        <p>Either the name of the lowest element in a profiled FHIR resource that addresses the requirement or 'N/A' where 
                        the requirement has been deemed not applicable to a FHIR profile.</p>
                       <p>If the lowest possible decomposition is to the resource then only the resource name (e.g. Patient) is present. 
                    If the lowest possible decomposition is to one or more child elements of a FHIR resource then a dot notation is 
                    used to indicate the hierarchical relationship.</p>
                       <p>For example Patient.communication.language indicates 
                    the requirement maps to the language element, that is a child of the communication element, 
                    in the Patient FHIR resource.</p>
                    </td>
                    <td>
                        <p>Either the full hierarchical path from the root FHIR resource (e.g. Composition) to the element 
                    the requirement is mapped to or 'N/A' where the requirement has been deemed not applicable to a FHIR profile.</p>
                        <p>A dot notation is used to demonstrate hierarchy within a FHIR resource.</p>
                        <p>An arrow '<span style="font-family:courier;">&#62;</span>' is used to denote the reference connecting one FHIR resource 
                    to another from the linking element. For example Composition.subject> Patient or Composition.author> Patient.</p>
                    <p>Where a requirement is addressed by multiple elements, the elements are presented in order of appearance in the profiled FHIR resource.</p>
                    </td>
                    <td>
                        <p>Additional notes are provided where a gap between a requirement, or parts of a requirement, and the 
                    profiles is identified. Where a requirement is fully addressed by the mapped elements then no entry in this 
                    column is expected.</p>
                    </td>
                </tr>
             </tbody>
</table>
