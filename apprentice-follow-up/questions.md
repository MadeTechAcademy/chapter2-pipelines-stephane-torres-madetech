# Follow up questions

Commit your answers to these questions in your copy

## Part 1
Answer these after a day or two after the course 

1. Which exercise did you find the easiest? and why<br/>
    I found exercise 2 and 4 to be the easiest/easier, after completing exercise 1 and understanding a bit of what the YAML file needs to include and how it needs to be structured to run a job, exercise 2 was just a case of changing the trigger everything else remained the same.
    Exercise 4 became a lot easier when gaining a little bit more understanding the a runner is just a machine that we can plug commands into and that ubuntu has docker out of the box so the pipeline ends up being extremely simple.
2. Which was most difficult? and why<br/>
    I found exercise 1 and 3 to be the harder of the exercises, the idea of plugins and how to use them as well as what different steps, structure and blocks we need in our YAML files to get a pipeline to work to begin with we quite difficult to get along with. Also not knowing what is happening at the end of each step.


## Part 2

After some reflection and perhaps investigation while on your delivery

1. Which pipeline types are used on your delivery?<br/>
    - We have both scheduled and manual pipeline triggers on our delivery, triggering both the creation destruction of sandboxes( creating the app in a development environment). Stages in the pipeline build, tag and publish the app Docker image to AWS ECR, using plugins authored by serveral organisations including AWS and GitHub. Some of these pipelines are reliant on other workflows, something we talked about but not get in to due to time constraints.
2. What techniques are in place that make pipelines more secure on your delivery?<br/>
    - The use of GitHub secrets and plugins to access AWS SSM secrets to complete pipeline steps help keep the pipelines secure.
    - Some actions such as deploying to pre-prod and prod are protected behind permissions so not any one can do them.
    - Publishing images to a remote image repository.
3. Describe something you have learned that you were able to use directly in your delivery.<br/>
    - Looking at the pipeline step logs has helped this week diagnose some issues with creating and pushing a new image to AWS ECR showing which steps failed and why. I've had more confidence in understanding what some of the workflows/actions I use regularly actually do, which plugins are being used, how the inputs affect what sandbox is being spun up etc 










