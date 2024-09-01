# 1 - link checker

## Instructions
Take a look at the circle ci pipeline in Madetech's learn repo.
How would you recreate that task in a github action pipeline that was manually triggered? What language environment does it rely on?

- Create the configuration for the pipeline in the `01-link-check.yaml` file including name, trigger, and job that runs on ubuntu-latest.
- Add steps to the job which support the language environment used and run the command.
- Move the config file into `.github/workflows` folder and commit & push your code.
- Use the github web interface to find and start your new pipeline.
- Assuming that there are some broken links on the Madetech Learn website, do you expect the pipeline to pass or fail?

## Notes
