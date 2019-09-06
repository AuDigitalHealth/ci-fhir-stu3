This section lists known issues with this profile at the time of publishing. We are working on solutions to these issues and encourage comments to help us develop these solutions.
<style>
table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width: 100%;
}

th {
  background-color: #f2f2f2;
}

td, th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
}

</style>

<table>
	<col style="width:20%"/>
	<col style="width:60%"/>
	<col style="width:20%"/>
            <thead>
                <tr>
                    <th>Reference</th>
                    <th>Description</th>
                    <th>Issue No.</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Binding: PBS Medicines Item Codes</td>
                    <td>The PBS Medicines Item Codes value set, originating from the HL7 AU Base Medication profile, is a placeholder resource. Forthcoming work is expected to result in an authoritative value set published in the National Clinical Terminology Service (NCTS) with the following canonical URL: https://healthterminologies.gov.au/fhir/ValueSet/australian-pbs-item-1. Implementers are to make use of the value set served via the NCTS when available.</td>
                    <td><a href="https://confluence.hl7australia.com/pages/viewpage.action?pageId=14582568">Ballot comment FHIRIG-24</a></td>
                </tr>
                <tr>
                    <td>Binding: GTIN for Medicines</td>
                    <td>No expansion is available for this value set using the associated code system published in the HL7 AU Base material. None of the concepts defined by the code system are included in the code system resource. Implementers are expected to have available an expansion that defines what codes are in the value sets to make use of this terminology.</td>
                    <td><a href="https://github.com/hl7au/au-fhir-base-stu3/issues/9">au-fhir-base-stu3/issues/9</a></td>
                </tr>
                <tr>
                    <td>Binding: MIMS Terminology</td>
                    <td>No expansion is available for this value set using the associated code system published in the HL7 AU Base material. None of the concepts defined by the code system are included in the code system resource. Implementers are expected to have available an expansion that defines what codes are in the value sets to make use of this terminology.</td>
                    <td><a href="https://github.com/hl7au/au-fhir-base-stu3/issues/9">au-fhir-base-stu3/issues/9</a></td>
                </tr>
            </tbody>
</table>