## Integration Patterns:

Lets look at some architecture patterns for integrating applications. Some of these patterns have been around for a while and some are newer and asociated with the Semantic Web:

#### [File Transfer](http://www.eaipatterns.com/FileTransferIntegration.html)
An application transfers a data file to another application. Two copies of the file exist in two different places! If changes are made how will we know which copy is accurate? Other solutions exist but we could make one application the [Master](https://www.ibm.com/developerworks/community/wikis/home?lang=en#!/wiki/W4108ee665aa0_4201_8931_923a96c3653a/page/Master%20Data%20Management%20Solutions), and only allow write-access to this copy. Changes on Master are pushed to Subordinates.

####[Shared Database](http://www.enterpriseintegrationpatterns.com/SharedDataBaseIntegration.html)
Integrate applications by having them store their data in a single Shared Database. All applications can have write access. Changes to the database might occur close together but this is manageable. 

#### [Messaging](http://www.eaipatterns.com/Messaging.html)
Transfer packets of data between applications frequently. Distributed applications generally store data in different (and often vernacular) formats. Applications must convert data between formats to use the data ([Message Translator](http://www.eaipatterns.com/MessageTranslator.html) pattern). 

#### [IDs as Universally Unique Identifier (UUID)](http://en.wikipedia.org/wiki/Universally_unique_identifier)
Identify a **resource** with a UUID (a long random string of numbers and letters). Distributed applications can uniquely identify the resource without central coordination. To which 'things' does this data resource refer? A Human can read the resource and figure this out (eventually). 

#### [IDs as Uniform Resource Identifiers (URI)](http://en.wikipedia.org/wiki/Uniform_resource_identifier)

Identify a **thing** with a URI (a http address). Distributed applications can uniquely identify the thing without central coordination. Web connected computers can look up the thing. Humans can too. Everyone knows to which 'thing' the information is referring.

####[Query Federation](http://linkeddatabook.com/editions/1.0/#htoc84)


####[UI Components](http://webcomponents.org/)