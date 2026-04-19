# Here is a base image python baked on alpine. Alpine is the gold standard for minimal size. It is built on musl libc and busybox.
FROM python:3.15.0-alpine3.22


# These are "gutted" versions of standard OS images. They remove documentation, man pages, and unnecessary packages but keep the core glibc library.
FROM python:3.13.13-slim


# Bookworm is the codename for Debian 12, This is a heavy image, with full fledged libraries.
FROM python:3.13.13-bookworm


# Maintained by Google, these images contain only your application and its runtime dependencies. They do not contain shell (sh/bash), package managers (apt/apk), or any other standard binaries.
FROM gcr.io/distroless/python3-debian12


# Above is a few example of images which can be used as a base image for python application, for other softwares it varies and choosing a right base image helps in better optimized and secured image. 



