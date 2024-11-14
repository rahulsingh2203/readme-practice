
# About the action script
---
This is a documented guide to understand the actions script written within this repository. It will also help you to understand the why factor involved in the script since there are ample of methodologies to execute a particular task.

### Workflow:
There are 2 workflows in the repository, one is for staging environment and other is for production environment.

### Workflow Steps:

Workflow is structured in the following template:
- name
- on
- jobs
  - build
    - steps
  - deploy
    - steps

#### Build

- First of all we use GitHub's own runner where we perform tasks involved in the build job.
- steps include checking out repository, installing application dependencies, generating artifacts and uploading it

#### Deploy

- For this job also, we use GitHub's own runner where we perform task involved in the deploy job.
- steps include, downloading artifacts in runner, establishing connection between runner and remote server, performing file copying, directory creating, deletion snd modification and generating backup using appleboy's ssh and scp actions.
