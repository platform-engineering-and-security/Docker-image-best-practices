# Dockerfile Security

1. Always pull base image from authorized sources.
2. Don't use latest tag, always use some meangfully tagging.
3. Use minimal Image to reduce the attach surface.
4. Always install latest compatible packages.
5. Never store secrets or password in docker image
6. Always run image with non root user.
7. Scan Docker image with security scanning tools to make sure the image is vulnerability free.
8. Rebuild the image with latest compatible packages immediately when vulnerabilities identified.