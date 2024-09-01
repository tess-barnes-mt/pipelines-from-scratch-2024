# 6 - build an internal app - more securely

## Instructions
There is a node app provided in the `internal-app` folder. It gets all its dependencies from a private registry you need access to.

Access is authenticated and authorized by a github PAT. These tokens should be short lived and not shared. We have been told not to commit these secrets into version control in apps or pipeline configuration so need to store them in a github secret instead.

We need a pipeline to checkout the code, install the private dependencies, and run the tests.

We would like the pipeline to run on each push to `main` and also to be triggered manually

- Create a new **short-lived** [CLASSIC Personal Access Token](https://github.com/settings/tokens/new?scopes=read:packages) in github with read:packages permissions and copy the value
- Update the token in the `.npmrc` file with an environment variable reference.
- Create the configuration for the pipeline in the `07-internal-app-secure-build.yaml` file including name, trigger, and job that runs on ubuntu-latest.
- Add steps to the job which check out the code, support the node environment and run the necessary commands.
- Move the config file into `.github/workflows` folder and commit & push your code.
- Use the github web interface to find the pipeline and check the logs
- What went wrong?
- Add your PAT value to a github secret for your repository
- Tigger a manual build of the pipeline and check it now succeeds
- Disable the pipeline
- Invalidate your github PAT

## Questions (write your answers in the notes section):
- Which part of this is pipeline is still not ideal and why?

## References
Github secrets: [Set for a repository](https://docs.github.com/en/actions/security-for-github-actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-a-repository)

Using environment variables in github workflows: [Github docs](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/store-information-in-variables)

## Hints
- Check which folder the commands need to run in
- Check the version of node for the project in the `.nvmrc` file
- Check the available runnable npm `scripts` in the `package.json` file
- Check the docker deep dive course for an example of environment variable references in the `.npmrc` file

## Notes

