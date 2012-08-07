This is the official Android OpenSSL sources with the makefiles lightly patched to build as an external project with the Android NDK. Similar to https://github.com/eighthave/openssl-android but updated for Android 4.0.3 (OpenSSL 1.0.0e) and NDK r8b.

To build, run:
```
ndk-build -j $(getconf _NPROCESSORS_ONLN)
```

* Upstream: https://android.googlesource.com/platform/external/openssl
* Makefile patches inpired by: https://github.com/eighthave/openssl-android

To see the patches, run:
<pre>
git remote add upstream https://android.googlesource.com/platform/external/openssl
git fetch upstream
git diff upstream/ics-plus-aosp 
</pre>

# Background
Although Android ships with OpenSSL, it understandably doesn't provide libcrypto and libssl as part of its public API. Thus developers porting OpenSSL using apps to Android need a project like this.
