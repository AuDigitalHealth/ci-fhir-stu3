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
        <td>inv-dh-lst-09</td>
        <td>This invariant should be merged into inv-dh-lst-04, so that it becomes 'The author role shall at least have a reference that conforms to PractitionerRole with Practitioner with Mandatory Identifier or an identifier with at least a system and a value'. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/73">ci-fhir-stu3/issues/73</a></td>
  </tr>
      <tr>
        <td>inv-dh-lst-10</td>
        <td>This invariant should be merged into inv-dh-lst-05, so that it becomes 'The authoring related person shall at least have a reference that conforms to RelatedPerson with Mandatory Identifier or an identifier with at least a system and a value'. This issue will be fixed in an R4 variant of this profile.</td>
        <td>See <a href="https://github.com/AuDigitalHealth/ci-fhir-stu3/issues/73">ci-fhir-stu3/issues/73</a></td>
  </tr>  
 </tbody>
</table>
