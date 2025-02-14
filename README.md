# Incorrect Working Directory in Dockerfile

This repository demonstrates a common error in Dockerfiles: specifying an incorrect working directory.

## The Problem

The original `Dockerfile` sets the working directory to `/app`, copies files, installs dependencies, and tries to execute `index.js`. However, if the `index.js` file isn't in the correct location within the image, the command will fail because it cannot find the file.

## Solution

The `DockerfileSolution.txt` provides a corrected `Dockerfile`.  It ensures that the working directory is set correctly so that all subsequent commands operate within the expected context.