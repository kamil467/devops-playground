### Best Pratcies for Branch Management and Devops Practices

#### Main Branch Startegy 
 - features and bugs fixes should go as pull request via sperate branhces ( feature branches or topics)
 - Branch protection policies
 - Always update to date.
 - No Build errors

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
