#When building a new image we have to start from a base image, choosing the base image will be a crucial point to keep docker image more optimized. 


##1. Alpine Linux (:alpine)
 Alpine is the gold standard for minimal size. It is built on musl libc and busybox.

Size: ~5MB to 7MB.

Pros: Extremely small attack surface fast bootstrap time. 

Cons: Uses musl instead of glibc. This often causes performance issues or compilation failures with Python libraries (like pandas or numpy) and C++ extensions. 

##2. Debian/Ubuntu Slim (:-slim)
These are "gutted" versions of standard OS images. They remove documentation, man pages, and unnecessary packages but keep the core glibc library.

Size: ~30MB to 50MB.

Pros: Highly compatible with almost all Linux software, Have almost all dependecy libraries for the apps. Have bash helps in troubleshooting. 

Cons: Larger than Alpine.

##3. Distroless (gcr.io/distroless/...)
Maintained by Google, these images contain only your application and its runtime dependencies. They do not contain shell (sh/bash), package managers (apt/apk), or any other standard binaries.

Size: Varies (Python is ~50MB, Go is ~2MB).

Best for: High-security production environments.

Pros: Nearly impossible for a hacker to move laterally because there is no ls, cd, or curl inside the container. It only contains the application code

Cons: Hard to debug (you can't kubectl exec into a shell). You must use ephemeral debug containers.
