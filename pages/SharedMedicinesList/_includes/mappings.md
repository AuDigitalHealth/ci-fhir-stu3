# {{ page.title }}

This informative section provides mapping from the data items (i.e. requirements) in [Pharmacist Shared Medicines List scenarios and business requirements v2.0 d005]() [DH2019xx].

The table below matches the data items to the corresponding supported element in the {{site.data.fhir.igName}} profile, or referenced profile (e.g. Summary Statement of Allergy or Intolerance). The hierarchy column demonstrates the path to that supported element from the root Composition. 


 <table class="list" width="100%">
            <thead>
                <tr>
                    <th>Data Item</th>
                    <th>Req. No</th>
                    <th>Element</th>
                    <th>Hierarchy</th>
                </tr>
            </thead>
            <tfoot>
                <tr>
                    <td></td>
                    <td></td>
                    <td>Supported element</td>
                    <td>The path to the supported element from the root Composition</td>
                </tr>
            </tfoot>
            <tbody>
                <tr>
                    <td>Completeness of PSML document</td>
                    <td>028324</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">Identifier for document author</td>
                    <td rowspan="2">028317</td>
                    <td rowspan="2">Practitioner.identifier</td>
                    <td>Composition.composition-author-role.PractitionerRole.practitioner(Practitioner
                        as Practitioner with Mandatory Identifier).Practitioner.identifier</td>
                </tr>
                <tr>
                    <td>Composition.author(Practitioner as Practitioner with Mandatory
                        Identifier).Practitioner.identifier</td>
                </tr>

                <tr>
                    <td>No Address for the consumer</td>
                    <td>028319</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td>No Electronic Communication Detail for the consumer</td>
                    <td>028320</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td>Attribute for Healthcare Setting</td>
                    <td>028349</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td>Packed medicines present</td>
                    <td>028413</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="3">Additional Comment</td>
                    <td rowspan="3">028348</td>
                    <td rowspan="3">List.note</td>
                    <td>Composition.section(Medications)</td>
                </tr>
                <tr>
                    <td>Composition.section(Medications).entry</td>
                </tr>
                <tr>
                    <td>Composition.section(Medications).entry(List as List of Medicine Items from a Review).List.note</td>
                </tr>
                <tr>
                    <td rowspan="4">Attribute for Substance/ Agent of allergy and adverse
                        reaction</td>
                    <td rowspan="4">028330</td>
                    <td rowspan="3">AllergyIntolerance.code</td>
                    <td>Composition.section(Allergies)</td>
                </tr>
                <tr>
                    <td>Composition.section(Allergies).entry</td>
                </tr>
                <tr>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement
                        of Allergy or Intolerance).AllergyIntolerance.code</td>
                </tr>
                <tr>
                    <td>AllergyIntolerance.reaction.substance</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement
                        of Allergy or Intolerance).AllergyIntolerance.reaction.substance</td>
                </tr>
                <tr>
                    <td>Attribute for Reaction Type</td>
                    <td>028331</td>
                    <td>AllergyIntolerance.type</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement
                        of Allergy or Intolerance).AllergyIntolerance.type</td>
                </tr>
                <tr>
                    <td>Attribute for Reaction</td>
                    <td>028332</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement
                        of Allergy or Intolerance).AllergyIntolerance.reaction.manifestation</td>
                </tr>
                <tr>
                    <td>Attribute for Reaction Onset Date</td>
                    <td>028410</td>
                    <td>AllergyIntolerance.onset</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement
                        of Allergy or Intolerance).AllergyIntolerance.onset</td>
                </tr>
                <tr>
                    <td>Attribute for Medicine Identifier</td>
                    <td>028329</td>
                    <td>Medication.code</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.medication(Medication as Known
                        Medication).Medication.code</td>
                </tr>
                <tr>
                    <td>Attribute for Active Ingredient</td>
                    <td>028333</td>
                    <td>Medication.ingredient</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.medication(Medication as Known
                        Medication).Medication.ingredient</td>
                </tr>
                <tr>
                    <td>No Latin words or abbreviations of Active Ingredient</td>
                    <td>028390</td>
                    <td></td>
                    <td></td>
                </tr>

                <tr>
                    <td rowspan="2">Attribute for Brand Name</td>
                    <td rowspan="2">028335</td>
                    <td>Medication.code</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.medication(Medication as Known
                        Medication).Medication.code</td>
                </tr>
                <tr>
                    <td>Medication.medication-brand-name</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.medication(Medication as Known
                        Medication).Medication.medication-brand-name</td>
                </tr>
                <tr>
                    <td>Active Ingredient or Brand Name</td>
                    <td>028412</td>
                    <td></td>
                    <td></td>
                </tr>

                <tr>
                    <td>Attribute for Strength</td>
                    <td>028392</td>
                    <td>Medication.ingredient.amount</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.medication(Medication as Known
                        Medication).Medication.ingredient.amount</td>
                </tr>
                <tr>
                    <td rowspan="2">Attribute for Dose Form</td>
                    <td rowspan="2">028391</td>
                    <td>Medication.code</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.medication(Medication as Known
                        Medication).Medication.code</td>
                </tr>
                <tr>
                    <td>Medication.form</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.medication(Medication as Known
                        Medication).Medication.form</td>
                </tr>
                <tr>
                    <td>Attribute for Route</td>
                    <td>028399</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.dosage</td>
                </tr>
                <tr>
                    <td>Attribute for Direction</td>
                    <td>028336</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.dosage</td>
                </tr>
                <tr>
                    <td>No Latin words or abbreviations for Direction</td>
                    <td>028337</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td>Attribute for Medicine Purpose</td>
                    <td>028338</td>
                    <td>MedicationStatement.reasonCode</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.reasonCode</td>
                </tr>
                <tr>
                    <td>Terminology for Medicine Purpose</td>
                    <td>028339</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td>Attribute for Expected End Date</td>
                    <td>028343</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td>Attribute for Special Instruction</td>
                    <td>028345</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(Medications).entry(List as
                        List of Medicine Items from a Review).List.entry.item(MedicationStatement as Detailed Statement of Known
                        Medication).MedicationStatement.dosage</td>
                </tr>
                <tr>
                    <td>Attribute for Medicine Image</td>
                    <td>028346</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td>Image sizes</td>
                    <td>028406</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td>Attribute for Physical Descriptions</td>
                    <td>028347</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td>Attribute for reason for ceasing medicine</td>
                    <td>028351</td>
                    <td></td>
                    <td></td>
                </tr>
                <tr>
                    <td>Attribute for Medicine Status</td>
                    <td>028342</td>
                    <td>List.entry.flag</td>
                    <td>Composition.section(Medications).entry(List as List of Medicine Items from a Review).List.entry.flag</td>
                </tr>
             </tbody>
        </table>
            
             
          


