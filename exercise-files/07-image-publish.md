# 7 - build & publish an image to a private registry

## Instructions
Now we are happy with the images we built in exercise 4, and know a lot more about using credentials securely.

We need a pipeline that will checkout the code, authenticate with Github Container Registry, build the image and publish it.

For now (and the purposes of this exercise) we will need to trigger the pipeline manually. In future we will need to trigger this when we release the code in github by creating a tag. 

- Create the configuration for the pipeline in the `07-image-publish.yaml` file including name, trigger, and job that runs on ubuntu-latest.
- Add steps to the job which checkout the code and run the necessary commands.
- Move the config file into `.github/workflows` folder and commit & push your code.
- Use the github web interface to find and start your new pipeline.
- Once the pipeline has run successfully, disable it
- Consider which steps are important for all contrainer registries and which ones are specific to Github Container Registry

## Hints
- You could copy your exercise pipeline as a starting point
- Read the reference below for more information on the possible steps you can use
- The examples in the reference use a new, more secure, way of handling credentials - what is it?
    We're using secrets.GITHUB_TOKEN

## References
Pushing images to github container registry: [github docs]{https://docs.github.com/en/actions/use-cases-and-examples/publishing-packages/publishing-docker-images#publishing-images-to-github-packages}

## Notes

We are able to use plugins authored by other organisations, in this case we're using docker authored plugins to work with docker images, documentation however can be found on github.

As we're using plugins authored by another organisation, the way we reference context/working dirs is a bit different.

We're authenticating in a different way here, still don't quite get it but github is creating a token for us to use when we build our image using the docker provided plugins.

Those within our organisation are able to use the image/package that's been published to the github image repository.


Tried pulling the image that is created as a github package... get an unauthorised error from docker daemon.... 

