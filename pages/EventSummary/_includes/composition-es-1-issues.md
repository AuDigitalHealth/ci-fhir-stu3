<table class="list" width="100%">
<tbody>
  <tr>
    <th>Reference</th>
    <th>Description</th>
    <th>Issue No.</th>
  </tr>
  <tr>
        <td>Constraint presentation</td>
        <td>The full set of constraints (i.e. invariants) defined in this profile are only presented in the Detailed Descriptions tab or the raw representation (e.g. XML) of the profile. The Differential Table only presents constraints introduced in this profile in addition to the constraints present in the base profile and base resource. The Snapshot Table only presents the constraints visible in the Differential Table and additionally presents those constraints set in slices in the base profile.</td>
        <td>See Zulip <a href="https://chat.fhir.org/#narrow/stream/179252-IG-creation/topic/Derived.20profile.20snapshot.20missing.20upstream.20invariants">Derived profile snapshot missing upstream invariants</a> stream</td>
  </tr>
  <tr>
        <td>Composition.encounter</td>
        <td>The design of this profile is incomplete. This profile is missing an invariant to mandate the inclusion of Encounter.extension:encounterDescription.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/34">ci-fhir-stu3/issues/34</a></td>
  </tr>
  <tr>
        <td>type (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on Composition.type using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
  </tr>
  <tr>
        <td>section:eventOverview.code (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on Composition.section:eventOverview.code using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
  </tr>
  <tr>
        <td>section:allergies.code (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on Composition.section:allergies.code using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
  </tr>
  <tr>
        <td>section:medications.code (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on Composition.section:medications.code using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
  </tr>
  <tr>
        <td>section:medicalHistory.code (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on Composition.section:medicalHistory.code using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
  </tr>
  <tr>
        <td>section:immunisations.code (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on Composition.section:immunisations.code using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
  </tr>
  <tr>
        <td>section:diagnosticInvestigations.code (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on Composition.section:diagnosticInvestigations.code using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
  </tr>
 </tbody>
</table>
