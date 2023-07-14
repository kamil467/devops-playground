### Best Pratcies for Branch Management and Devops Practices updated main--- update -- update

#### Main Branch Startegy 
 - features and bugs fixes should go as pull request via sperate branhces ( feature branches or topics)
 - Branch protection policies
 - Always update to date. bxxbbfg
 - No Build errors thid

#### Release Branch Strategy
 - Create release branch once branch is deployed in production or when it close to release verssion
 - separare bug fix / feature branch should be created for release branches
 - `periodically release branch should be merged back to main branch`
 
 ##### port changes into main branch from release branch
       - Create a new feature branch off the main branch to port the changes.
       - Cherry-pick the changes from the release branch to your new feature branch.
       - Merge the feature branch back into the main branch in a second pull request.
       
 #### Tags for release
  - If we use separate branches for release then tags are not neccessary.
  - 

#### Update Workflow Run Name:
- Link : https://github.blog/changelog/2022-09-26-github-actions-dynamic-names-for-workflow-runs/
- It will be easier if we follow comman naming pattern for work flow run
-  Naming Convention would be Release-{incremental}
-  Also it is easy to promote specific release to deployment when required

####  Version :
- .version file should keep in repo
- Version= {MAJOR, MINOR, PATCH/BUILD}
- whenever new build triggered for main branch from pull request , this should increase the build OR patch number
- feature level changes - we should increase the minor version
- breaking changes - it will be incremental of Major version
- run-name for workflow can follow version number of application
