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
 </tbody>
</table>


<p>Provenance.entity.agent is a reference to another element (Provenance.agent) but as the target element has been sliced into two slices, it appears that the reference cannot be found.
An XML example incorporating a Provenance.entity.agent passed validation.</p>

<p>Elements such as 'who[x]' or 'what[x]' get renamed if there is only a single choice of data types. However, in some elements the renaming differs and what should be rendered as 'whoReference:whoReference', is rendered as 'who[x]:whoReference'. The issue has been raised with the Profile Editor software provider (Forge/Firely) who have acknowledged this as a bug and are attending to a fix.</p>
