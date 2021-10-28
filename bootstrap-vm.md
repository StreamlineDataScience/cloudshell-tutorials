
# Creating an RStudio Virtual Machine

## Overview

Here we will walk you through how to create a Virtual Machine (VM) on a
project with RStudio running.

**Time to complete**: About 5 minutes

Click the **Start** button to move to the next step.

## Getting the Shiny Requirements Shell

First we will download the shell file to your cloud shell directory to
run the shiny application. These 2 commands will pull in the shell file
`vmshiny.sh` and run it (may take a minute or 2)

``` bash
gsutil cp gs://streamline-startup-scripts/vmshiny.sh ./
source vmshiny.sh
```

If this fails, you need to request access to
`gs://streamline-startup-scripts`.

### Overview of what’s going on

The `vmshiny.sh` is running a `docker pull` command on a Docker image
that we created running shiny that is based on
<https://github.com/rocker-org/rocker-versioned2>. Then the script runs
docker with `-p 3838:3838` which forwards the port 3838 to the Cloud
Shell.

## Running the Shiny App

### Just trying a URL

This URL should open up in a new window with the shiny application.

<https://shell.cloud.google.com/devshell/proxy?port=3838&environment_id=default&devshellProxyPath=/create_vm>

### Use Web Preview

Click the Web Preview Icon:

<walkthrough-spotlight-pointer
    spotlightId="devshell-web-preview-button"> spotlight on the web
preview icon </walkthrough-spotlight-pointer>

Change the port to `3838` since that’s what Shiny typically runs on,
including this docker container.

## Conclusion

Done!
