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
    This one is meant to fail, a failing pipeline isn't necessarily a bad thing, the failure in this case indicates that there are broken links within the website being checked.

    For workflows/pipelines to run they need to be in a specific folder, in the case of github actions, they need to be in .github/workflows

    Need some specific blocks for our pipeline to work, a name for the pipeline, name: block. A trigger defined in the on: block. What type of VM we want our pipeline to run on, our runner, in a runs-on: block. Finally the steps we want carried out in a steps: block, these are each defined by a dash '-' and must contain a runs: or uses: block.

    YAML is fussy, indentation matters for defining block scope.
