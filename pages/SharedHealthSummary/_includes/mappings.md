# {{ page.title }}

This informative section provides mapping from the data items (i.e. requirements) in [NEHTA Shared Health Summary Information Requirements](https://www.digitalhealth.gov.au/implementation-resources/clinical-documents/EP-1816-2015/NEHTA-1837-2015) [NEHT2015e].

The table below matches the data items to the corresponding supported element in the Shared Health Summary (SHS) profile, or referenced profile (e.g. Summary Statement of Allergy or Intolerance). The hierarchy column demonstrates the path to that supported element from the root Composition. 

 <table border="1" cellpadding="1" valign="middle">
            <tbody>
                <tr bgcolor="#DCDCDC">
                    <th>Data Item</th>
                    <th>Req. No</th>
                    <th>Hierarchy</th>
                    <th>FHIR element</th>
                </tr>
                <tr>
                    <td>Individual Healthcare Identifier (mandatory)</td>
                    <td>022082</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > identifier</td>
                </tr>
                <tr>
                    <td>Individual’s Title (optional)</td>
                    <td>022081</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > name</td>
                </tr>
                <tr>
                    <td>Individual’s Given Name (optional)</td>
                    <td>023056</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > name</td>
                </tr>
                <tr>
                    <td>Individual’s family name (mandatory)</td>
                    <td>023058</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > name</td>
                </tr>
                <tr>
                    <td>Individual’s Name Suffix (optional)</td>
                    <td>023059</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > name</td>
                </tr>
                <tr>
                    <td>Individual’s Sex (mandatory)</td>
                    <td>024032</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > name</td>
                </tr>
                <tr>
                    <td>Individual’s Date of Birth (mandatory)</td>
                    <td>023060</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > birthDate</td>
                </tr>
                <tr>
                    <td>Date of Birth accuracy indicator (optional)</td>
                    <td>024026</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > birthDate > date-accuracy-indicator</td>
                </tr>
                <tr>
                    <td>Individual’s Address (mandatory)</td>
                    <td>024041</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > address</td>
                </tr>
                <tr>
                    <td>Individual’s Electronic Communication Details (optional)</td>
                    <td>024042</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > telecom</td>
                </tr>
                <tr>
                    <td>Indigenous Status (mandatory)</td>
                    <td>024033</td>
                    <td>Composition > subject(Patient)</td>
                    <td>Patient > indigenous-status</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Professional Role (mandatory)</td>
                    <td>024040</td>
                    <td>Composition > composition-author-role</td>
                    <td>PractitionerRole > code</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Professional Role (mandatory)</td>
                    <td>024040</td>
                    <td>Composition > composition-author-role</td>
                    <td>PractitionerRole > code</td>
                </tr>
                <tr>
                    <td>Healthcare provider organisation name (mandatory)</td>
                    <td>023070</td>
                    <td>Composition > composition-author-role > PractitionerRole > organization</td>
                    <td>Organization > name</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Employer Organisation Address</td>
                    <td>025064</td>
                    <td>Composition > composition-author-role PractitionerRole > organization</td>
                    <td>Organization > address</td>
                </tr>

                <tr>
                    <td>Healthcare provider organisation name (mandatory)</td>
                    <td>023070</td>
                    <td>Composition > composition-author-role > PractitionerRole > organization</td>
                    <td>Organization > name</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Employer Organisation Electronic Communication
                        Detail</td>
                    <td>025063</td>
                    <td>Composition > composition-author-role</td>
                    <td>PractitionerRole > organization(Organization) > Organization > telecom</td>
                </tr>

                <tr>
                    <td>Healthcare provider Identifier-Individual (mandatory)</td>
                    <td>023066</td>
                    <td>Composition > composition-author-role > PractitionerRole > practitioner </td>
                    <td>Practitioner > identifier</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Identifier-Organisation (mandatory)</td>
                    <td>023071</td>
                    <td>Composition > composition-author-role > PractitionerRole > organization</td>
                    <td>Organization > identifier</td>
                </tr>

                <tr>
                    <td>Healthcare Provider Identifier-Organisation (mandatory)</td>
                    <td>023071</td>
                    <td>Composition > composition-author-role > PractitionerRole > organization</td>
                    <td>Organization > identifier</td>
                </tr>

                <tr>
                    <td rowspan="2">Healthcare Provider’s Title (optional)</td>
                    <td rowspan="2">023061</td>
                    <td>Composition > composition-author-role > PractitionerRole > practitioner</td>
                    <td>Practitioner >
                        name</td>
                </tr>
                <tr>
                    <td>Composition > author</td>
                    <td>Practitioner > name </td>
                </tr>
                <tr>
                    <td>Healthcare Provider Given Name (optional)</td>
                    <td>023062</td>
                    <td>Composition > composition-author-role</td>
                    <td>>PractitionerRole > name ?????</td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td>Composition > author</td>
                    <td>Practitioner > name ????</td>
                </tr>

                <tr>
                    <td>Healthcare Provider Family Name (mandatory)</td>
                    <td>023064</td>
                    <td>Composition > composition-author-role > practitioner</td>
                    <td>Practitioner > name</td>
                </tr>
                <tr>
                    <td></td>
                    <td></td>
                    <td>Composition > author</td>
                    <td> Practitioner > name</td>
                </tr>
                <tr>
                    <td rowspan="2">Healthcare provider name suffix (optional)</td>
                    <td rowspan="2">023065</td>
                    <td>Composition > composition-author-role > PractitionerRole > practitioner</td>
                    <td>Practitioner > name </td>
                </tr>
                <tr>
                    <td>Composition > author</td>
                    <td> Practitioner > name</td>
                </tr>
                <tr>
                    <td>Healthcare Provider Individual’s Workplace Address (optional)</td>
                    <td>024035</td>
                    <td>Composition > composition-author-role PractitionerRole > practitioner</td>
                    <td>Practitioner > address</td>
                </tr>
                <tr>
                    <td rowspan="2">Healthcare Provider Individual’s Workplace Electronic
                        Communication Details (optional)</td>
                    <td rowspan="2">024036</td>
                    <td>Composition > composition-author-role > PractitionerRole > practitioner</td>
                    <td>Practitioner > telecom</td>
                </tr>
                <tr>
                    <td>Composition > author</td>
                    <td>Practitioner > telecom</td>
                </tr>
                <tr>
                    <td rowspan="5">Component</td>
                    <td rowspan="3">022870</td>
                    <td>Composition > section(Allergies)</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance</td>
                </tr>
                <tr>
                    <td>Composition > section(Allergies) > emptyReason</td>
                    <td></td>
                </tr>

                <tr>
                    <td rowspan="2">024962</td>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > code</td>
                </tr>
                <tr>
                    <td>Composition > section(Allergies) > emptyReason</td>
                    <td> </td>
                </tr>
                <tr>
                    <td rowspan="4">Agent Description</td>
                    <td rowspan="2">022871</td>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > code</td>
                </tr>
                <tr>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > reaction > substance</td>
                </tr>
                <tr>
                    <td rowspan="2">023235</td>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > code</td>
                </tr>
                <tr>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > reaction > substance</td>
                </tr>
                <tr>
                    <td rowspan="2">Reaction Type</td>
                    <td>024963</td>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > type</td>
                </tr>
                <tr>
                    <td>024964</td>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > type</td>
                </tr>
                <tr>
                    <td rowspan="4">Reaction Description</td>
                    <td>023239</td>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > reaction > manifestation</td>
                </tr>
                <tr>
                    <td>022887</td>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > reaction > manifestation</td>
                </tr>
                <tr>
                    <td>023240</td>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > reaction > manifestation</td>
                </tr>
                <tr>
                    <td>023241</td>
                    <td>Composition > section(Allergies) > entry</td>
                    <td>AllergyIntolerance > reaction > manifestation</td>
                </tr>
                <tr>
                    <td rowspan="4">Component</td>
                    <td rowspan="2">022746</td>
                    <td>Composition > section(Medications) > entry</td>
                    <td>MedicationStatement</td>
                </tr>
                <tr>
                    <td>Composition > section(Medications) > entry</td>
                    <td>Observation</td>
                </tr>
                <tr>
                    <td rowspan="2">024965</td>
                    <td>Composition > section(Medications) > entry</td>
                    <td>MedicationStatement</td>
                </tr>
                <tr>
                    <td>Composition > section(Medications) > entry</td>
                    <td>Observation</td>
                </tr>

                <tr>
                    <td rowspan="3">Item Description</td>
                    <td>023242</td>
                    <td>Composition > section(Medications) > entry</td>
                    <td>MedicationStatement > medication[x]</td>
                </tr>
                <tr>
                    <td>023243</td>
                    <td>Composition > section(Medications) > entry</td>
                    <td>MedicationStatement > medication[x]</td>
                </tr>
                <tr>
                    <td>023244</td>
                    <td>Composition > section(Medications) > entry</td>
                    <td>MedicationStatement > medication[x]</td>
                </tr>
                <tr>
                    <td>Dose Instructions</td>
                    <td>023245</td>
                    <td>Composition > section(Medications) > entry</td>
                    <td>MedicationStatement > dosage</td>
                </tr>
                <tr>
                    <td rowspan="2">Reason for Medicine</td>
                    <td>023246</td>
                    <td>Composition > section(Medications) > entry</td>
                    <td>MedicationStatement > reasonCode</td>
                </tr>
                <tr>
                    <td>023247</td>
                    <td>Composition > section(Medications) > entry</td>
                    <td>MedicationStatement > reasonCode</td>
                </tr>
                <tr>
                    <td rowspan="2">Additional comments</td>
                    <td>023248</td>
                    <td>Composition > section(Medications) > entry</td>
                    <td>MedicationStatement > note</td>
                </tr>
                <tr>
                    <td>023249</td>
                    <td>Composition > section(Medications) > entry</td>
                    <td>MedicationStatement > note</td>
                </tr>
                <tr>
                    <td rowspan="12">Component</td>
                    <td rowspan="4">023250</td>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Procedure</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Observation</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="4">023251</td>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Procedure</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Observation</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="4">024966</td>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Procedure</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Observation</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="6">Medical History Description</td>
                    <td rowspan="2">023252</td>
                    <td>Composition > section(MedicalHistory) > entry > </td>
                    <td>Condition > code</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) >entry</td>
                    <td>Procedure > code</td>
                </tr>
                <tr>
                    <td rowspan="2">023253</td>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > code</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) >entry</td>
                    <td>Procedure > code</td>
                </tr>
                <tr>
                    <td rowspan="2">023236</td>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > code</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) >entry</td>
                    <td>Procedure > code</td>
                </tr>
                <tr>
                    <td rowspan="8">Medical History DateTime Range</td>
                    <td rowspan="2">024947</td>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > onset[x]</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > abatement[x]</td>
                </tr>
                <tr>
                    <td rowspan="2">024948</td>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > onset[x]</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > abatement[x]</td>
                </tr>
                <tr>
                    <td rowspan="2">024949</td>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > onset[x]</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > abatement[x]</td>
                </tr>
                <tr>
                    <td rowspan="2">024991</td>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > onset[x]</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > abatement[x]</td>
                </tr>
                <tr>
                    <td rowspan="2">Medical History comments</td>
                    <td rowspan="2">024950</td>
                    <td>Composition > section(MedicalHistory) > entry</td>
                    <td>Condition > note</td>
                </tr>
                <tr>
                    <td>Composition > section(MedicalHistory) >entry</td>
                    <td>Procedure > note</td>
                </tr>
                <tr>
                    <td rowspan="9">Component</td>
                    <td rowspan="3">023254</td>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Immunization</td>
                </tr>
                <tr>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Observation</td>
                </tr>
                <tr>
                    <td>Composition > section(Immunisations) > emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="3">024924</td>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Immunization</td>
                </tr>
                <tr>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Observation</td>
                </tr>
                <tr>
                    <td>Composition > section(Immunisations) > emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="3">024967</td>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Immunization</td>
                </tr>
                <tr>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Observation</td>
                </tr>
                <tr>
                    <td>Composition > section(Immunisations) > emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="3">Vaccine Name</td>
                    <td>024925</td>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Immunization > vaccineCode</td>
                </tr>
                <tr>
                    <td>024926</td>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Immunization > vaccineCode</td>
                </tr>
                <tr>
                    <td>024927</td>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Immunization > vaccineCode</td>
                </tr>
                <tr>
                    <td rowspan="2">DateTime Administration</td>
                    <td>024928</td>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Immunization > date</td>
                </tr>
                <tr>
                    <td>024929</td>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Immunization > date</td>
                </tr>
                <tr>
                    <td rowspan="2">Sequence Number</td>
                    <td>024930</td>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Immunization > vaccinationProtocol > doseSequence</td>
                </tr>
                <tr>
                    <td>024931</td>
                    <td>Composition > section(Immunisations) > entry</td>
                    <td>Immunization > vaccinationProtocol > doseSequence</td>

                </tr>
                <tr>
                    <td>DateTime Attested (mandatory)</td>
                    <td>024038</td>
                    <td>Composition > attester(Legal Attester) > time</td>
                    <td></td>
                </tr>
            </tbody>
        </table>



