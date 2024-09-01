# 5 - build an internal app

## Instructions
There is a basic node app provided in the `internal-app` folder. It gets all its dependencies from a private registry you need access to.

Access is authenticated and authorized by a github PAT. These tokens should be short lived and not shared.

We need a pipeline to checkout the code, install the private dependencies, and run the tests.

We would like the pipeline to run on each push to `main`

- Create the configuration for the pipeline in the `06-internal-app-build.yaml` file including name, trigger, and job that runs on ubuntu-latest.
- Add steps to the job which check out the code, support the node environment and run the necessary commands.
- Move the config file into `.github/workflows` folder and commit & push your code.
- Use the github web interface to find the pipeline and check the logs.
- What went wrong?
- Create a **short-lived** [CLASSIC Personal Access Token](https://github.com/settings/tokens/new?scopes=read:packages) in github with read:packages permissions and copy the value
- Update the token in the `.npmrc` file with this value.
- Commit & push your changes
- Use the github web interface to find the pipeline and check the pipeline now succeeds
- Disable the pipeline.
- Invalidate your github PAT

## Questions (write your answers in the notes section):
- Which part of this is pipeline is insecure and why?
- What else could go wrong?

## Hints
- Check which folder the commands need to run in
- Check the version of node for the project in the `.nvmrc` file
- Check the available runnable npm `scripts` in the `package.json` file

## Notes

