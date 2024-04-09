# Under Construction Page

This is a generic under construction page.

## Building the Docker Image

To build the Docker image for the under construction page, run the following command:

```
docker build -t under-construction-page .
```

To run the Docker image in a Docker container, use the following command:

```
docker run -d -p 80:80 --name under-construction-container under-construction-page
```