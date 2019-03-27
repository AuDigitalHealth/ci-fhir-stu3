<html>
<title>DB Style</title>
<style>
#DbTbl {font-family:Calibri; color:#777;}
#tabNav {border-bottom:5px solid #69f;}
#tabNav ul {margin:0; padding:0;}
#tabNav ul li {list-style:none; display:inline-block;margin:0; padding:0;}
#tabNav a {	display:inline-block;
			margin:0; 
            padding:10px;
            text-decoration:none;
            border:1px solid #ccc; 
            border-bottom:none; 
            border-top-left-radius:15px; 
            background-color:#009;
            color:white; 
            foint-weight:bold; 
            font-size:1.2em;
            transition-duration: 0.5s;}            
#tabNav a:hover {background-color:#36e;}
#tabNav a.currentNavLink {background-color:#69f; cursor:default;}
.hidden {display:none;}

.verticalText {writing-mode: vertical-rl;font-size: 1.1em;}

.contntTbl { border:none;
  				border-collapse: collapse;
                width: 100%;}
.contntTbl td, .contntTbl th, th.rowTitle  {	border:1px solid #ccc; 
									border-style: solid none; 
                                    padding:10px 20px 10px 5px;}
th.rowTitle { background-color:#eee;} 
.contntTbl a {text-decoration: none; color:#69f;}
.contntTbl a:hover {text-decoration: underline; color:#009;}
.contntTbl ul {margin:0;}
.contntTbl ul li {margin:5px;}

</style>
<body>
<div class="col-12">

<p>Profiles</p>

<div style="border-right-style: none;" id="tabs">
   <div style="border-right-style: none;" id="tabs">
            <ul>
                <li><a href="#tabs-1">Categorized</a></li>
                <li><a href="#tabs-2">Alphabetical</a></li>
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
                    <tr class="frm-contents">
                        <td class="frm-set">
                            <ul class="frm-set">
                                    <li><a href="#"></a></li>
                                    <li><a href="#"></a></li>
                                    <li><a href="#"></a></li>
                                    <li><a href="#"></a></li>    
                                </ul>
                            </td>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-set">
                                <ul>
                                    <li><a href="StructureDefinition-composition-shs-1.html">Composition (Shared Health Summary)</a></li>
                                    <li><a href="#"></a></li>
                                    <li><a href="#"></a></li>
                                    <li><a href="#"></a></li>    
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
                                <li><a href="StructureDefinition-practitioner-ident-1.html">Practitioner (Practitioner with Mandatory Identifier)</a></li>
                                <li><a href="StructureDefinition-practitionerrole-withpractitionerident-1.html">PractitionerRole (Practitioner Role with Practitioner with Mandatory Identifier)</a></li>
                                <li><a href="StructureDefinition-relatedperson-dh-base-1.html">Base RelatedPerson</a></li>
                            </ul>
                        </ul>
                        </td>
                       <td class="frm-set">
                            <ul class="frm-set">
                                <li><a href="StructureDefinition-organization-dh-base-1.html">Organization (Base Organization)</a></li>
                            </ul>
                        </td>
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
                        <td class="frm-set"><ul class="frm-set">
                            <li><a href="StructureDefinition-allergyintolerance-summary-1.html">AllergyIntolerance (Summary Statement of Allergy or Intolerance)</a></li>
                            <li><a href="StructureDefinition-condition-summary-1.html">Condition (Summary Statement of Condition)</a></li>
                            <li><a href="StructureDefinition-procedure-summary-1.html">Procedure (Summary Statement of Known Procedure)</a></li>
                       </ul></td>
                        <td class="frm-null"/>
                        <td class="frm-null"/>
                        <td class="frm-set"><ul class="frm-set">
                            <li><a href="StructureDefinition-medicationstatement-summary-1.html">MedicationStatement (Summary Statement of Known Medicine)</a></li>
                            <li><a href="StructureDefinition-immunization-summary-administration-1.html">Immunization (Summary Statement of Administered Vaccine)</a></li>
                        </ul></td>
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
                    <tr class="frm-contents">
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
                    <tr class="frm-contents">
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
      <th>Item</th>
      <th>Base 1</th>
      <th>Base 2</th>
    </tr>
    <tr>
      <td><a href="StructureDefinition-composition-shs-1.html">Composition (Shared Health Summary)</a></td>
      <td>dhjk kljklsa kljads k</td>
      <td>gkh jjjk </td>
    </tr>
    <tr>
      <td><a href="StructureDefinition-patient-dh-base-1.html">Patient (Base Patient)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>
     <tr>
      <td><a href="StructureDefinition-patient-ident-1.html">Patient (Patient with Mandatory Identifier)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>
    <tr>
      <td><a href="StructureDefinition-patient-ihi-1.html">Patient (Patient with Mandatory IHI)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>
        <tr>
      <td><a href="StructureDefinition-practitioner-dh-base-1.html">Practitioner (Base Practitioner)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>
    <tr>
      <td><a href="StructureDefinition-practitioner-ident-1.html">Practitioner (Practitioner with Mandatory Identifier)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>
        <tr>
      <td><a href="StructureDefinition-practitionerrole-withpractitionerident-1.html">PractitionerRole (Practitioner Role with Practitioner with Mandatory Identifier)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>
    <tr>
      <td><a href="StructureDefinition-relatedperson-dh-base-1.html">Base RelatedPerson</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr> 
   <tr>
      <td><a href="StructureDefinition-organization-dh-base-1.html">Organization (Base Organization)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr> 
   <tr>
      <td><a href="StructureDefinition-allergyintolerance-summary-1.html">AllergyIntolerance (Summary Statement of Allergy or Intolerance)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>    
    <tr>
      <td><a href="StructureDefinition-condition-summary-1.html">Condition (Summary Statement of Condition)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>   
     <tr>
      <td><a href="StructureDefinition-procedure-summary-1.html">Procedure (Summary Statement of Known Procedure)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>     
     <tr>
      <td><a href="StructureDefinition-medicationstatement-summary-1.html">MedicationStatement (Summary Statement of Known Medicine)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>  
         <tr>
      <td><a href="StructureDefinition-immunization-summary-administration-1.html">Immunization (Summary Statement of Administered Vaccine)</a></td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>  

  
  </table>
</div>

<script>
function showcontnt(clickedLink, divId)
{
	var contntDivs = document.getElementsByClassName("contnt");
  	for (var i = 0; i < contntDivs.length; i++) 
  	{
    	(contntDivs[i].id == divId)? 
        	contntDivs[i].classList.remove('hidden') : contntDivs[i].classList.add('hidden');            
  	}
    
    links = document.getElementById('tabNav').getElementsByTagName('a');
   
    for (var j = 0; j < links.length; j++) 
    {	
    	(links[j] == clickedLink)? 
        	links[j].classList.add('currentNavLink') :	links[j].classList.remove('currentNavLink');
    }    
}
</script>
</div>
</body>
</html>