# 4 - build a container image

## Instructions
We have a node app we need to build into a container image before deployment.

We need a pipeline that runs a docker command to build and tag the image. To confirm the image has been built we want to see the output of the build history

- Create the configuration for the pipeline in the `04-image-build.yaml` file including name, trigger, and job that runs on ubuntu-latest.
- Add steps to the job which get the code and run the necessary commands.
- Move the config file into `.github/workflows` folder and commit & push your code.
- Use the github web interface to find and start your new pipeline.

## Hints
- Think about which folder the step needs to run commands in
- Refer back to docker-deep-dive for a reminder on the docker commands
- How many plugins or actions do you need to do this? Fewer is better and it may be fewer than you think!

## Notes

