# 3 - build a basic app

## Instructions
There is a basic node app provided in the `app` folder. It gets all its dependencies publically from nodejs.

We need a pipeline to checkout the code, install the dependencies, prettify the code and run the tests.

We would like the pipeline to run on each push to `main`

- Create the configuration for the pipeline in the `03-app-build.yaml` file including name, trigger, and job that runs on ubuntu-latest.
- Add steps to the job which check out the code, support the node environment and run the necessary commands.
- Move the config file into `.github/workflows` folder and commit & push your code.
- Use the github web interface to find the pipeline and check it has run correctly.

## Hints
- Check which folder the commands need to run in
- Check the version of node for the project in the `.nvmrc` file
- Check the available runnable npm `scripts` in the `package.json` file

## Notes

Each new steps works in a new terminal and so won't keep track of pathing/context for example, one way around this it define a default working directory in a defaults: block to define where we want to run our commands, or to specify within each step wehere we are wanting to run our command.

Github can be quite helpful with it's error messages to help us figure out why our pipeline might be failing

Plugins are our friends! we can specify what environments/dependencies we need to use, like Node for example.

