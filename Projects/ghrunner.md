# Self Hosted GitHub Runner

<img src="../Images/github-mark-white.png" alt="Github Logo">

Image by (https://github.com) (C)

## About

This project was part of the migration to Github and to assist the team in creating a more gitOps style workflows.

# Roles

My Role was to create virtual machines in each datacentre location and to allow workflows to be directed to a specific datacentre.

The runner was created using docker so the runners could be ephemeral if needed. The idea for this approach came from [testdriven.io ](https://testdriven.io/blog/github-actions-docker/) "Deploying Self-Hosted GitHub Actions Runners with Docker"

This made it easier to manage the configuration of the runner with code within Github and to be able to run the build workflow on itself to push new containers to github container registery.

The dockerfile had to be tweaked to also be able to run docker-in-docker (dind) and additional tweaking had to be made to have docker compose profiles for building for different environments.

# Difficulties

The most difficult part of this task was to work out how to get docker in docker working and to automate the build and redeploy workflow.

# Achievements

Created a working container image that can be used to run github action runner on a machine within docker, that can build docker images push new images to ghcr using github actions.

[Home](../index.md)
