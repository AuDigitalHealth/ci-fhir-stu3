How to build a implementation guide:

Step #1: Use the [IG Publisher](http://wiki.hl7.org/index.php?title=IG_Publisher_Documentation)

Use the following command line:

java - jar [jpath]org.hl7.fhir.igpublisher.jar -ig [path]<doc-type>.json 

where [jpath] is the location of the IG pubisher (from the current build - see downloads), [path] is the folder for your local copy of the repository, and <doc-type> is the name of document type

e.g. java - jar org.hl7.fhir.igpublisher.jar -ig ig-sharedhealthsummary-1.json 

