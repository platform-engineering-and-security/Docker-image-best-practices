# Layering in Dockerfile

## 1. Layer caches 
Each instruction in your Dockerfile. If a layer changes, every subsequent layer must be rebuilt.

Best Practice: Place instructions that change frequently (like COPY . .) at the bottom of the file.

Best Practice: Place stable instructions (installing OS packages, setting environment variables) at the top.

## 2. Combine Commands to Reduce Layer Count
Every RUN, COPY, and ADD instruction creates a new layer. While modern Docker versions are better at handling many layers, combining related commands reduces overhead and allows for better cleanup.

Best Practice: Use && and backslashes \ to group commands.

Best Practice: Delete temporary files (like zip files or package caches) in the same RUN command they were created.

