# The Under Construction Page

This is a repository containing a generic under construction page as well as the instructions on building and running the page as a docker container.

## Building the Docker Image Locally

To build the Docker image for the under construction page, run the following command:

```
docker build -t underconstruction .
```

## Running the Docker Container Locally

To run the Docker image in a Docker container, use the following command:

```
docker run -d -p 8081:80 --name underconstruction underconstruction
```

## Running the Docker Container on Synology Hosted Docker

To deploy the 'underconstruction' Docker image to a Synology NAS using a custom scheduled task, follow these steps:

1. Open the Synology DSM control panel and navigate to the 'Task Scheduler'.
2. Create a new 'scheduled task' for a 'user-defined script' with the following settings.
3. Save task.
4. Manually execute task.
5. Confirm that the 'underconstruction' docker container is running.
6. Access the underconstruction page by accessing the Synology server host at port 18080


| Tab | Field | Configuration |
| --- | ------- | ----- |
| General | Task | Enter 'Manual-deploy underconstruction page' |
|  | User | Select 'root' |
| Schedule | Date | Select 'Run on the following date' with default values: today's date, and 'Do not repeat' |
| | Time | Leave as default |
| Task Settings | Notification | Leave as default (not checked) |
| | Run command | Paste the content this repo's 'synology-scripts/custom-scheduled-task.script' into the 'User-defined script' text box |


