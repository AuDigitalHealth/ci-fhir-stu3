<!DOCTYPE html>
<html>
<title>DB Style</title>
<style>
#DbTbl {font-family:Calibri; color:#777;margin-left: 0px;}
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

.contentTbl { border:none;
  				border-collapse: collapse;
                width: 100%;}
.contentTbl td, .contentTbl th, th.rowTitle  {	border:1px solid #ccc; 
									border-style: solid none; 
                                    padding:10px 20px 10px 5px;}
th.rowTitle { background-color:#eee;} 
.contentTbl a {text-decoration: none; color:#69f;}
.contentTbl a:hover {text-decoration: underline; color:#009;}
.contentTbl ul {margin:0;}
.contentTbl ul li {margin:5px;}

</style>
<body>
<div id='DbTbl'>
<div id="tabNav">
  <ul>
    <li><a href="#" onclick="showContent(this, 'Categorised');" class='currentNavLink'>Categorised</a></li>
    <li><a href="#" onclick="showContent(this, 'Tabular');">Tabular</a></li>   
  </ul>
</div>
<div id='Categorised' class='content'>
  <table class='contentTbl'>
   <tr>
    <th rowspan="2" class='rowTitle'><span class='verticalText'>Foundation</span></th>
    <th>Conformance</th>
    <th>Terminology</th>
    <th>Security</th>
    <th>Documents</th>
    <th>Other</th>
   </tr>
   <tr>
    <td>
      <ul>
        <li><a href="#">CapabilityStatement</a></li>
        <li><a href="#">StructureDefinition</a></li>
        <li><a href="#">ImplementationGuide</a></li>
        <li><a href="#">SearchParameter</a></li>    
      </ul>
    </td>
    <td>
      <ul>
        <li><a href="#">CapabilityStatement</a></li>
        <li><a href="#">StructureDefinition</a></li>
        <li><a href="#">ImplementationGuide</a></li>
        <li><a href="#">SearchParameter</a></li>    
      </ul>
    </td>
    <td>
      <ul>
        <li><a href="#">CapabilityStatement</a></li>
        <li><a href="#">StructureDefinition</a></li>
        <li><a href="#">ImplementationGuide</a></li>
        <li><a href="#">SearchParameter</a></li>    
      </ul>
    </td>
    <td>
      <ul>
        <li><a href="#">CapabilityStatement</a></li>
        <li><a href="#">StructureDefinition</a></li>
        <li><a href="#">ImplementationGuide</a></li>
        <li><a href="#">SearchParameter</a></li>    
      </ul>
    </td>
    <td>
      <ul>
        <li><a href="#">CapabilityStatement</a></li>
        <li><a href="#">StructureDefinition</a></li>
        <li><a href="#">ImplementationGuide</a></li>
        <li><a href="#">SearchParameter</a></li>    
      </ul>
    </td>
   </tr>
   <tr>
    <th rowspan="2" class='rowTitle'><span class='verticalText'>Base</span></th>
    <th>Conformance</th>
    <th>Terminology</th>
    <th>Security</th>
    <th>Documents</th>
    <th></th>
   </tr>
   <tr>
    <td>
      <ul>
        <li><a href="#">CapabilityStatement</a></li>
        <li><a href="#">StructureDefinition</a></li>
        <li><a href="#">ImplementationGuide</a></li>
        <li><a href="#">SearchParameter</a></li>    
      </ul>
    </td>
    <td>
      <ul>
        <li><a href="#">CapabilityStatement</a></li>
        <li><a href="#">StructureDefinition</a></li>
        <li><a href="#">ImplementationGuide</a></li>
        <li><a href="#">SearchParameter</a></li>    
      </ul>
    </td>
    <td>
      <ul>
        <li><a href="#">CapabilityStatement</a></li>
        <li><a href="#">StructureDefinition</a></li>
        <li><a href="#">ImplementationGuide</a></li>
        <li><a href="#">SearchParameter</a></li>    
      </ul>
    </td>
    <td>
      <ul>
        <li><a href="#">CapabilityStatement</a></li>
        <li><a href="#">StructureDefinition</a></li>
        <li><a href="#">ImplementationGuide</a></li>
        <li><a href="#">SearchParameter</a></li>    
      </ul>
    </td>
    <td>  	
    </td>
   </tr>
  </table>
</div>
<div id='Tabular' class='content hidden' >
  <table class='contentTbl'>
    <tr>
      <th>Item</th>
      <th>Base 1</th>
      <th>Base 2</th>
    </tr>
    <tr>
      <td>ghghjgjgjgjhgjhg hjhjhjkjkhjkh</td>
      <td>dhjk kljklsa kljads k</td>
      <td>gkh jjjk </td>
    </tr>
    <tr>
      <td>kjkdajkl</td>
      <td>sjahkh in asdhjkhk</td>
      <td>hgasjdgja kj haJKHJH JK</td>
    </tr>
  </table>
</div>
<script>
function showContent(clickedLink, divId)
{
	var contentDivs = document.getElementsByClassName("content");
  	for (var i = 0; i < contentDivs.length; i++) 
  	{
    	(contentDivs[i].id == divId)? 
        	contentDivs[i].classList.remove('hidden') : contentDivs[i].classList.add('hidden');            
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