<html>
	<div id="segment-content" class="segment">  <!-- segment-content -->
	<div class="container">  <!-- container -->
            <div class="row">
            	<div class="inner-wrapper">

<div class="col-12">


<h1>Profiles</h1>
{% include publish-box.html %}
<p>The following profiles form part of this implementation guide:</p>

<div style="border-right-style: none;" id="tabs">
   <div style="border-right-style: none;" id="tabs">
            <ul>
                <li><a href="#tabs-1">Categorized</a></li>
                <li><a href="#tabs-2">Based on</a></li>
            </ul>
            <div id="tabs-1">
                <table width="100%">
                    <tr class="frm-group">
                        <td rowspan="2" class="frm-group rotate"><div>Foundation</div></td>
                        <td class="frm-category">Conformance</td>
                        <td class="frm-category">Terminology</td>
                        <td class="frm-category">Security</td>
                        <td class="frm-category">Documents</td>
                        <td class="frm-category">Other</td>
                    </tr> 
                    <tr class="frm-contents" height="80">
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-set">
                                <ul>
                                    <li><a href="StructureDefinition-composition-docheader-cei-1.html">Composition (Consumer Entered Information Document Header)</a></li>
                                </ul>
                                 <ul>
                                    <li><a href="StructureDefinition-composition-phn-1.html">Composition (Personal Health Notes)</a></li>
                                </ul>
                                <ul>
                                    <li><a href="StructureDefinition-composition-phs-1.html">Composition (Personal Health Summary)</a></li>
                                </ul>
                            </td>
                        <td class="frm-null"/>
                    </tr>
                    <tr class="frm-break"><td colspan="6"/></tr>
                    <tr class="frm-group">
                        <td rowspan="2" class="frm-group rotate"><div>Base</div></td>
                        <td class="frm-category">Individuals</td>
                        <td class="frm-category">Entities</td>
                        <td class="frm-category">Workflow</td>
                        <td class="frm-category">Management</td>
                        <td class="frm-null"/>
                    </tr> 
                    <tr class="frm-contents">
                        <td class="frm-set">
                            <ul class="frm-set">
                                <li><a href="StructureDefinition-patient-dh-base-1.html">Patient (Base Patient)</a></li>
                                <li><a href="StructureDefinition-patient-ident-1.html">Patient (Patient with Mandatory Identifier)</a></li>
                                <li><a href="StructureDefinition-patient-ihi-1.html">Patient (Patient with Mandatory IHI)</a></li>
                                <li><a href="StructureDefinition-practitioner-dh-base-1.html">Practitioner (Base Practitioner)</a></li>  
                                <li><a href="StructureDefinition-relatedperson-dh-base-1.html">RelatedPerson (Base RelatedPerson)</a></li>
                                <li><a href="StructureDefinition-relatedperson-ihi-1.html">RelatedPerson (Related Person with Mandatory IHI)</a></li>
                            </ul>
                       </td>
                       <td class="frm-set">
                            <ul class="frm-set">
                                <li><a href="StructureDefinition-organization-dh-base-1.html">Organization (Base Organization)</a></li>
                                <li><a href="StructureDefinition-organization-ident-1.html">Organization (Organization with Mandatory Identifier)</a></li>
                            </ul>
                        </td>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                    </tr> 
                    <tr class="frm-break"><td colspan="6"/></tr>
                    <tr class="frm-group">
                        <td rowspan="2" class="frm-group rotate"><div>Clinical</div></td>
                        <td class="frm-category">Summary</td>
                        <td class="frm-category">Diagnostics</td>
                        <td class="frm-category">Medications</td>
                        <td class="frm-category">Care Provision</td>
                        <td class="frm-category">Request &amp; Response</td>
                    </tr> 
                    <tr class="frm-contents">
                        <td class="frm-set">
                          <ul class="frm-set">
                            <li><a href="StructureDefinition-allergyintolerance-summary-1.html">AllergyIntolerance (Summary Statement of Allergy or Intolerance)</a></li>
                         </ul>
                       </td>
                      <td class="frm-set">
                         <ul class="frm-set">
                            <li><a href="StructureDefinition-observation-norelevantfinding-1.html">Observation (Assertion of No Relevant Finding)</a></li>
                          </ul>
                       </td>
                      <td class="frm-set">
                        <ul class="frm-set">
                            <li><a href="StructureDefinition-medicationstatement-summary-1.html">MedicationStatement (Summary Statement of Known Medicine)</a></li>
                        </ul>
                        </td>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                    </tr> 
                    <tr class="frm-break"><td colspan="6"/></tr>
                    <tr class="frm-group">
                        <td rowspan="2" class="frm-group rotate"><div>Financial</div></td>
                        <td class="frm-category">Support</td>
                        <td class="frm-category">Billing</td>
                        <td class="frm-category">Payment</td>
                        <td class="frm-category">General</td>
                        <td class="frm-null"/>
                    </tr> 
                    <tr class="frm-contents" height="80">
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                    </tr> 
                    <tr class="frm-break"><td colspan="6"/></tr>
                    <tr class="frm-group">
                        <td rowspan="2" class="frm-group rotate"><div>Specialized</div></td>
                        <td class="frm-category">Public Health &amp; Research</td>
                        <td class="frm-category">Definitional Artifacts</td>
                        <td class="frm-category">Clinical Decision Support</td>
                        <td class="frm-category">Quality Reporting</td>
                        <td class="frm-category">Testing</td>
                    </tr> 
                    <tr class="frm-contents" height="80">
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                    </tr> 
                    <tr class="frm-break"><td colspan="6"/></tr>
                </table>
</div>

 </div>
  <div id="tabs-2">

<table width="100%">
    <tr>
      <th>Implementation guide profile</th>
      <th>Implementation guide profile base</th>
      <th>FHIR base resource</th>
    </tr>
    <tr>
        <td><a href="StructureDefinition-allergyintolerance-summary-1.html">AllergyIntolerance (Summary Statement of Allergy or Intolerance)</a></td>
        <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-allergyintolerance.html">AU Base Allergy Intolerance</a></td>
        <td><a href="http://hl7.org/fhir/STU3/allergyintolerance.html">AllergyIntolerance </a></td>
    </tr>    
    <tr>
       <td><a href="StructureDefinition-composition-docheader-cei-1.html">Composition (Consumer Entered Information Document Header)</a></td>
       <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-composition.html">AU Base Composition</a></td>
       <td><a href="http://hl7.org/fhir/STU3/composition.html">Composition</a></td>
    </tr>
    <tr>
       <td><a href="StructureDefinition-composition-phn-1.html">Composition (Personal Health Notes)</a></td>
       <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-composition.html">AU Base Composition</a></td>
       <td><a href="http://hl7.org/fhir/STU3/composition.html">Composition</a></td>
    </tr>
     <tr>
        <td><a href="StructureDefinition-composition-phs-1.html">Composition (Personal Health Summary)</a></td>
        <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-composition.html">AU Base Composition</a></td>
        <td><a href="http://hl7.org/fhir/STU3/composition.html">Composition</a></td>
    </tr>    
    <tr>
        <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-dosage.html">Dosage (AU Base Dosage)</a></td>
        <td><a href="http://hl7.org/fhir/STU3/dosage.html#Dosage">Dosage</a></td>
        <td><a href="http://hl7.org/fhir/STU3/dosage.html#Dosage">Dosage</a></td>
    </tr>    
    <tr>
        <td><a href="StructureDefinition-humanname-dh-base-1.html">HumanName (Base HumanName)</a></td>
        <td><a href="http://hl7.org/fhir/STU3/datatypes.html#HumanName">HumanName</a></td>
        <td><a href="http://hl7.org/fhir/STU3/datatypes.html#HumanName">HumanName</a></td>
    </tr>
    <tr>
        <td><a href="StructureDefinition-medicationstatement-summary-1.html">MedicationStatement (Summary Statement of Known Medicine)</a></td>
        <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-medicationstatement.html">AU Base Medication Statement</a></td>
        <td><a href="http://hl7.org/fhir/STU3/medicationstatement.html">MedicationStatement</a></td>
    </tr>  
    <tr>
        <td><a href="StructureDefinition-observation-norelevantfinding-1.html">Observation (Assertion of No Relevant Finding)</a></td>
        <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-norelevantfinding.html">AU Assertion of No Relevant Finding</a></td>
        <td><a href="http://hl7.org/fhir/STU3/observation.html">Observation</a></td>
    </tr>
    <tr>
        <td><a href="StructureDefinition-organization-dh-base-1.html">Organization (Base Organization)</a></td>
        <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-organisation.html">AU Base Organization</a></td>
        <td><a href="http://hl7.org/fhir/STU3/organization.html">Organization</a></td>
    </tr> 
    <tr>
        <td><a href="StructureDefinition-organization-ident-1.html">Organization (Organization with Mandatory Identifier)</a></td>
        <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-organisation.html">AU Base Organization</a></td>
        <td><a href="http://hl7.org/fhir/STU3/organization.html">Organization</a></td>
   </tr> 
   <tr>
      <td><a href="StructureDefinition-patient-dh-base-1.html">Patient (Base Patient)</a></td>
      <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-patient.html">AU Base Patient</a></td>
      <td><a href="http://hl7.org/fhir/STU3/patient.html">Patient</a></td>
    </tr>
    <tr>
      <td><a href="StructureDefinition-patient-ident-1.html">Patient (Patient with Mandatory Identifier)</a></td>
      <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-patient.html">AU Base Patient</a></td>
      <td><a href="http://hl7.org/fhir/STU3/patient.html">Patient</a></td>
    </tr>
    <tr>
      <td><a href="StructureDefinition-patient-ihi-1.html">Patient (Patient with Mandatory IHI)</a></td>
      <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-patient.html">AU Base Patient</a></td>
      <td><a href="http://hl7.org/fhir/STU3/patient.html">Patient</a></td>
    </tr>
    <tr>
      <td><a href="StructureDefinition-practitioner-dh-base-1.html">Practitioner (Base Practitioner)</a></td>
      <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-practitioner.html">AU Base Practitioner</a></td>
      <td><a href="http://hl7.org/fhir/STU3/practitioner.html">Practitioner </a></td>
    </tr>
    <tr>
       <td><a href="StructureDefinition-relatedperson-dh-base-1.html">RelatedPerson (Base RelatedPerson)</a></td>
       <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-relatedperson.html">AU Base RelatedPerson</a></td>
       <td><a href="http://hl7.org/fhir/STU3/relatedperson.html">RelatedPerson </a></td>
    </tr> 
    <tr>
       <td><a href="StructureDefinition-relatedperson-ihi-1.html">RelatedPerson (Related Person with Mandatory IHI)</a></td>
       <td><a href="https://build.fhir.org/ig/hl7au/au-fhir-base-stu3/StructureDefinition-au-relatedperson.html">AU Base RelatedPerson</a></td>
       <td><a href="http://hl7.org/fhir/STU3/relatedperson.html">RelatedPerson </a></td>
    </tr> 

</table>
  </div>
				</div>  <!-- /inner-wrapper -->
            </div>  <!-- /row -->
        </div>  <!-- /container -->
        
    </div>  <!-- /segment-content -->

	<div id="segment-post-footer" class="segment hidden">  <!-- segment-post-footer -->
		<div class="container">  <!-- container -->
		</div>  <!-- /container -->
	</div>  <!-- /segment-post-footer -->
    
      <!-- JS and analytics only. -->
      <!-- Bootstrap core JavaScript
================================================== -->
  <!-- Placed at the end of the document so the pages load faster -->
<script src="./assets/js/jquery.js"> </script>     <!-- note keep space here, otherwise it will be transformed to empty tag -> fails -->
<script src="./dist/js/bootstrap.min.js"> </script>
<script src="./assets/js/respond.min.js"> </script>

<script src="./assets/js/fhir.js"> </script>

  <!-- Analytics Below
================================================== -->


<script src="external/jquery/jquery.js"> </script>
<script src="jquery-ui.min.js"> </script>
<script>
try {
  var currentTabIndex = sessionStorage.getItem('fhir-resourcelist-tab-index');
}
catch(exception){
}

if (!currentTabIndex)
  currentTabIndex = '0';

$( '#tabs' ).tabs({
         active: currentTabIndex,
         activate: function( event, ui ) {
             var active = $('.selector').tabs('option', 'active');
             currentTabIndex = ui.newTab.index();
             document.activeElement.blur();
             try {
               sessionStorage.setItem('fhir-resourcelist-tab-index', currentTabIndex);
             }
             catch(exception){
             }
         }
     });
</script>
</div>
</div>
</html>




