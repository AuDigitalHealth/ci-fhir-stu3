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
        <td>Profile design</td>
        <td>The design of this profile is incomplete. The profile is missing on invariants to turn the implementation guidance into the rules in the profile, for example to constrain the document type to match the sections. This issue will be fixed in an R4 variant of this profile.</td>
        <td>n/a</td>  
  </tr>
  <tr>
        <td>section:dispenseList.code (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on Composition.section:dispenseList.code using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
  </tr>
   <tr>
        <td>section:prescriptionList.code (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on Composition.section:prescriptionList.code using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
  </tr>
   <tr>
        <td>section:prescriptionDispenseList.code (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on Composition.section:prescriptionDispenseList.code using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
  </tr>
  <tr>
        <td>Unconfirmed FHIRPath expressions (inv-dh-cmp-04, inv-dh-cmp-05,inv-dh-cmp-09)</td>
        <td>This is the early design of the Composition profile. FHIRPath expressions for invariants inv-dh-cmp-04, inv-dh-cmp-05 and inv-dh-cmp-09 have not been validated and may not function as intented. This issue will be fixed in an R4 variant of this profile. </td>
        <td>n/a</td>
  </tr>
  <tr>
        <td>FHIRPath expression not mathing the invariant description (inv-dh-cmp-08)</td>
        <td>FHIRPath expression for invariant inv-dh-cmp-08 does not match the invariant description in that it does not limit the number of entries of type list to one and only one. This issue will be fixed in an R4 variant of this profile. </td>
        <td>n/a</td>
  </tr>
  </tbody>
</table>
