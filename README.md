"# SCA-Cloud-School-Application" 
# Submission #
Firstly, my github repository can be assumed as where my code is written and the jenkins server acts as a pipeline to get that code onto the world wide web. The Jenkinsfile is checked into source control and provides an audit trail for that process. An audit trail essentially means that the pipeline creates a footprint that can always be checked and monitored for errors.
Every time I initiate a git command  such as git add . and git push on the cmd line interface on my computer, this means I'm initiating a push of any changeas I've made to my code in my github repository to the jenkins server and jenkins receives thouse chanes using the jenkins file which is checked into source control.
The build command generates the web assets present in the programs in my repository on github to be deployed.
The test command is a way of ensuring that the programs present in my repository on github behave as I expect them to when run and is seen as I expect the end user to see it. 
The deploy command sounds basically as it is. It deploys or pushes the code to a production system which in this case is the jenkins server. The deploy satge will only execute assuming the previous stages like build and test were completed successfully.
The Echo command outputs the strings it is being passed as arguments and here is being used as a source part of a pipeline.
The steps command here is basically each increment it goes up by and as previously mensioned until each stage or step is completed, the other does not run.
The “agent” section configures on which nodes the pipeline can be run. Specifying “agent any” means that Jenkins will run the job on any of the available nodes.

## Jenkins Username and Password ##
Username: scajenkinsid
Password: scajenkinsid