<table class="list" width="100%" cellspacing="4">
<tbody>
  <tr>
    <th>Reference</th>
    <th>Description</th>
    <th>Issue No.</th>
  </tr>
  
  <tr>
        <td>Invariants may not constrain as intended</td>
        <td>Current validation capabilities of the FHIR Validator and IG Publisher do not fully support all expressions defined in the FHIR specification. Invariants using conformsTo() or … have not been able to be confirmed and do not reject resources that are expected to fail.</td>
        <td>???</td>
  </tr>
  
  <tr>
        <td>Element missing Must Support flag</td>
        <td>The tooling (Forge) used to author this profile throws an error when mustSupport is set to true on Patient.deceased.deceasedDateTime.date-accuracy-indicator. </td>
        <td>
            <p>gForge Change Request #17165</p>
            <p><a href="https://gforge.hl7.org/gf/project/fhir/tracker/?action=TrackerItemEdit&tracker_item_id=17165">IG Publisher - Adding Must Support to Patient.deceased.deceasedDateTime.date-accuracy-indicator</a></p>
        </td>
  </tr>

 </tbody>
</table> 


