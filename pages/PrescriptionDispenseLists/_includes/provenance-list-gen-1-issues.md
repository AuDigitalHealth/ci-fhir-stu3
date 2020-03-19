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
        <td>target (list reference)</td>
        <td>inv-dh-prov-03 should enforce a reference to a list. This invariant needs to be updated to remove the part allowing an identifier.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/28">ci-fhir-stu3/issues/28</a></td>
      </tr>
      <tr>
        <td>activity (use of fixedCoding)</td>
        <td>This profile fixes the value on activity using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
      </tr>
      <tr>
        <td>agent:preparingEntity.role (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on agent:preparingEntity.role using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
      </tr>
      <tr>
        <td>agent:assemblingDevice.role (use of fixedCodeableConcept)</td>
        <td>This profile fixes the value on agent:assemblingDevice.role using fixedCodeableConcept. Fixing the value in this way prohibits parts of CodeableConcept that are intended to be optional including CodeableConcept.text and CodeableConcept.coding.display. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/48">ci-fhir-stu3/issues/48</a></td>
      </tr>
      <tr>
        <td>agent:All Slices (erroneous)</td>
        <td>The profile contains a slice "agent:All Slices" that is not an intended design for this profile. This slice will be removed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/72">ci-fhir-stu3/issues/72</a></td>
      </tr>
 </tbody>
</table>

