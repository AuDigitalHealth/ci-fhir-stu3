# {{ page.title }}
{% include publish-box.html %}
{:.no_toc}
<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->
* Do not remove this line (it will not be displayed)
{:toc}

## Introduction

The Shared Medicines List implementation guide is intended to support multiple usage scenarios; some profiles described within this implementation guide are reused across usage scenarios and other implementation guides.

This informative section provides a mapping from the requirements of each end-product clinical specification to elements in a profiled FHIR resource. At the time of publication of this implementation guide the only end-product clinical specification supported is Pharmacist Shared Medicines List (PSML).

The mapping from requirements table below demonstrates the logical decomposition of each requirement to the lowest possible element in an applicable profile. 

## Mapping from PSML business requirements

The table below provides mapping from the requirements in [Pharmacist Shared Medicines List scenarios and business requirements v2.0 [DH2019m]](index.html#DH2019m) to the corresponding supported element in the [Shared Medicines List Authored by Practitioner](StructureDefinition-composition-sml-prac-1.html) profile, or referenced profile (e.g. [Summary Statement of Allergy or Intolerance](StructureDefinition-allergyintolerance-summary-1.html)).

See the [legend](mappings.html#legend-for-mapping-from-requirements) for information on the columns used to present the mapping content.

 <table class="list" width="100%">
	<col style="width:20%"/>
	<col style="width:7%"/>
	<col style="width:20%"/>
	<col style="width:25%"/>
	<col style="width:28%"/>
            <thead>
                <tr>
                    <th>Requirement</th>
                    <th>Req. No</th>
                    <th>Element name</th>
                    <th>Hierarchy</th>
                    <th>Additional notes</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td rowspan="2">Pharmacist shared medicines list</td>
                    <td rowspan="2">027948</td>
                    <td>Composition</td>
                    <td>Composition</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.extension(composition-author-role)</td>
                    <td>Composition.extension(composition-author-role)</td>
                </tr>
                <tr>
                    <td rowspan="9">Components in the PSML document</td>
                    <td rowspan="9">028321</td>
                    <td>Composition</td>
                    <td>Composition</td>
                    <td rowspan="9">
                        <p>This requirement states that the PSML document will contain the organisation the pharmacist is representing at the
time of document authoring. The profile has this as optional.</p>
                        <p>The profile does not mandate a versioning mechanism (e.g. meta.versionId). Versioning is an implementation environment concern and outside of the scope of the FHIR profiles.</p>
                        <p>This requirement states if the PSML document contains the primary healthcare provider then the
name of the primary healthcare provider organisation is mandatory. The profile requires either a name or an identifier - it does not mandate name.</p>
                        <p>These parts of the requirement are best enforced in a conformance profile.</p>
                     </td>
                 </tr>
                 <tr>
                    <td>Composition.identifier</td>
                    <td>Composition.identifier</td>
                 </tr> 
                 <tr>
                    <td>Composition.date</td>
                     <td>Composition.date</td>
                 </tr> 
                 <tr>
                    <td>Composition.subject</td>
                     <td>Composition.subject</td>
                 </tr>
                 <tr>
                    <td>Composition.extension(composition-author-role)</td>
                     <td>Composition.extension(composition-author-role)</td>
                 </tr>  
                 <tr>
                    <td>PractitionerRole.organization</td>
                     <td>Composition.extension(composition-author-role)->PractitionerRole.organization</td>
                 </tr> 
                 <tr>
                    <td>Patient.generalPractitioner</td>
                     <td>Composition.subject->Patient.generalPractitioner</td>
                 </tr>  
                 <tr>
                    <td>Composition.section(allergies)</td>
                     <td>Composition.section(allergies)</td>
                 </tr>
                 <tr>
                    <td>Composition.section(medications)</td>
                     <td>Composition.section(medications)</td>
                 </tr>
                <tr>
                    <td>Document conformance levels</td>
                    <td>028315</td>
                     <td>N/A</td>
                     <td>N/A</td>
                     <td><p>This requirement is applicable only to a CDA implementation.</p></td>
                </tr>            
                <tr>
                    <td rowspan="2">Point-to-point transmission</td>
                    <td rowspan="2">027954</td>
                     <td>Composition</td>
                     <td>Composition</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                     <td>List</td>
                     <td>List</td>
                </tr>                        
                <tr>
                    <td>HPI-I relaxed template package</td>
                    <td>028394</td>
                     <td>N/A</td>
                     <td>N/A</td>
                     <td><p>This requirement is applicable only to a CDA implementation.</p></td>
                </tr>                                     
                 <tr>
                    <td rowspan="2">Compatible with Prescription and Dispense Record</td>
                    <td rowspan="2">028323</td>
                    <td>MedicationStatement</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement</td>
                     <td rowspan="2"><p></p></td>
                 </tr>   
                 <tr>
                    <td>Medication</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication</td>
                 </tr>                                             
                 <tr>
                    <td>Prompt to upload recent PSML</td>
                    <td>028325</td>
                     <td>N/A</td>
                     <td>N/A</td>
                     <td><p>This requirement is a producing system behavioural requirement.</p></td>
                </tr>                                                                          
                <tr>
                    <td rowspan="2">Medicines information presentation</td>
                    <td rowspan="2">028359</td>
                     <td>Composition.section(allergies)</td>
                     <td>Composition.section(allergies)</td>
                    <td rowspan="2"><p>This requirement includes a rendering requirement on sequence of information. This part of the requirement is a rendering requirement and not applicable for the profile.</p></td>
                </tr>
                <tr>
                     <td>Composition.section(medications)</td>
                     <td>Composition.section(medications)</td>
                </tr>
                <tr>
                    <td>Allergies and Adverse Reactions section</td>
                    <td>028355</td>
                     <td>Composition.section(allergies).text</td>
                     <td>Composition.section(allergies).text</td>
                    <td><p>This requirement includes a rendering requirement on sequence of information. This part of the requirement is a rendering requirement and not applicable for the profile.</p></td>
                </tr>
                <tr>
                    <td>Allergies and Adverse Reactions header</td>
                    <td>028360</td>
                     <td>Composition.section(allergies).text</td>
                     <td>Composition.section(allergies).text</td>
                    <td><p>This requirement includes a rendering requirement on sequence of information. This part of the requirement is a rendering requirement and not applicable for the profile.</p></td>
                </tr>                                
                <tr>
                    <td>No known allergies or adverse reactions</td>
                    <td>028411</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>
                        <p>This requirement includes a rendering requirement in the absence of recorded allergy information. This part of the requirement is a rendering requirement and not applicable for the profile.</p>
                        <p>Alternatively the profile caters for recording that a patient does not have an allergy or category of allergies in AllergyIntolerance.code.</p>
                    </td>
                </tr>
                 <tr>
                    <td>Current Medicines section</td>
                    <td>028361</td>
                    <td>Composition.section(medications).text</td>
                    <td>Composition.section(medications).text</td>
                    <td><p>This requirement includes a rendering requirement that is not applicable for the profile.</p></td>
                </tr> 
                 <tr>
                    <td>Current Medicines header</td>
                    <td>028362</td>
                    <td>Composition.section(medications).text</td>
                    <td>Composition.section(medications).text</td>
                    <td><p>This requirement includes a rendering requirement that is not applicable for the profile.</p></td>
                </tr>                             
                <tr>
                    <td>Ceased Medicines section</td>
                    <td>028363</td>
                    <td>Composition.section(medications).text</td>
                    <td>Composition.section(medications).text</td>
                    <td><p>This requirement includes a rendering requirement on sequence of information. This part of the requirement is a rendering requirement and not applicable for the profile.</p></td>
                </tr>
                 <tr>
                    <td>Ceased Medicines header</td>
                    <td>028364</td>
                    <td>Composition.section(medications).text</td>
                    <td>Composition.section(medications).text</td>
                    <td><p>This requirement includes a rendering requirement that is not applicable for the profile.</p></td>
               </tr>
               <tr>
                    <td rowspan="2">Suppressing Ceased Medicines section</td>
                    <td rowspan="2">028358</td>
                    <td>Composition.section(medications)</td>
                    <td>Composition.section(medications)</td>
                    <td rowspan="2">
                        <p>This requirement states a ceased medicines section with no recorded ceased medicines will not be rendered.</p>
                        <p>The profiles do not allow for an empty ceased medicines list (or section) - at least one medicine item is mandatory.</p>
                     </td>
                </tr>
                <tr>
                    <td>List.entry.item</td>
                    <td>Composition.section(medications).entry->List.entry.item</td>
                </tr>
               <tr>
                    <td>Suppressing codes and medicine identifiers</td>
                    <td>028625</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>
                        <p>This requirement is a system behavioural requirement.</p>
                        <p>This requirement is satisifed by typical producing and consuming system behaviour. Only a display or text associated with a code is expected to be included in the narrative and rendered.</p>
                    </td>
                </tr>               
               <tr>
                    <td>Completeness of PSML document</td>
                    <td>028324</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>
                        <p>This requirement is a producing system behavioural requirement.</p>
                    </td>
                </tr>                                                                                                         
                <tr>
                    <td rowspan="3">Identifier for document author</td>
                    <td rowspan="3">028317</td>
                    <td>Composition.author.identifier</td>
                    <td>Composition.author.identifier</td>
                    <td rowspan="3"><p></p></td>
                </tr>
                <tr>
                    <td rowspan="2">Practitioner.identifier</td>
                    <td>Composition.author->Practitioner.identifier</td>
                </tr>
                <tr>
                    <td>Composition.extension(composition-author-role)->PractitionerRole.practitioner->Practitioner.identifier</td>
                </tr>
                <tr>
                    <td rowspan="5">No Address for the consumer</td>
                    <td rowspan="5">028319</td>
                    <td rowspan="5">Patient.address</td>
                    <td>Composition.subject->Patient.address</td>
                    <td rowspan="5">
                        <p>This requirement states a PSML document, when uploaded to the My Health Record, will not contain any address for the consumer within the document. Patient profiles in this implementation guide allow the optional inclusion of address to support point-to-point transmission. Implementation guidance is included on the profile page to direct implementers to not send address when sending to the My Health Record.</p>
                        <p>This requirement is best enforced in a conformance profile.</p>
                     </td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.address</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.address</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.address</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.address</td>
                </tr>
                <tr>
                    <td rowspan="5">No Electronic Communication Detail for the consumer</td>
                    <td rowspan="5">028320</td>
                    <td rowspan="5">Patient.telecom</td>
                    <td>Composition.subject->Patient.telecom</td>
                    <td rowspan="5">
                        <p>This requirement states a PSML document, when uploaded to the My Health Record, will not contain any types of electronic communication contact detail for the consumer within the document. Patient profiles in this implementation guide allow the optional inclusion of telecom to support point-to-point transmission. Implementation guidance is included on the profile page to direct implementers to not send telecom when sending to the My Health Record.</p>
                        <p>This requirement is best enforced in a conformance profile.</p>
                     </td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.telecom</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.telecom</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.telecom</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.telecom</td>
                </tr>
                <tr>
                    <td rowspan="3">Attribute for Healthcare Setting</td>
                    <td rowspan="3">028349</td>
                    <td>PractitionerRole.code</td>
                    <td>Composition.extension(composition-author-role)->PractitionerRole.code</td>
                    <td rowspan="3">
                        <p>This requirement states the PSML document will include the healthcare setting in which the
PSML document was authored. The profiles allow for an authoring role or organisation type (e.g. "Community Pharmacy" or "Hospital Pharmacy") and an encounter type (e.g. "Home Medicines Review) - they do not mandate any of these elements.</p>
                        <p>These parts of the requirement are best enforced in a conformance profile.</p>
                    </td>
                </tr>
                <tr>
                    <td>Organization.type</td>
                    <td>Composition.extension(composition-author-role)->PractitionerRole.organization->Organization.type</td>
                </tr>
                <tr>
                    <td>Encounter.type</td>
                    <td>Composition.encounter->Encounter.type</td>
                </tr>
                <tr>
                    <td>Attribute for Dose Administration Aid medicines present</td>
                    <td>028413</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>
                        <p>Not directly supported in FHIR.</p>
                        <p>This requirement states the PSML document may include a statement or an indicator that a medicines list includes medicine items packed in a dose administration aid (DAA).</p>
                        <p>A request has been submitted to HL7 AU to consider this requirement on the national level,see <a href="https://github.com/hl7au/au-fhir-base/issues/320">https://github.com/hl7au/au-fhir-base/issues/320</a>.</p>
                        <p>See <a href="index.html">Known issues</a> for further information on this issue and possible work arounds.</p>
                    </td>
                </tr>
                <tr>
                    <td rowspan="2">Additional Comment</td>
                    <td rowspan="2">028348</td>
                    <td>Composition.section(medications).text</td>
                    <td>Composition.section(medications).text</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>List.note</td>
                    <td>Composition.section(medications).entry->List.note</td>
                </tr>
                <tr>
                    <td>Attribute for Ceased Date</td>
                    <td>028352</td>
                    <td>MedicationStatement.effective[x]</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.effective[x]</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td rowspan="2">Attribute for Substance/ Agent of allergy and adverse
                        reaction</td>
                    <td rowspan="2">028330</td>
                    <td>AllergyIntolerance.code</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.code</td>
                    <td rowspan="2"><p></p></td>
               </tr>
               <tr>
                    <td>AllergyIntolerance.reaction.substance</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.reaction.substance</td>
                </tr>    
                <tr>
                    <td>Attribute for Reaction Type</td>
                    <td>028331</td>
                    <td>AllergyIntolerance.type</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.type</td>
                    <td><p>This requirement as stated is satisifed however it is noted that the concept of 'reaction type' is not supported - <span style="padding-left: 3px; padding-right: 3px; color: white; background-color: red">TBD</span> - SOMEONE GET ME A DEF OF REACTION TYPE AND WHY ITS NOT THIS</p></td>
                </tr>
                <tr>
                    <td>Attribute for Reaction</td>
                    <td>028332</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.reaction.manifestation</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Attribute for Reaction Onset Date</td>
                    <td>028410</td>
                    <td>AllergyIntolerance.onsetDateTime</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.onsetDateTime</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Attribute for Medicine Identifier</td>
                    <td>028329</td>
                    <td>Medication.code</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td rowspan="2">Attribute for Active Ingredient</td>
                    <td rowspan="2">028333</td>
                    <td>Medication.code</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                 <tr>
                    <td>Medication.ingredient.item[x]</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.ingredient.item[x]</td>
                </tr>
                <tr>
                    <td>No Latin words or abbreviations of Active Ingredient</td>
                    <td>028390</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td><p>This requirement is a producing system behavioural requirement.</p></td>
                </tr>
                <tr>
                    <td rowspan="2">Attribute for Brand Name</td>
                    <td rowspan="2">028335</td>
                    <td>Medication.code</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                    <td rowspan="2"><p></p></td>
                </tr>
               <tr>
                    <td>Medication.extension(medication-brand-name)</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.extension(medication-brand-name)</td>
                </tr>
                <tr>
                    <td rowspan="3">Active Ingredient or Brand Name</td>
                    <td rowspan="3">028412</td>
                     <td>Medication.code</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                    <td rowspan="3">
                        <p>This requirement states each medicine item will have either the
active ingredient(s) or a brand name, or both.</p>
                        <p>The profile allows a brand name and active ingredient(s) - it does not mandate the presence of either.</p>
                        <p>These parts of the requirement are best enforced in a conformance profile.</p>
                        </td>
                </tr>
                <tr>
                    <td>Medication.extension(medication-brand-name)</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.extension(medication-brand-name)</td>
                </tr>
                <tr>
                    <td>Medication.ingredient.item[x]</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.ingredient.item[x]</td>
                </tr>
                <tr>
                    <td rowspan="2">Attribute for Strength</td>
                    <td rowspan="2">028392</td>
                    <td>Medication.code</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>Medication.ingredient.amount</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.ingredient.amount</td>
                </tr>
                <tr>
                    <td rowspan="2">Attribute for Dose Form</td>
                    <td rowspan="2">028391</td>
                    <td>Medication.code</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>Medication.form</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.form</td>
                </tr>
                <tr>
                    <td rowspan="3">Attribute for Route</td>
                    <td rowspan="3">028399</td>
                    <td>MedicationStatement.dosage.text</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage.text</td>
                    <td rowspan="3"><p></p></td>
                </tr>
                <tr>
                    <td>MedicationStatement.dosage.patientInstruction</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage.patientInstruction</td>
                </tr>
                <tr>
                    <td>MedicationStatement.dosage.route</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage.route</td>
                </tr>
                <tr>
                    <td>Attribute for Direction</td>
                    <td>028336</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>No Latin words or abbreviations for Direction</td>
                    <td>028337</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td><p>This requirement is a producing system behavioural requirement.</p></td>
                 </tr>
                <tr>
                    <td>Attribute for Medicine Purpose</td>
                    <td>028338</td>
                    <td>MedicationStatement.reasonCode</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.reasonCode</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Terminology for Medicine Purpose</td>
                    <td>028339</td>
                    <td>MedicationStatement.reasonCode</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.reasonCode</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Attribute for Expected End Date</td>
                    <td>028343</td>
                    <td>MedicationStatement.effectivePeriod</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.effectivePeriod</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td rowspan="2">Attribute for Special Instruction</td>
                    <td rowspan="2">028345</td>
                    <td>MedicationStatement.note</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.note</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage</td>
                </tr>
                <tr>
                    <td>Attribute for Medicine Image</td>
                    <td>028346</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>
                        <p>Support for medicine image attribute has been removed from the Medication resource in the first normative release of FHIR (R4). For this
                            reason the use of medication image is strongly discouraged in the HL7 AU content based on a prior FHIR release (STU3) and unsupported by this
                            implementation guide.</p>
                        <p>One possible way a sending system can include a medicine image is to include the image in the section text element or List text element.</p>
                    </td>
                </tr>
                <tr>
                    <td>Image sizes</td>
                    <td>028406</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td><p>This requirement is a producing system behavioural requirement.</p></td>
                </tr>    
                <tr>
                    <td>Attribute for Physical Descriptions</td>
                    <td>028347</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>
                        <p>Not directly supported in FHIR.</p>
                        <p>One possible way a sending system can include a physical description of the medicine item is to include such description in the section text element or Medication text element.</p>
                    </td>
                </tr>
                <tr>
                    <td>Attribute for reason for ceasing medicine</td>
                    <td>028351</td>
                    <td>List.entry.extension(change-description)</td>
                    <td>Composition.section(medications).entry->List.entry.extension(change-description)</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td rowspan="2">Attribute for Medicine Status</td>
                    <td rowspan="2">028342</td>
                    <td>List.entry.extension(change-description)</td>
                    <td>Composition.section(medications).entry->List.entry.extension(change-description)</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>List.entry.flag</td>
                    <td>Composition.section(medications).entry->List.entry.flag</td>
                </tr>
                <tr>
                    <td>Withheld Medicine</td>
                    <td>028620</td>
                    <td>List.entry.extension(change-description)</td>
                    <td>Composition.section(medications).entry->List.entry.extension(change-description)</td>
                    <td><p></p></td>
                </tr> 
                <tr>
                    <td>Withheld Medicine Ordering</td>
                    <td>028626</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>
                        <p>This requirement is a system behavioural requirement.</p>
                    </td>
                </tr>
                <tr>
                    <td>Ceased medicines</td>
                    <td>028623</td>
                    <td>MedicationStatement</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement</td>
                    <td>
                        <p>This requirement states a ceased medicine item has the same atomic data requirements (as a current medicine item) but different rendering requirements limiting the displayed information to medicine item description, reason for ceasing, and date of ceasing.</p> 
                        <p>These parts of the requirement are producing system behavioural requirements.</p>
                    </td>
                  </tr>                                                 
             </tbody>
        </table>

            
## Mapping from PSML information requirements
This informative section provides mapping from the data items (i.e. requirements) in [Pharmacist Shared Medicines List Information Requirements v2.0 [DH2019n]](index.html#DH2019n).

The table below matches the data items to the corresponding supported element in the [Shared Medicines List Authored by Practitioner profile](StructureDefinition-composition-sml-prac-1.html) profile, or referenced profile (e.g. [Summary Statement of Allergy or Intolerance](StructureDefinition-allergyintolerance-summary-1.html)). The hierarchy column demonstrates the path to that supported element from the root Composition. 

See the [legend](mappings.html#legend-for-mapping-from-requirements) for information on the columns used to present the mapping content.

 <table class="list" width="100%">
	<col style="width:20%"/>
	<col style="width:7%"/>
	<col style="width:20%"/>
	<col style="width:25%"/>
	<col style="width:28%"/>
            <thead>
                <tr>
                    <th>Requirement</th>
                    <th>Req. No</th>
                    <th>Element name</th>
                    <th>Hierarchy</th>
                    <th>Additional notes</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td rowspan="5">Individual's address (optional)</td>
                    <td rowspan="5">028640</td>
                    <td rowspan="5">Patient.address</td>
                    <td>Composition.subject->Patient.address</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.address</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.address</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.address</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.address</td>
                </tr>
                <tr>
                    <td rowspan="5">Individual's electronic communication details (optional)</td>
                    <td rowspan="5">024042</td>
                    <td rowspan="5">Patient.telecom</td>
                    <td>Composition.subject->Patient.telecom</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.telecom</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.telecom</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.telecom</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.telecom</td>
                </tr>
                <tr>
                    <td rowspan="5">Individual (subject of care)</td>
                    <td rowspan="5">027984</td>
                    <td rowspan="5">Patient</td>
                    <td>Composition.subject->Patient</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient</td>
                </tr>                
                <tr>
                    <td rowspan="5">Individual Healthcare Identifier (mandatory)</td>
                    <td rowspan="5">022082</td>
                    <td rowspan="5">Patient.identifier</td>
                    <td>Composition.subject->Patient.identifier</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.identifier</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.identifier</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.identifier</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.identifier</td>
                </tr>                
                <tr>
                    <td rowspan="5">Individual's title (optional)</td>
                    <td rowspan="5">022081</td>
                    <td rowspan="5">Patient.name</td>
                    <td>Composition.subject->Patient.name</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.name</td>
                </tr>          
                <tr>
                    <td rowspan="5">Individual's given name (optional)</td>
                    <td rowspan="5">023056</td>
                    <td rowspan="5">Patient.name</td>
                    <td>Composition.subject->Patient.name</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.name</td>
                </tr>
                <tr>
                    <td rowspan="5">Individual's family name (optional)</td>
                    <td rowspan="5">023058</td>
                    <td rowspan="5">Patient.name</td>
                    <td>Composition.subject->Patient.name</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.name</td>
                </tr>
                <tr>
                    <td rowspan="5">Individual's name suffix (optional)</td>
                    <td rowspan="5">023059</td>
                    <td rowspan="5">Patient.name</td>
                    <td>Composition.subject->Patient.name</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.name</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.name</td>
                </tr>        
                <tr>
                    <td rowspan="5">Individual's gender (mandatory)</td>
                    <td rowspan="5">027983</td>
                    <td rowspan="5">Patient.gender</td>
                    <td>Composition.subject->Patient.gender</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.gender</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.gender</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.gender</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.gender</td>
                </tr>
                <tr>
                    <td>Individual's sex (optional)</td>
                    <td>028570</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>
                        <p>The information requirements specification includes an optional requirement for recording individual’s biological sex, interpreted as sex at birth. This implementation guide only supports including a patient’s gender as part of a patient’s demographics for identification purposes in line with the Australian Government recommendations. <a href="https://www.ag.gov.au/Publications/Pages/AustralianGovernmentGuidelinesontheRecognitionofSexandGender.aspx">Australian Government Guidelines on the Recognition of Sex and Gender</a> state that patient’s biological sex should only be collected when clinically relevant.</p>
                        <p>Biological sex is not directly supported in FHIR; work is underway via HL7 AU to define a nationally agreed model for representing biological sex at birth, see <a href="https://github.com/hl7au/au-fhir-base/issues/321">https://github.com/hl7au/au-fhir-base/issues/321</a>.</p>
                    </td>
                </tr>
                <tr>
                    <td rowspan="5">Individual's date of birth (mandatory)</td>
                    <td rowspan="5">023060</td>
                    <td rowspan="5">Patient.birthDate</td>
                    <td>Composition.subject->Patient.birthDate</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.birthDate</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.birthDate</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.birthDate</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.birthDate</td>
                </tr>
                <tr>
                    <td rowspan="2">Date of birth accuracy indicator (optional)</td>
                    <td>024026</td>
                    <td rowspan="2">Patient.birthDate.extension(date-accuracy-indicator)</td>
                    <td rowspan="2">Composition.subject->Patient.extension(date-accuracy-indicator)</td>
                    <td rowspan="2"><p><span style="padding-left: 3px; padding-right: 3px; color: white; background-color: red">TBD</span></p></td>
                </tr>  
                <tr>
                    <td>027005</td>
                </tr>
                <tr>
                    <td rowspan="5">Indigenous status (mandatory)</td>
                    <td rowspan="5">024033</td>
                    <td rowspan="5">Patient.extension(indigenous-status)</td>
                    <td>Composition.subject->Patient.extension(indigenous-status)</td>
                    <td rowspan="5"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.encounter->Encounter.subject->Patient.extension(indigenous-status)</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.patient->Patient.extension(indigenous-status)</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.subject->Patient.extension(indigenous-status)</td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.subject->Patient.extension(indigenous-status)</td>
                </tr>
                <tr>
                    <td rowspan="3">Document author (mandatory)</td>
                    <td rowspan="3">027985</td>
                    <td>PractitionerRole</td>
                    <td>Composition.extension(composition-author-role)->PractitionerRole</td>
                    <td rowspan="3"><p></p></td>
                </tr>
                <tr>
                    <td>Practitioner</td>
                    <td>Composition.author->Practitioner</td>
                </tr>
                <tr>
                    <td>List.source</td>
                    <td>Composition.section(medications).entry->List.source</td>
                </tr>
                <tr>
                    <td>Healthcare provider organisation name (mandatory)</td>
                    <td>023070</td>
                    <td>Organization.name</td>
                    <td>Composition.extension(composition-author-role)->PractitionerRole.organization->Organization.name</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td rowspan="2">Healthcare provider individual's workplace address (mandatory)</td>
                    <td rowspan="2">024891</td>
                    <td rowspan="2">Practitioner.address</td>
                    <td>Composition.author->Practitioner.address</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.source->Practitioner.address</td>
                </tr>
                <tr>
                    <td rowspan="4">Healthcare provider individual's workplace electronic communication details (optional)</td>
                    <td rowspan="4">024036</td>
                    <td>PractitionerRole.telecom</td>
                    <td>Composition.extension(composition-author-role)->PractitionerRole.telecom</td>
                    <td rowspan="4"><p></p></td>
                </tr>
                <tr>
                    <td>Practitioner.telecom</td>
                    <td>Composition.author->Practitioner.telecom</td>
                </tr>
                <tr>
                    <td>PractitionerRole.telecom</td>
                    <td>Composition.section(medications).entry->List.extension(author-role)->PractitionerRole.telecom</td>
                </tr>
                <tr>
                    <td>Practitioner.telecom</td>
                    <td>Composition.section(medications).entry->List.source->Practitioner.telecom</td>
                </tr>
                <tr>
                    <td rowspan="2">Healthcare provider professional role (mandatory)</td>
                    <td rowspan="2">024040</td>
                    <td rowspan="2">PractitionerRole.code</td>
                    <td>Composition.extension(composition-author-role)->PractitionerRole.code</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry->List.extension(author-role)->PractitionerRole.code</td>
                </tr>
                <!-- ========================== UP TO HERE ========================== -->
                <tr>
                    <td>Healthcare Provider Identifier-Individual (optional)</td>
                    <td>024601</td>
                    <td>Practitioner.identifier</td>
                    <td>Composition.author->Practitioner.identifier</td>
                    <td><p></p></td>
                </tr>
                <!-- ========================== UP TO HERE ========================== -->
                <tr>
                    <td>Healthcare Provider Identifier-Organisation (optional)</td>
                    <td>024602</td>
                    <td>Organization.identifier</td>
                    <td>Composition.extension(composition-author-role)->PractitionerRole.organization->Organization.identifier</td>
                    <td><p></p></td>
                </tr>                   
                <tr>
                    <td>Healthcare provider's title (optional)</td>
                    <td>023061</td>
                    <td>Practitioner.name</td>
                    <td>Composition.author->Practitioner.name</td>
                    <td><p></p></td>
                </tr> 
                <tr>
                    <td>Healthcare provider given name (optional)</td>
                    <td>023062</td>
                    <td>Practitioner.name</td>
                    <td>Composition.author->Practitioner.name</td> 
                </tr>   
                <tr>
                    <td>Healthcare provider family name (mandatory)</td>
                    <td>023064</td>
                    <td>Practitioner.name</td>
                    <td>Composition.author->Practitioner.name</td>
                    <td><p></p></td>
                </tr> 
                <tr>
                    <td>Healthcare provider name suffix (optional)</td>
                    <td>023065</td>
                    <td>Practitioner.name</td>
                    <td>Composition.author->Practitioner.name</td>  
               </tr> 
                <tr>
                    <td>Primary healthcare provider (optional)</td>
                    <td>028028</td>
                    <td>Patient.generalPractitioner</td>
                    <td>Composition.subject->Patient.generalPractitioner</td>
                    <td><p></p></td>
                </tr> 
                <tr>
                    <td>Healthcare Provider Identifier-Individual (optional)</td>
                    <td>024601</td>
                    <td>Practitioner.identifier</td>
                    <td>Composition.subject->Patient.generalPractitioner->Practitioner.identifier</td>
                    <td><p></p></td>
                </tr> 
                <tr>
                    <td>Healthcare Provider Identifier-Organisation (optional)</td>
                    <td>024602</td>
                    <td>Organization.identifier</td>
                    <td>Composition.subject->Patient.generalPractitioner->Organization.identifier</td>
                    <td><p></p></td>
                </tr> 
               <tr>
                    <td>Healthcare provider's title (optional)</td>
                    <td>023061</td>
                    <td>Practitioner.name</td>
                    <td>Composition.subject->Patient.generalPractitioner->Practitioner.name</td>
                    <td><p></p></td>
                </tr> 
                 <tr>
                    <td>Healthcare provider given name (optional)</td>
                    <td>023062</td>
                    <td>Practitioner.name</td>
                    <td>Composition.subject->Patient.generalPractitioner->Practitioner.name</td>
                    <td><p></p></td>
                </tr> 
                <tr>
                    <td>Healthcare provider family name (optional)</td>
                    <td>028638</td>
                    <td>Practitioner.name</td>
                    <td>Composition.subject->Patient.generalPractitioner->Practitioner.name</td>
                    <td><p></p></td>
                </tr> 
                 <tr>
                    <td>Healthcare provider name suffix (optional)</td>
                    <td>023065</td>
                    <td>Practitioner.name</td>
                    <td>Composition.subject->Patient.generalPractitioner->Practitioner.name</td>
                    <td><p></p></td>
                </tr>      
                 <tr>
                    <td>Healthcare provider organisation name (mandatory)</td>
                    <td>023070</td>
                    <td>Organization.name</td>
                    <td>Composition.subject->Patient.generalPractitioner->Organization.name</td>
                    <td><p></p></td>
                </tr>  
                 <tr>
                    <td>Healthcare provider individual's workplace address (optional)</td>
                    <td>024035</td>
                    <td>Practitioner.address</td>
                    <td>Composition.subject->Patient.generalPractitioner->Practitioner.address</td>
                    <td><p></p></td>
                </tr>  
                <tr>
                    <td>Healthcare provider individual's workplace electronic communication details (optional)</td>
                    <td>024036</td>
                    <td>Practitioner.telecom</td>
                    <td>Composition.subject->Patient.generalPractitioner->Practitioner.telecom</td>
                    <td><p></p></td>
                </tr>  
                <tr>
                    <td>Healthcare provider professional role (mandatory)</td>
                    <td>024040</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>This requirement is not directly supported by a FHIR profile; it is supported in CDA. Where a sending system can state patient's generalPractitioner healthcare provider professional role, the role is expected to be sent in narrative or as local extension.</td>
                </tr>  
                <tr>
                    <td rowspan="2">Healthcare setting (mandatory)</td>
                    <td>028435</td>
                    <td rowspan="2">Encounter.type</td>
                    <td rowspan="2">Composition.encounter->Encounter.type</td>
                    <td rowspan="2"><p></p></td>
                </tr>  
                <tr>
                   <td>028534</td>
                </tr>  
                <tr>
                    <td>Additional comments (optional)</td>
                    <td>028403</td>
                    <td>List.note</td>
                    <td>Composition.section(medications).entry->List.note </td>
                    <td><p></p></td>
                </tr>  
                <tr>
                    <td>Dose Administration Aid medicines present (mandatory)</td>
                    <td>028441</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>
                        <p>Not directly supported in FHIR.</p>
                        <p>The requirements specification mandates the inclusion of a statement or an indicator that a medicines list document includes medicine items packed in a dose administration aid (DAA). A request has been submitted to HL7 AU to consider this requirement on the national level, see <a href="https://github.com/hl7au/au-fhir-base/issues/320">https://github.com/hl7au/au-fhir-base/issues/320</a>.</p>
                        <p>See <a href="index.html">Known issues</a> for further information on this issue and possible work arounds.</p>
                    </td>
                </tr>  
                <tr>
                    <td rowspan="4">Allergy and Adverse Reaction (optional)</td>
                    <td rowspan="2">028631</td>
                    <td>Composition.section(Allergies)</td>
                    <td>Composition.section(Allergies)</td>
                </tr>
                <tr>
                    <td>Composition.section(allergies).entry</td>
                    <td>Composition.section(allergies).entry</td>
                </tr>
                <tr>
                    <td rowspan="2">028673</td>
                    <td>Composition.section(allergies).emptyReason</td>
                    <td>Composition.section(allergies).emptyReason</td>
                </tr>
                <tr>
                    <td>AllergyIntolerance.code</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.code</td>
                </tr>
               <tr>
                    <td rowspan="2">Substance/Agent (optional)</td>
                    <td rowspan="2">028436</td>
                    <td>AllergyIntolerance.reaction.substance</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.reaction.substance</td>
                    <td rowspan="2"><p></p></td>
               </tr>
               <tr>
                    <td>AllergyIntolerance.code</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.code</td>
                </tr>    
                <tr>
                    <td>Reaction type (optional)</td>
                    <td>028437</td>
                    <td>AllergyIntolerance.type</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.type</td>
                    <td><p></p></td>
                </tr>  
                <tr>
                    <td>Reaction (optional)</td>
                    <td>028438</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.reaction.manifestation</td>
                    <td><p></p></td>
                </tr>  
                <tr>
                    <td>Reaction Onset Date (optional)</td>
                    <td>028439</td>
                    <td>AllergyIntolerance.onset</td>
                    <td>Composition.section(allergies).entry->AllergyIntolerance.onset</td>
                    <td><p></p></td>
                </tr>  
               <tr>
                    <td rowspan="2">Medicine Item (mandatory)</td>
                    <td rowspan="2">028632</td>
                    <td>Composition.section(medications)</td>
                    <td>Composition.section(medications)</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry</td>
                    <td>Composition.section(medications).entry</td>
                </tr>    
                <tr>
                    <td rowspan="2">Medicine identifier (mandatory)</td>
                    <td>028633</td>
                    <td rowspan="2">Medication.code</td>
                    <td rowspan="2">Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>028634</td>
               </tr>
                <tr>
                    <td rowspan="2">Active Ingredient (optional)</td>
                    <td rowspan="2">028014</td>
                    <td>Medication.ingredient</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.ingredient</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                 <tr>
                    <td>Medication.code</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                </tr>
                <tr>
                    <td rowspan="2">Brand name (optional)</td>
                    <td rowspan="2">028442</td>
                    <td>Medication.code</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                    <td rowspan="2"><p></p></td>
                </tr>
               <tr>
                    <td>medicationReference->Medication-brand-name</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.extension(medication-brand-name)</td>
                </tr>
                <tr>
                    <td rowspan="2">Medicine strength (optional)</td>
                    <td rowspan="2">028635</td>
                    <td>Medication.ingredient.amount</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.ingredient.amount</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>Medication.code</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                </tr>
                <tr>
                    <td rowspan="2">Dose form (optional)</td>
                    <td rowspan="2">028026</td>
                    <td>Medication.form</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.form</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>          
                    <td>Medication.code</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                </tr>
                <tr>
                    <td>Route (optional)</td>
                    <td>028443</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Direction (mandatory)</td>
                    <td>028021</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Dose per administration (optional)</td>
                    <td>028670</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Frequency of administration (optional)</td>
                    <td>028668</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Timing of dministration (optional)</td>
                    <td>028669</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Medicine purpose (optional)</td>
                    <td>028016</td>
                    <td>MedicationStatement.reasonCode</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.reasonCode</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Expected end date (optional)</td>
                    <td>028445</td>
                    <td>MedicationStatement.effective[x]</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.effective[x]</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td>Special instructions (optional)</td>
                    <td>028446</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.dosage</td>
                    <td><p></p></td>
                </tr>
                <tr>
                    <td rowspan="2">Medicine image (optional)</td>
                    <td>028018</td>
                    <td>N/A</td>
                    <td>
                        <p>Support for medicine image attribute has been removed from the Medication model in the first normative release of FHIR (R4). For this
                            reason the use of medication image is strongly discouraged in the HL7 AU content based on a prior FHIR release (STU3) and unsupported by this
                            implementation guide.</p>
                        <p>Where a sending system can include a medicine image, it is expected to be sent in the Medicines List section narrative or List narrative.</p>
                    </td>  
                </tr>               
                <tr>
                    <td>028535</td>
                    <td>N/A</td>
                    <td>This requirement is not directly managed by a FHIR profile; it may be enforced in a rendering specification, conformance profile or handled by implementation.</td>
                </tr>  
                <tr>
                    <td>Physical description (optional)</td>
                    <td>028020</td>
                    <td>N/A</td>
                    <td>This requirement is not directly supported by a FHIR profile. Where a sending system can include physical description of a medicine, it is expected to be sent in the Medicines List section narrative or List narrative.</td>
                </tr>  
                <tr>
                    <td rowspan="3">Medicine status (optional)</td>
                    <td>028017</td>
                    <td rowspan="2">List.entry.flag</td>
                    <td rowspan="2">Composition.section(medications).entry->List.entry.flag</td>
                    <td rowspan="2"><p></p></td>
                </tr>  
                <tr>
                    <td>028027</td>
               </tr>  
                <tr>
                    <td>028636</td>
                    <td>N/A</td>
                    <td>This requirement is not directly managed by a FHIR profile; it may be enforced in a conformance profile or handled by an implementation.</td>
                </tr>
                <tr>
                    <td rowspan="2">Ceased medicine (optional)</td>
                    <td rowspan="2">028674</td>
                    <td>Composition.section(medications)</td>
                    <td>Composition.section(medications)</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>Composition.section(medications).entry</td>
                    <td>Composition.section(medications).entry</td>
                </tr> 
                <tr>
                    <td rowspan="2">Medicine identifier (mandatory)</td>
                    <td>028633</td>
                    <td rowspan="2">Medication.code</td>
                    <td rowspan="2">Composition.section(medications).entry->List.entry.item->MedicationStatement.medicationReference->Medication.code</td>
                    <td rowspan="2"><p></p></td>
                </tr>
                <tr>
                    <td>028634</td>
                </tr>  
                <tr>
                    <td>Reason for ceasing medicine (optional)</td>
                    <td>028447</td>
                    <td>List.entry.change-description</td>
                    <td>Composition.section(medications).entry->List.entry.extension(change-description)</td>
                    <td><p></p></td>
                </tr>  
                <tr>
                    <td>Ceased date (optional)</td>
                    <td>028629</td>
                    <td>MedicationStatement.effective[x]</td>
                    <td>Composition.section(medications).entry->List.entry.item->MedicationStatement.effective[x]</td>
                    <td><p></p></td>
                </tr>  
                <tr>
                    <td>Ceased medicines (mandatory)</td>
                    <td>028636</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>This requirement is not directly managed by a FHIR profile; it may be enforced in a conformance profile or handled by an implementation.</td>
                </tr>  
                <tr>
                    <td>Extensions not permitted (mandatory)</td>
                    <td>028637</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>This requirement is not directly managed by a FHIR profile; it may be enforced in a rendering specification, conformance profile or handled by an implementation.</td>
                </tr>  
                <tr>
                    <td>Document version number (mandatory)</td>
                    <td>023068</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>This is managed in the implementation (e.g. FHIR Bundle, CDA)</td>
                </tr>  
                <tr>
                    <td>Document instance identifier (mandatory)</td>
                    <td>023067</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>This is managed in the implementation (e.g. FHIR Bundle, CDA)</td>
                </tr> 
                <tr>
                    <td>Date and time of document creation (mandatory)</td>
                    <td>024025</td>
                    <td>N/A</td>
                    <td>N/A</td>
                    <td>This is managed in the implementation (e.g. FHIR Bundle, CDA)</td>
                 </tr> 
                <tr>
                    <td>Document type (mandatory)</td>
                    <td>024027</td>
                    <td>Composition.type</td>
                    <td>Composition.type</td>
                    <td><p></p></td>
                </tr> 
                <tr>
                    <td rowspan="2">Document sub-type (mandatory)</td>
                    <td>028671</td>
                    <td rowspan="2">Composition.type | Composition.composition-author-role</td>
                    <td rowspan="2">Composition.type | Composition.composition-author-role</td>
                    <td rowspan="2"><p></p></td>
                </tr> 
                <tr>
                    <td>028672</td>
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
                    <th>Requirement</th>
                    <th>Req. No</th>
                    <th>Element name</th>
                    <th>Hierarchy</th>
                    <th>Additional notes</th>
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
                    <p>Where a requirement is addressed by multiple elements, the elements are presented in order of appearance in the profiled FHIR resource.</p>
                    </td>
                    <td>
                        <p>Either the full hierarchical path from the root FHIR resource (e.g. Composition) to the element 
                    the requirement is mapped to or 'N/A' where the requirement has been deemed not applicable to a FHIR profile.</p>
                        <p>A dot notation is used to demonstrate hierarchy within a FHIR resource. 
                    An arrow '<span style="font-family:courier;">-&#62;</span>' is used to denote the reference connecting one FHIR resource 
                    to another from the linking element (e.g. Composition.subject->Patient or Composition.author->Patient).</p></td>
                    <td><p>Additional notes are provided where a gap between a requirement, or parts of a requirement, and the 
                    profiles is identified. Where a requirement is fully addressed by the mapped elements then no entry in this 
                    column is expected.</p></td>
                </tr>
             </tbody>
</table>