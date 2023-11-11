##### build the project

    gradle build
	
	
Exercises for Module "Artifact Repository Manager with Nexus"

You and other teams in 2 different projects in your company see that they have many different small projects, including the NodeJS application you built in the previous step, the java-gradle helper application and so on. You discuss and decide it would be a good idea to be able to keep all these app artifacts in 1 place, where each team can keep their app artifacts and can access them when they need.
So they ask you to setup Nexus in the company and create repositories for 2 different projects.

EXERCISE 1: Install Nexus on a server

EXERCISE 2: Create npm hosted repository
For a Node application you:
create a new npm hosted repository with a new blob store

EXERCISE 3: Create user for team 1
You create Nexus user for the project 1 team to have access to this npm repository

EXERCISE 4: Build and publish npm tar
You want to test that the project 1 user has correct access configured. So you:
build and publish a nodejs tar package to the npm repo

EXERCISE 5: Create maven hosted repository
For a Java application you: create a new maven hosted repository

EXERCISE 6: Create user for team 2
You create a Nexus user for project 2 team to have access to this maven repository

EXERCISE 7: Build and publish jar file
You want to test that the project 2 user has the correct access configured and also upload the first version. 
So: build and publish the jar file to the new repository using the team 2 user.

Use the java-app application from the Build Tools module

EXERCISE 8: Download from Nexus and start application
Create new user for droplet server that has access to both repositories
On a digital ocean droplet, using Nexus Rest API, fetch the download URL info for the latest NodeJS app artifact
Execute a command to fetch the latest artifact itself with the download URL
Untar it and run on the server!

# fetch download URL with curl
curl -u {user}:{password} -X GET 'http://{nexus-ip}:8081/service/rest/v1/components?repository={node-repo}&sort=version'


