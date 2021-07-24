"# SCA-Cloud-School-Application" 
# Submission #

Firstly, my github repository can be assumed as where my code is written and the jenkins server acts as a pipeline to get that code onto the world wide web. The Jenkinsfile is checked into source control and provides an audit trail for that process. An audit trail essentially means that the pipeline creates a footprint that can always be checked and monitored for errors.
<p> Every time I initiate a git command  such as git add ., git commit -m and git push on the cmd line interface on my computer, this means I'm initiating a push of any changes I've made to my code in my github repository to the jenkins server and jenkins receives those changes using the jenkins file which is checked into source control.</p>

## Pipeline Stages ##
### Build ###
<p>The build step builds and packages the code dependencies, including web assets present in the code in my repository on github, to be deployed down the pipeline. The build stage can also be seen as running the tests present in my code.</p>

### Test ###
<p>The test step is a way of ensuring that the programs present in my repository on github behave as I expect them to when run and is seen as I expect the end user to see it. This essentially means that the tests present in my build stage are being executed. </p>

### Deploy ###
The deploy step sounds basically as it is. It deploys or pushes the code to a production system which in this case is the jenkins server. The deploy stage will only execute assuming the previous stages like build and test were completed successfully.

## Jenkins Pipeline Syntax##

### Source (Echo) ###
The Echo command outputs the strings it is being passed as arguments and here is being used as the source part of my pipeline.

### Steps ###
The steps command here is basically indicating an increment and as previously mentioned, until each stage or step is completed, the other does not run. The most fundamental part of a pipeline is the "step". Steps tells Jenkins what to do.

### Pipeline ###
The pipeline is a block which contains my steps or assignment statements. Enclosed within this block is my declarative pipeline. 

### Agent ###
The “agent” section configures on which nodes the pipeline can be run. Specifying “agent any” means that Jenkins will run the job on any of the available nodes, meaning it executes the pipeline on any available agent. Simply put, the agent section specifies where the entire pipeline or a specific stage, will execute in the Jenkins environment depending on where the agent section is placed.

### Stage ###
The stage section is where the bulk of the "work" described by a pipeline will be located. At a minimum, it is best for stages to contain at least one stage directive for each discrete part of the continuous delivery process, such as Build, Test, and Deploy. This can be observed in my jenkins file. The stages section will typically follow directives such as agent. This can also be seen in my jenkins file.



## Jenkins Username and Password ##
<p>Username: scajenkinsid</p>
<p>Password: scajenkinsid</p>