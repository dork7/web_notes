# Github Actions
- Automate software development workflow
- Testing
- Automatic releases

___
## Workflow
- Workflow is a collection of job definition that will be executed concurrently as well as sequentially, when it’s triggered by an event.

To add a workflow in repo **.github/workflows** folder, which will contain workflow files with **.yml** extension.
___

## Events
- An event is anything that can happen on a Github repository. This goes from pushing a code, creating a branch, opening a pull request, and even commenting on an issue.
 

## Jobs
- Jobs can be executed concurrently as well as sequentially
- A job is consists of several steps which will be executed sequentially
- A job is a series of tasks that gets executed in a workflow upon being triggered by an event. Each step is either a script or a Github action.

![Alt text](assets/githubaction-jobs.webp)

## Runners
- Runners are processes on a server that run the workflow when it’s triggered. Each runner is responsible for executing a given job.
Runners are hosted in the cloud but…

___
# Example
~~~
# Define workflow name
name: Docker Image CI

on:
# trigger on push in following branches
  push:
    branches: [ master ,main]
jobs:
  build:
# specify a runner
    runs-on: ubuntu-latest

    steps:
# step: predefined checkout step 
    - uses: actions/checkout@v2

# step:  login to dockerhub
    - name: docker login
    # setting the env variables in ubuntu runner
      env:
        DOCKER_USER: ${{secrets.DOCKER_USER}}
        DOCKER_PASSWORD: ${{secrets.DOCKER_PASSWORD}}
    # running command inside runner
      run: |
        docker login -u $DOCKER_USER -p $DOCKER_PASSWORD 

# step : build the image from the docker file
    - name: Build the Docker image
      run: docker build . --file Dockerfile --tag dork7/python-test
      
# step : push image to docker hun
    - name: Docker Push
      run: docker push dork7/python-test
~~~
