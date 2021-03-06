# {{ page.title }}
{% include publish-box.html %}
{:.no_toc}
<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->
* Do not remove this line (it will not be displayed)
{:toc}

## Introduction

This informative section provides a mapping from the requirements of each end-product clinical specification to elements in a profiled FHIR resource.

The mapping from requirements table below demonstrates the logical decomposition of each requirement to the lowest possible element in an applicable profile. 

## Mapping from SHS information requirements

This informative section provides mapping from the data items (i.e. requirements) in [Shared Health Summary Information Requirements [NEHT2015e]](index.html#NEHT2015e) to elements in a profiled FHIR resource.

The table below matches the data items to the corresponding supported element in the [{{site.data.fhir.igName}}](StructureDefinition-composition-shs-1.html) profile, or referenced profile (e.g. [Summary Statement of Allergy or Intolerance](StructureDefinition-allergyintolerance-summary-1.html)). The hierarchy column demonstrates the path to that supported element from the root Composition. 

<table class="list" width="100%">
               <thead>
                    <tr>
                    <th>Data Item</th>
                    <th>Req. No</th>
                    <th>Element</th>
                    <th>Hierarchy</th>
                    <th>Additional notes</th>
                </tr>
                </thead>
               <tfoot>
                  <tr>
                    <td></td>
                    <td></td>
                    <td>Supported element</td>
                    <td>The path to the supported element from the root Composition</td>
                    <td></td>
                </tr>
                </tfoot> 
                <tbody> 
                <tr>
                    <td>Individual Healthcare Identifier (mandatory)</td>
                    <td>022082</td>
                    <td>Patient.identifier</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.identifier</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Individual’s Title (optional)</td>
                    <td>022081</td>
                    <td>Patient.name</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Individual’s Given Name (optional)</td>
                    <td>023056</td>
                    <td>Patient.name</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Individual’s family name (mandatory)</td>
                    <td>023058</td>
                    <td>Patient.name</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Individual’s Name Suffix (optional)</td>
                    <td>023059</td>
                    <td>Patient.name</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Individual’s Sex (mandatory)</td>
                    <td>024032</td>
                    <td>Patient.gender</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.gender</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Individual’s Date of Birth (mandatory)</td>
                    <td>023060</td>
                    <td>Patient.birthDate</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.birthDate</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Date of Birth accuracy indicator (optional)</td>
                    <td>024026</td>
                    <td>Patient.birthDate.date-accuracy-indicator</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.birthDate.date-accuracy-indicator</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Individual’s Address (mandatory)</td>
                    <td>024041</td>
                    <td>Patient.address</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.address</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Individual’s Electronic Communication Details (optional)</td>
                    <td>024042</td>
                    <td>Patient.telecom</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.telecom</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Indigenous Status (mandatory)</td>
                    <td>024033</td>
                    <td>Patient.indigenous-status</td>
                    <td>Composition.subject(Patient as Patient with Mandatory IHI).Patient.indigenous-status</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Healthcare Provider Professional Role (mandatory)</td>
                    <td>024040</td>
                    <td>PractitionerRole.code</td>
                    <td>Composition.composition-author-role.PractitionerRole.code</td>
                    <td></td>
                </tr>
                 <tr>
                    <td>Healthcare provider organisation name (mandatory)</td>
                    <td>023070</td>
                    <td>Organization.name</td>
                    <td>Composition.composition-author-role.PractitionerRole.organization(Organization as Base Organization).Organization.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Healthcare Provider Employer Organisation Address</td>
                    <td>025064</td>
                    <td>Organization.address</td>
                    <td>Composition.composition-author-role.PractitionerRole.organization(Organization as Base Organization).Organization.address</td>
                    <td></td>
                </tr>

                <tr>
                    <td>Healthcare provider organisation name (mandatory)</td>
                    <td>023070</td>
                    <td>Organization. name</td>
                    <td>Composition.composition-author-role.PractitionerRole.organization(Organization as Base Organization).Organization.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Healthcare Provider Employer Organisation Electronic Communication Detail</td>
                    <td>025063</td>
                    <td>Organization.telecom</td>
                    <td>Composition.composition-author-role.PractitionerRole.organization(Organization as Base Organization).Organization.telecom</td>
                    <td></td>
                </tr>

                <tr>
                    <td>Healthcare provider Identifier-Individual (mandatory)</td>
                    <td>023066</td>
                    <td>Practitioner.identifier</td>
                    <td>Composition.composition-author-role.PractitionerRole.practitioner(Practitioner as Practitioner with Mandatory Identifier).Practitioner.identifier </td>
                    <td></td>
                </tr>
                <tr>
                    <td>Healthcare Provider Identifier-Organisation (mandatory)</td>
                    <td>023071</td>
                    <td>Organization.identifier</td>
                    <td>Composition.composition-author-role.PractitionerRole.organization(Organization as Base Organization).Organization.identifier</td>
                    <td></td>
                </tr>

                <tr>
                    <td>Healthcare Provider Identifier-Organisation (mandatory)</td>
                    <td>023071</td>
                    <td>Organization.identifier</td>
                    <td>Composition.composition-author-role.PractitionerRole.organization(Organization as Base Organization).Organization.identifier</td>
                    <td></td>
                </tr>

                <tr>
                    <td rowspan="2">Healthcare Provider’s Title (optional)</td>
                    <td rowspan="2">023061</td>
                    <td>Practitioner.name</td>
                    <td>Composition.composition-author-role.PractitionerRole.practitioner(Practitioner as Practitioner with Mandatory Identifier).Practitioner.name</td>
                </tr>
                <tr>
                    <td>Practitioner.name </td>
                    <td>Composition.author(Practitioner as Practitioner with Mandatory Identifier).Practitioner.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">Healthcare Provider Given Name (optional)</td>
                    <td rowspan="2">023062</td>
                    <td>Practitioner.name</td>
                    <td>composition-author-role.practitioner(Practitioner as Practitioner with Mandatory Identifier).Practitioner.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Practitioner.name</td>
                    <td>Composition.composition-author-role.practitioner(Practitioner as Practitioner with Mandatory Identifier).Practitioner.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">Healthcare Provider Family Name (mandatory)</td>
                    <td rowspan="2">023064</td>
                    <td>Practitioner.name</td>
                    <td>Composition.composition-author-role.practitioner(Practitioner as Practitioner with Mandatory Identifier).Practitioner.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Practitioner.name</td>
                    <td>Composition.author(Practitioner as Practitioner with Mandatory Identifier).Practitioner.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">Healthcare provider name suffix (optional)</td>
                    <td rowspan="2">023065</td>
                    <td>Practitioner.name </td>
                    <td>Composition.composition-author-role.PractitionerRole.practitioner(Practitioner as Practitioner with Mandatory Identifier).Practitioner.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Practitioner.name</td>
                    <td>Composition.author(Practitioner as Practitioner with Mandatory Identifier).Practitioner.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Healthcare Provider Individual’s Workplace Address (optional)</td>
                    <td>024035</td>
                    <td>Practitioner.address</td>
                    <td>Composition.composition-author-role.ractitionerRole.practitioner(Practitioner as Practitioner with Mandatory Identifier).Practitioner.name</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">Healthcare Provider Individual’s Workplace Electronic
                        Communication Details (optional)</td>
                    <td rowspan="2">024036</td>
                    <td>Practitioner.telecom</td>
                    <td>Composition.composition-author-role.ractitionerRole.practitioner(Practitioner as Practitioner with Mandatory Identifier).Practitioner.telecom</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Practitioner.telecom</td>
                    <td>Composition.author(Practitioner as Practitioner with Mandatory Identifier).Practitioner.telecom</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="5">Component</td>
                    <td rowspan="3">022870</td>
                    <td>Composition.section(Allergies)</td>
                    <td>Composition.section(Allergies)</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Composition.section(Allergies).entry</td>
                    <td>Composition.section(Allergies).entry</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Composition.section(Allergies).emptyReason</td>
                    <td>Composition.section(Allergies).emptyReason</td>
                    <td></td>
                </tr>

                <tr>
                    <td rowspan="2">024962</td>
                    <td>AllergyIntolerance.code</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.code</td>
                    <td></td>
                </tr>
                <tr>
                    <td> Composition.section(Allergies).emptyReason</td>
                    <td>Composition.section(Allergies).emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="4">Agent Description</td>
                    <td rowspan="2">022871</td>
                    <td>AllergyIntolerance.code</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.code</td>
                    <td></td>
                </tr>
                <tr>
                    <td>AllergyIntolerance.reaction.substance</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.substance</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">023235</td>
                    <td>AllergyIntolerance.code</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.code</td>
                    <td></td>
                </tr>
                <tr>
                    <td>AllergyIntolerance.reaction.substance</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.substance</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">Reaction Type</td>
                    <td>024963</td>
                    <td>AllergyIntolerance.type</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.type</td>
                    <td></td>
                </tr>
                <tr>
                    <td>024964</td>
                    <td>AllergyIntolerance.type</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.type</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="4">Reaction Description</td>
                    <td>023239</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.manifestation</td>
                    <td></td>
                </tr>
                <tr>
                    <td>022887</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.manifestation</td>
                    <td></td>
                </tr>
                <tr>
                    <td>023240</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance).AllergyIntolerance.reaction.manifestation</td>
                    <td></td>
                </tr>
                <tr>
                    <td>023241</td>
                    <td>AllergyIntolerance.reaction.manifestation</td>
                    <td>Composition.section(Allergies).entry(AllergyIntolerance as Summary Statement of Allergy or Intolerance).AllergyIntolerance.reaction.manifestation</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="5">Component</td>
                    <td rowspan="3">022746</td>
                    <td>Composition.section(Medications)</td>
                    <td>Composition.section(Medications)</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Composition.section(Medications).entry</td>
                    <td>Composition.section(Medications).entry</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Composition.section(Medications).emptyReason</td>
                    <td>Composition.section(Medications).emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">024965</td>
                    <td>Composition.section(Medications).entry</td>
                    <td>Composition.section(Medications).entry</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Composition.section(Medications).emptyReason</td>
                    <td>Composition.section(Medications).emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="3">Item Description</td>
                    <td>023242</td>
                    <td>MedicationStatement.medication[x]</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.medication[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td>023243</td>
                    <td>MedicationStatement.medication[x]</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.medication[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td>023244</td>
                    <td>MedicationStatement.medication[x]</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.medication[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Dose Instructions</td>
                    <td>023245</td>
                    <td>MedicationStatement.dosage</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.dosage</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">Reason for Medicine</td>
                    <td>023246</td>
                    <td>MedicationStatement.reasonCode</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.reasonCode</td>
                    <td></td>
                </tr>
                <tr>
                    <td>023247</td>
                    <td>MedicationStatement.reasonCode</td>
                  <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.reasonCode</td>
                  <td></td>
                </tr>
                <tr>
                    <td rowspan="2">Additional comments</td>
                    <td>023248</td>
                    <td>MedicationStatement.note</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.note</td>
                    <td></td>
                </tr>
                <tr>
                    <td>023249</td>
                    <td>MedicationStatement.note</td>
                    <td>Composition.section(Medications).entry(MedicationStatement as Summary Statement of Known Medicine).MedicationStatement.note</td>
                    <td></td>
                </tr>
                <tr>
                <td rowspan="6">Component</td>
                <td rowspan="3">023250</td>
                <td>Composition.section(MedicalHistory)</td>
                <td>Composition.section(MedicalHistory)</td>
                <td></td>
        </tr>
        <tr>
              <td>Composition.section(MedicalHistory).entry</td>
              <td>Composition.section(MedicalHistory).entry</td>
              <td></td>
        </tr>
        <tr>
            <td>Composition.section(MedicalHistory).emptyReason</td>
            <td>Composition.section(MedicalHistory).emptyReason</td>
            <td></td>
        </tr>
        <tr>
            <td>023251</td>
            <td>Composition.section(MedicalHistory).entry</td>
            <td>Composition.section(MedicalHistory).entry</td>
            <td></td>
        </tr>
        <tr>
            <td rowspan="2">024966</td>
            <td>Composition.section(MedicalHistory).entry</td>
            <td>Composition.section(MedicalHistory).entry</td>
            <td></td>
        </tr>
        <tr>
            <td>Composition.section(MedicalHistory).emptyReason</td>
            <td>Composition.section(MedicalHistory).emptyReason</td>
            <td></td>
        </tr>
                <tr>
                    <td rowspan="6">Medical History Description</td>
                    <td rowspan="2">023252</td>
                    <td>Condition.code</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.code</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Procedure.code</td>
                    <td>Composition.section(MedicalHistory).entry(Procedure as Summary Statement of Known Procedure).Procedure.code</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">023253</td>
                    <td>Condition.code</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.code</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Procedure.code</td>
                    <td>Composition.section(MedicalHistory).entry(Procedure as Summary Statement of Known Procedure).Procedure.code</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">023236</td>
                    <td>Condition.code</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.code</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Procedure.code</td>
                    <td>Composition.section(MedicalHistory).entry(Procedure as Summary Statement of Known Procedure).Procedure.code</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="8">Medical History DateTime Range</td>
                    <td rowspan="2">024947</td>
                    <td>Condition.onset[x]</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.onset[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Condition.abatement[x]</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.abatement[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">024948</td>
                    <td>Condition.onset[x]</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.onset[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Condition.abatement[x]</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.abatement[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">024949</td>
                    <td>Condition.onset[x]</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.onset[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Condition.abatement[x]</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.abatement[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">024991</td>
                    <td>Condition.onset[x]</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.onset[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Condition.abatement[x]</td>
                    <td>Composition.section(MedicalHistory).entry(Condition).Condition.abatement[x]</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">Medical History comments</td>
                    <td rowspan="2">024950</td>
                    <td>Condition.note</td>
                    <td>Composition.section(MedicalHistory).entry(Condition as Summary Statement of Condition).Condition.note</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Procedure.note</td>
                    <td>Composition.section(MedicalHistory).entry(Procedure as Summary Statement of Known Procedure).Procedure.note</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="6">Component</td>
                    <td rowspan="3">023254</td>
                    <td>Composition.section(Immunisations)</td>
                    <td>Composition.section(Immunisations)</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Composition.section(Immunisations).entry</td>
                    <td>Composition.section(Immunisations).entry</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Composition.section(Immunisations).emptyReason</td>
                    <td>Composition.section(Immunisations).emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td>024924</td>
                    <td>Composition.section(Immunisations).entry</td>
                    <td>Composition.section(Immunisations).entry</td>
                    <td></td>
                </tr>
               <tr>
                    <td rowspan="2">024967</td>
                    <td>Composition.section(Immunisations).entry</td>
                    <td>Composition.section(Immunisations).entry</td>
                    <td></td>
                </tr>
                <tr>
                    <td>Composition.section(Immunisations).emptyReason</td>
                    <td>Composition.section(Immunisations).emptyReason</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="3">Vaccine Name</td>
                    <td>024925</td>
                    <td>Immunization.vaccineCode</td>
                    <td>Composition.section(Immunisations).entry(Immunization as Summary Statement of Administered Vaccine).Immunization.vaccineCode</td>
                    <td></td>
                </tr>
                <tr>
                    <td>024926</td>
                    <td>Immunization.vaccineCode</td>
                    <td>Composition.section(Immunisations).entry(Immunization as Summary Statement of Administered Vaccine).Immunization.vaccineCode</td>
                    <td></td>
                </tr>
                <tr>
                    <td>024927</td>
                    <td>Immunization.vaccineCode</td>
                    <td>Composition.section(Immunisations).entry(Immunization as Summary Statement of Administered Vaccine).Immunization.vaccineCode</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">DateTime Administration</td>
                    <td>024928</td>
                    <td>Immunization.date</td>
                    <td>Composition.section(Immunisations).entry(Immunization as Summary Statement of Administered Vaccine).Immunization.date</td>
                    <td></td>
                </tr>
                <tr>
                    <td>024929</td>
                    <td>Immunization.date</td>
                    <td>Composition.section(Immunisations).entry(Immunization as Summary Statement of Administered Vaccine).Immunization.date</td>
                    <td></td>
                </tr>
                <tr>
                    <td rowspan="2">Sequence Number</td>
                    <td>024930</td>
                    <td>Immunization.vaccinationProtocol.doseSequence</td>
                    <td>Composition.section(Immunisations).entry(Immunization as Summary Statement of Administered Vaccine).Immunization.vaccinationProtocol.doseSequence</td>
                    <td></td>
                </tr>
                <tr>
                    <td>024931</td>
                    <td>Immunization.vaccinationProtocol.doseSequence</td>
                    <td>Composition.section(Immunisations).entry(Immunization as Summary Statement of Administered Vaccine).Immunization.vaccinationProtocol.doseSequence</td>
                    <td></td>
                </tr>
                <tr>
                    <td>DateTime Attested (mandatory)</td>
                    <td>024038</td>
                    <td>Composition.attester(Legal Attester).time</td>
                    <td>Composition.attester(Legal Attester).time</td>
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
