## **DEPLOYMENT DONE ON THURSDAY 30TH MARCH, 2023**

For every new project to be deployed, the first step to take is to clone everything needed for the app on to my local machine.

Next is to create a new branch to do the deployment.

In the config file, the first  secton is the orbs  for slack. This is to implement event-based notifications across all of your CI/CD pipelines. It is important to check circleci to confirm that any orbs to be used is verified of their platform to avoid any security issues.

For the doocker image, always make use of a consistent image i.e. python image for a python app and a node.js image for a node.js app



The first job is a build job and the first step is to checkout.

**Note:** The git checkout command lets you navigate between the branches created by git branch. Checking out a branch updates the files in the working directory to match the version stored in that branch, and it tells Git to record all new commits on that branch. Think of it as a way to select which line of development you’re working on.

Next is the build-image section where the docker image is built and pushed to the container registry (in this case Google Container Registry (GCR))


For the environmental variables, we used Context on CircleCI. So. instead of adding new env for every new projects, we store the needed envs in the CircleCI context and simply refrence or call it whenever it is needed for any projects.

