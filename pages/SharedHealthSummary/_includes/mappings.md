# {{ page.title }}

This informative section provides mapping from the data items (i.e. requirements) in [NEHTA Shared Health Summary Information Requirements](https://www.digitalhealth.gov.au/implementation-resources/clinical-documents/EP-1816-2015/NEHTA-1837-2015) [NEHT2015e].

The table below matches the data items to the corresponding supported element in the Shared Health Summary (SHS) profile, or referenced profile (e.g. Summary Statement of Allergy or Intolerance). The hierarchy column demonstrates the path to that supported element from the root Composition. 

<table border="1" cellpadding="1" valign="middle">
               <thead>
                    <tr bgcolor="#DCDCDC">
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
                    <td>Individual Healthcare Identifier (mandatory)</td>
                    <td>022082</td>
                    <td>Patient.identifier</td>
                    <td>Composition.subject</td>
                </tr>
                <tr>
                    <td>Individual’s Title (optional)</td>
                    <td>022081</td>
                    <td>Patient.name</td>
                    <td>Composition.subject(Patient)</td>

                </tr>
                <tr>
                    <td>Individual’s Given Name (optional)</td>
                    <td>023056</td>
                    <td>Patient.name</td>
                    <td>Composition.subject(Patient)</td>
                </tr>
                <tr>
                    <td>Individual’s family name (mandatory)</td>
                    <td>023058</td>
                    <td>Patient.name</td>
                    <td>Composition.subject(Patient)</td>
                </tr>
                <tr>
                    <td>Individual’s Name Suffix (optional)</td>
                    <td>023059</td>
                    <td>Patient.name</td>
                    <td>Composition.subject(Patient)</td>
                </tr>
                <tr>
                    <td>Individual’s Sex (mandatory)</td>
                    <td>024032</td>
                    <td>Patient.gender</td>
                    <td>Composition.subject(Patient)</td>
                </tr>
                <tr>
                    <td>Individual’s Date of Birth (mandatory)</td>
                    <td>023060</td>
                    <td>Patient.birthDate</td>
                    <td>Composition.subject(Patient)</td>
                </tr>
                <tr>
                    <td>Date of Birth accuracy indicator (optional)</td>
                    <td>024026</td>
                    <td>Patient.birthDate.date-accuracy-indicator or Patient.birthDate.extension:accuracyIndicator</td>
                    <td>Composition.subject(Patient)</td>
                </tr>
                <tr>
                    <td>Individual’s Address (mandatory)</td>
                    <td>024041</td>
                    <td>Patient.address</td>
                    <td>Composition.subject(Patient)</td>
                </tr>
                <tr>
                    <td>Individual’s Electronic Communication Details (optional)</td>
                    <td>024042</td>
                    <td>Patient.telecom</td>
                    <td>Composition.subject(Patient)</td>
                </tr>
                <tr>
                    <td>Indigenous Status (mandatory)</td>
                    <td>024033</td>
                    <td>Patient.extension:indigenousStatus</td>
                    <td>Composition.subject(Patient)</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Professional Role (mandatory)</td>
                    <td>024040</td>
                    <td>PractitionerRole.code</td>
                    <td>Composition.extension:compositionAuthorRole</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Professional Role (mandatory)</td>
                    <td>024040</td>
                    <td>PractitionerRole. code</td>
                    <td>Composition.extension:compositionAuthorRole</td>
                </tr>
                <tr>
                    <td>Healthcare provider organisation name (mandatory)</td>
                    <td>023070</td>
                    <td>Organization. name</td>
                    <td>Composition.extension:compositionAuthorRole > PractitionerRole >
                        organization</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Employer Organisation Address</td>
                    <td>025064</td>
                    <td>Organization. address</td>
                    <td>Composition.extension:compositionAuthorRole  PractitionerRole >
                        organization</td>
                </tr>

                <tr>
                    <td>Healthcare provider organisation name (mandatory)</td>
                    <td>023070</td>
                    <td>Organization. name</td>
                    <td>CompoComposition.extension:compositionAuthorRole >  PractitionerRole >
                        organization</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Employer Organisation Electronic Communication
                        Detail</td>
                    <td>025063</td>
                    <td>Organization.telecom</td>
                    <td>Composition.extension:compositionAuthorRole > PractitionerRole >
                        organization(Organization</td>
                </tr>

                <tr>
                    <td>Healthcare provider Identifier-Individual (mandatory)</td>
                    <td>023066</td>
                    <td>Practitioner. identifier</td>
                    <td>Composition.extension:compositionAuthorRole> PractitionerRole > practitioner </td>
                </tr>
                <tr>
                    <td>Healthcare Provider Identifier-Organisation (mandatory)</td>
                    <td>023071</td>
                    <td>Organization.identifier</td>
                    <td>Composition.extension:compositionAuthorRole > PractitionerRole >
                        organization</td>
                </tr>

                <tr>
                    <td>Healthcare Provider Identifier-Organisation (mandatory)</td>
                    <td>023071</td>
                    <td>Organization. identifier</td>
                    <td>Composition.extension:compositionAuthorRole > PractitionerRole >
                        organization</td>
                </tr>

                <tr>
                    <td rowspan="2">Healthcare Provider’s Title (optional)</td>
                    <td rowspan="2">023061</td>
                    <td>Practitioner.name</td>
                    <td>Composition.extension:compositionAuthorRole > PractitionerRole >
                        practitioner</td>
                </tr>
                <tr>
                    <td>Practitioner. name </td>
                    <td>Composition.author</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Given Name (optional)</td>
                    <td>023062</td>
                    <td>PractitionerRole.name ?????</td>
                    <td>Composition.extension:compositionAuthorRole</td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td>Practitioner.name ????</td>
                    <td>Composition. author</td>
                </tr>

                <tr>
                    <td rowspan="2">Healthcare Provider Family Name (mandatory)</td>
                    <td rowspan="2">023064</td>
                    <td>Practitioner.name</td>
                    <td>Composition.extension:compositionAuthorRole > practitioner</td>
                </tr>
                <tr>
                    <td>Practitioner.name</td>
                    <td>Composition.author</td>
                </tr>
                <tr>
                    <td rowspan="2">Healthcare provider name suffix (optional)</td>
                    <td rowspan="2">023065</td>
                    <td>Practitioner.name </td>
                    <td>Composition.extension:compositionAuthorRole > PractitionerRole >
                        practitioner</td>
                </tr>
                <tr>
                    <td>Practitioner.name</td>
                    <td>Composition.author</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Individual’s Workplace Address (optional)</td>
                    <td>024035</td>
                    <td>Practitioner.address</td>
                    <td>Composition.extension:compositionAuthorRole PractitionerRole >
                        practitioner</td>
                </tr>
                <tr>
                    <td rowspan="2">Healthcare Provider Individual’s Workplace Electronic
                        Communication Details (optional)</td>
                    <td rowspan="2">024036</td>
                    <td>Practitioner.telecom</td>
                    <td>Composition.extension:compositionAuthorRole > PractitionerRole >
                        practitioner</td>
                </tr>
                <tr>
                    <td>Practitioner.telecom</td>
                    <td>Composition.author</td>
                </tr>
                <tr>
                    <td rowspan="5">Component</td>
                    <td rowspan="3">022870</td>
                    <td>Composition.section:allergies</td>
                    <td>Composition.section:allergies</td>
                </tr>
                <tr>
                    <td>AllergyIntolerance</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td>Composition.section:allergies.emptyReason</td>
                    <td>Composition.section:allergies.emptyReason</td>

                </tr>

                <tr>
                    <td rowspan="2">024962</td>
                    <td>AllergyIntolerance.code</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td> Composition.section:allergies.emptyReason</td>
                    <td>Composition.section:allergies.emptyReason</td>
                </tr>
                <tr>
                    <td rowspan="4">Agent Description</td>
                    <td rowspan="2">022871</td>
                    <td>AllergyIntolerance.code</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td>AllergyIntolerance.reaction.substance</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">023235</td>
                    <td>AllergyIntolerance.code</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td>AllergyIntolerance.reaction.substance</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">Reaction Type</td>
                    <td>024963</td>
                    <td>AllergyIntolerance.type</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td>024964</td>
                    <td>AllergyIntolerance.type</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td rowspan="4">Reaction Description</td>
                    <td>023239</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td>022887</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td>023240</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td>023241</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section:allergies.entry</td>
                </tr>
                <tr>
                    <td rowspan="4">Component</td>
                    <td rowspan="2">022746</td>
                    <td>MedicationStatement</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td>Observation</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">024965</td>
                    <td>MedicationStatement</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td>Observation</td>
                    <td>Composition.section:medications.entry</td>
                </tr>

                <tr>
                    <td rowspan="3">Item Description</td>
                    <td>023242</td>
                    <td>MedicationStatement. medication[x]</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td>023243</td>
                    <td>MedicationStatement.medication[x]</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td>023244</td>
                    <td>MedicationStatement.medication[x]</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td>Dose Instructions</td>
                    <td>023245</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">Reason for Medicine</td>
                    <td>023246</td>
                    <td>MedicationStatement.reasonCode</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td>023247</td>
                    <td>MedicationStatement.reasonCode</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">Additional comments</td>
                    <td>023248</td>
                    <td>MedicationStatement.note</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td>023249</td>
                    <td>MedicationStatement.note</td>
                    <td>Composition.section:medications.entry</td>
                </tr>
                <tr>
                    <td rowspan="12">Component</td>
                    <td rowspan="4">023250</td>
                    <td>Condition</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Procedure</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Observation</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Composition.section:medicalHistory.emptyReason</td>
                    <td>Composition.section:medicalHistory.emptyReason</td>
                </tr>
                <tr>
                    <td rowspan="4">023251</td>
                    <td>Condition</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Procedure</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Observation</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Composition.section:medicalHistory.emptyReason</td>
                    <td>Composition.section:medicalHistory.emptyReason</td>
                </tr>
                <tr>
                    <td rowspan="4">024966</td>
                    <td>Composition.section:medicalHistory.entry</td>
                    <td>Condition</td>
                 </tr>
                <tr>
                    <td>Procedure</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Observation</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Composition.section:medicalHistory.emptyReason</td>
                    <td>Composition.section:medicalHistory.emptyReason</td>
                </tr>
                <tr>
                    <td rowspan="6">Medical History Description</td>
                    <td rowspan="2">023252</td>
                    <td>Condition.code</td>
                    <td>Composition.section:medicalHistory.entry </td>
                </tr>
                <tr>
                    <td>Procedure.code</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">023253</td>
                    <td>Condition.code</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Procedure.code</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">023236</td>
                    <td>Condition.code</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Procedure.code</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td rowspan="8">Medical History DateTime Range</td>
                    <td rowspan="2">024947</td>
                    <td>Condition.onset[x]</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Condition.abatement[x]</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">024948</td>
                    <td>Condition.onset[x]</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Condition.abatement[x]</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">024949</td>
                    <td>Condition.onset[x]</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Condition.abatement[x]</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">024991</td>
                    <td>Condition.onset[x]</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Condition.abatement[x]</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">Medical History comments</td>
                    <td rowspan="2">024950</td>
                    <td>Condition.note</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td>Procedure.note</td>
                    <td>Composition.section:medicalHistory.entry</td>
                </tr>
                <tr>
                    <td rowspan="9">Component</td>
                    <td rowspan="3">023254</td>
                    <td>Immunization</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>Observation</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>Composition.section:immunisations.emptyReason</td>
                    <td>Composition.section:immunisations.emptyReason</td>
                </tr>
                <tr>
                    <td rowspan="3">024924</td>
                    <td>Immunization</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>Observation</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>Composition.section:immunisations.emptyReason</td>
                    <td>Composition.section:immunisations.emptyReason</td>
                </tr>
                <tr>
                    <td rowspan="3">024967</td>
                    <td>Immunization</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>Observation</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>Composition.section:immunisations.emptyReason</td>
                    <td>Composition.section:immunisations.emptyReason</td>
                </tr>
                <tr>
                    <td rowspan="3">Vaccine Name</td>
                    <td>024925</td>
                    <td>Immunization.vaccineCode</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>024926</td>
                    <td>Immunization.vaccineCode</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>024927</td>
                    <td>Immunization.vaccineCode</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">DateTime Administration</td>
                    <td>024928</td>
                    <td>Immunization.date</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>024929</td>
                    <td>Immunization.date</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td rowspan="2">Sequence Number</td>
                    <td>024930</td>
                    <td>Immunization.vaccinationProtocol.doseSequence</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>024931</td>
                    <td>Immunization.vaccinationProtocol.doseSequence</td>
                    <td>Composition.section:immunisations.entry</td>
                </tr>
                <tr>
                    <td>DateTime Attested (mandatory)</td>
                    <td>024038</td>
                    <td>Composition.ttester(Legal Attester) > time</td>
                    <td>Composition > attester(Legal Attester) > time</td>
                </tr>
            </tbody>
        </table>


