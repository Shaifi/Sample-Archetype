# Create Customised Maven Archetype
By following the below steps you can create your own customised maven archetype and use them as base for your own projects. You can clone my project for reference as well.

## Steps
1. Create a simple maven project with groupId, artifactId as well as versionId and packaging as 'maven-archetype' that you want for your archetype.
2. Create src > main > resources> META-INF > maven > archetype-metadata.xml and define the properties that you want about the archetype.(For reference use the file in project and rename the name parameter as same as your archetype artifact id )
3. Create src > main > resources > archetype-resources. In this replicate the structure that you want for your project.
4. use mvn install to create the archetype and install the archetype in your maven repository
5. Go to the folder where you want to create your own project and run the following command in the terminal :mvn archetype:generate  
 -DarchetypeGroupId=com.bansal
 -DarchetypeArtifactId=sample-archetype 
 -DarchetypeVersion=1.0
 -DgroupId=com.test   
 -DartifactId=demo
 where com.bansal is my archetypeGroupId, sample-archetype is my archetypeArtifactId, 1.0 is my archetypeVersionId, com.test is my required project GroupId, demo is my required project(Change these values as per your requirement)
P.S. Place sample files in your directories otherwise your packages will not get created.
