# codeship-volume-test
[ ![Codeship Status for InVisionApp/codeship-volume-test](https://app.codeship.com/projects/2a24fac0-db6b-0134-7718-125507c76e50/status?branch=master)](https://app.codeship.com/projects/204024)

We want to make sure that volume changes in Docker 1.13 will not cause issues with how we use volumes to share output between steps with Codeship. This repo runs a simple container with a volume to a directory that does not exist on the host system. We then add a file into. The next step mounts that same volume again and tries to read the file.

Once we are done testing this repository can be safely deleted.

## To Test Locally

1. Verify you are running Docker version 1.13 or newer (`docker version`)
1. Make sure you do not have an output dir already, if you do run `rm -R output/`
1. Run `jet steps`
