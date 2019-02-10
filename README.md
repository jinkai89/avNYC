#Autonomous Vehicle Simulation For New York City. 

This repository allows to run an autonomous mobility-on-demand scenario using the amodeus library (https://github.com/idsc-frazzoli/amodeus).


## Getting Started

- You may work on a Linux, Mac or Windows OS with a set of different possible IDEs. The combination Ubuntu, Java 8, Eclipse has worked well. 
- Install Java SE Development Kit (version 8, or above)
- Install Apache Maven
- Install IDE (ideally Eclipse Oxygen or Photon)
- Install GLPK and GLPK for Java (Ensure you install compatible versions, e.g. [here](http://glpk-java.sourceforge.net/gettingStarted.html))
	- Prerequisites are: GCC, Libtool, Swig and Subversion
- Install Git and connect to GitHub with [SSH](https://help.github.com/articles/connecting-to-github-with-ssh/)

The code format of the `amod` repository is specified in the `amodeus` profile that you can import from [amodeus-code-style.xml](https://raw.githubusercontent.com/idsc-frazzoli/amodeus/master/amodeus-code-style.xml).

## Installation guidelines for amod repository

1. Clone amod
2. Import to eclipse as existing maven project (Package Explorer->Import) using the pom.xml in the top folder of this repository.
3. Set up Run Configurations for: (ScenarioPreparer; ScenarioServer; ScenarioViewer), chose the Working Directory to be the top Simulation Folder directory. You can get a sample simulation scenario at http://www.idsc.ethz.ch/research-frazzoli/amodeus.html
4. Adjust the simulation settings in the 3 config files: av.xml for av fleet values (e.g. number vehicles), AmodeusOptions.properties for AMoDeus settings (e.g. max number of people) and config.xml for Matsim settings (e.g. output directory). 
5. Add JAVA VM arguments if necessary, e.g., `-Xmx10000m` to run with 10 GB of RAM and `-Dmatsim.preferLocalDtds=true` to prefer the local Dtds. 
6. Run the `ScenarioPreparer` as a Java application: wait until termination
7. Run the `ScenarioServer` as a Java application: the simulation should run
8. Run the `ScenarioViewer` as a Java application: the visualization of the scenario should open in a separate window

