<table class="list" width="100%">
<tbody>
  <tr>
    <th>Reference</th>
    <th>Description</th>
    <th>Issue No.</th>
  </tr>
  <tr>
        <td>code (incorrect use of fixedCodeableConcept)</td>
        <td>The HL7 AU Assertion of No Relevant Finding profile, from which this profile is derived, fixes the value on Observation.code by using fixedCodeableConcept. The result of this is to prohibit CodeableConcept.text and CodeableConcept.coding.display (as well as other elements), which will inhibit the representation of realistic instances of data. An alternate method of fixing values has been devised (as is documented in an associated ticket shown to the right). This issue will be fixed in an R4 variant of this profile.</td>
        <td>See GitHub <a href="https://github.com/hl7au/au-fhir-base/issues/326">StructureDefinition-au-norelevantfinding :: incorrect use of fixedCodeableConcept on Observation.code</a></td>
  </tr>
  <tr>
        <td>Constraint presentation</td>
        <td>The full set of constraints (i.e. invariants) defined in this profile are only presented in the Detailed Descriptions tab or the raw representation (e.g. XML) of the profile. The Differential Table only presents constraints introduced in this profile in addition to the constraints present in the base profile and base resource. The Snapshot Table only presents the constraints visible in the Differential Table and additionally presents those constraints set in slices in the base profile.</td>
        <td>See Zulip <a href="https://chat.fhir.org/#narrow/stream/179252-IG-creation/topic/Derived.20profile.20snapshot.20missing.20upstream.20invariants">Derived profile snapshot missing upstream invariants</a> stream</td>
  </tr>
</tbody>
</table>
