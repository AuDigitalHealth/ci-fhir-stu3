<table class="list" width="100%">
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
        <td>The tooling (Forge) used to author this profile throws an error when mustSupport is set to true on Practitioner.qualification.identifier, Practitioner.qualification.code, Practitioner.qualification.period and Practitioner.qualification.issuer. </td>
        <td>
            <p>JIRA Request CIFMM-2161</p>
            <p><a href="https://jira.nehta.net.au/browse/CIFMM-2161">CIFMM-2161</a></p>
        </td>
  </tr>

 </tbody>
</table> 