# Sprint 4

## Create Releases of your semester project: 

You can create a "release" of your repository using a URL `/releases` at the end of your repository url, like this: [https://github.com/chaoss/augur/releases](https://github.com/chaoss/augur/releases)
    - Tag the version
    - Give it a title
    - Provide a short description
    - Click the "Publish Release" button. This will create a zipped file of the current version of your primary branch, "Production" (or if you named it something else, that branch)

## Key Deadlines 

    - By Friday, December 6th at 11:59pm, create a release of the current status of your semester repository. 
    - By Saturday, December 14th at 11:59pm, create a release of the final version of your repository. 

## Due December 5th 
1. Make sure there is a README.md at the base of the repository that describes Deployment instructions for a [mac, ubuntu or other linux based system] [^1]. [**You do NOT need to repeat any basic, Augur installation instructions.**] [^2]. 
	- Step by step instructions on how to install and run your work. 
        - Include any dependencies. 
        - This will almost certainly entail having somebody try to install it from scratch on a computer you have not been working on; or at least to run it in a new clone folder, using a new python virtual environment. 
    - List what code you modified or created. 
        - If you modified specific existing files, list them. 
        - If you created an entirely new repository that reads API endpoints, state that. 
        - If you created new directories, state what they are, and what's in them. 
        - This must be complete. Look at your commit log on GitHub. Everything committed since the start of the repository is a good checklist. At the command line you can use `git log`
    - Completeness: Your repository should be deployable **without** dependencies on endpoints or data stored on a server that isn't one of the endpoint servers I shared with you. 
    - Describe how you tested your work. 
        - APIs should have pytest code that follows Augur's pattern
        - Front end should have scripts a user would follow to see if its working. 
        - System integration, such as front end talking to an API will be covered by the above. 
        - Individual projects will check with me to confirm. Usually this is simply a pull request description into the Augur repository at https://github.com/chaoss/augur and the execution of the pull request. 
    - **Rubric for Evaluation of README.md**: Caleb and I can clone your repository and run the system by following instructions.
2. All team members must be in class on Tuesday, December 3rd, to work together to assemble item 1, AND, prepare a walk around demo of your system for class on Thursday, December 5th. 
    - You will have the demo working on one laptop
    - Each member of the team will host the demo for 20 minutes
    - During the other 40 minutes of demo time, everyone will walk around and write down feedback and rankings for what each team delivered. 
    - **Rubric for Walkaround** : Active presence. Submission of brief, thoughtful, pro and con feedback for each team's project using a form provided in class by Dr. Goggins.  
    - After class, each person will turn in their feedback to Dr. Goggins and Caleb for each project. 
3. Modify your project to incorporate feedback from Sprint's 2 & 3. (Due by Saturday, December 14th, 11:59pm). 
    - Modification can include the creation of a specific issue on your repository that describes the work that needs to be done in sufficient detail that another developer could complete the work or 
    - Modification can include a change to the codebase through a pull request.  


 
[^1]: If you have Windows deployment instructions, since one project actually built these, that's ok. But if yours is not that project keep in mind that one person created and tested a LOT of specific instructions for Windows deployment, and you will in all likelihood have to do all THAT work again.
[^2]: Assume we have an instance installed that, if needed, we will connect your repository's work to. Everything we need to configure is in the `augur.config.json` file and we have one for testing student projects. If you have `.json` files stored in your deployment, please note what endpoints they were generated from.