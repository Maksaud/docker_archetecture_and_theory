# Containerizing an app

Containers on their own does not benefits businesses. So apps are put into the containers

## To put the app inside the container

1. Take the app's source code
2. Create a docker file
 - This is a bunch of instructions that tells docker how to take the code and make an image from it
 - examples of some commamds:
    - What base Image do you want to use
    - Copying the files from the app
    - Bringing dependencies along
    - Other things the app would need
    - Network ports can be set
    - How to run the app
3. Input the build command onto terminal
```bash
docker image build
```
4. A conatianer is ready


## Multistage builds

Multistage builds give smaller and better images that is ideal for production.
