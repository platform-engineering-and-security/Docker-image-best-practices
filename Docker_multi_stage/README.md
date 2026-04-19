# Multi Stage Dockerfile

## What is multi stage

In a dockerfile we build images on top of base images, in multistage we use multiple base images to build. We perform the operations in one stage and the final product which is essential for our app to run is being copied to the final stage which creates the app image.

## Example

### We need to unzip a folder 
In single stage Dockerfile
1. Install wget to download the remote zip folder
2. Download zip utility to unzip
3. unzip the folder


### Code Compilation
In single stage Dockerfile
1. Copy from local host to dockerfile.
3. Compile the code.
4. Use compiled code in app 

Disadvantag: multiple layers and unnecessary binary wget and zip which is not required for app to run, increases the size of image also the addon binary increases attack surface.