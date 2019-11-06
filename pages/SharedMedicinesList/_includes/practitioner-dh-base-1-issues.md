<table class="list" width="100%">
<tbody>
  <tr>
    <th>Reference</th>
    <th>Description</th>
    <th>Issue No.</th>
  </tr>
  <tr>
        <td>qualification</td>
        <td>The must support flag on the child elements of qualification only appears in the Differential and not in the Snapshot produced by IG Publisher. An implementer shall interpret the profile as having must support set on the child elements of qualification (i.e. qualification.identifier, qualification.code, qualification.period, qualification.issuer).</td>
        <td>See Zulip <a href="https://chat.fhir.org/#narrow/stream/179177-conformance/topic/More.20about.20Slicing">More about Slicing</a> stream</td>
  </tr>
  <tr>
        <td>qualification.code (Australian localisation)</td>
        <td>Work is underway to provide terminology for Australian qualifications. This work is expected to be available in an R4 variant of this profile.</td>
        <td>See GitHub issue <a href="https://github.com/hl7au/au-fhir-base/issues/314">au-practitioner :: Add ValueSet for Qualification.code to suit Australian Localisation</a></td>
  </tr>
  <tr>
        <td>Constraint presentation</td>
        <td>The full set of constraints (i.e. invariants) defined in this profile are only presented in the Detailed Descriptions tab or the raw representation (e.g. XML) of the profile. The Differential Table only presents constraints introduced in this profile in addition to the constraints present in the base profile and base resource. The Snapshot Table only presents the constraints visible in the Differential Table and additionally presents those constraints set in slices in the base profile.</td>
        <td>See Zulip <a href="https://chat.fhir.org/#narrow/stream/179252-IG-creation/topic/Derived.20profile.20snapshot.20missing.20upstream.20invariants">Derived profile snapshot missing upstream invariants</a> stream</td>
  </tr>
    <tr>
        <td>Practitioner.name</td>
        <td>The Snapshot table presents data type profile (HumanNameBase) definition "A human's name with the ability to identify parts and usage." rather than core element (Practitioner.name) definition "The name(s) associated with the practitioner.".</td>
        <td>See Zulip <a href="https://chat.fhir.org/#narrow/stream/179252-IG-creation/topic/core.20element.20definitions.20overwritten.20by.20IG.20Publisher/near/180005819">Core element definitions overwritten by IG Publisher</a> stream</td>
  </tr>
 </tbody>
</table>