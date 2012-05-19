This is the official Android OpenSSL sources with the makefiles lightly patched to build as an external project with the Android NDK. Similar to https://github.com/eighthave/openssl-android but updated for Android 4.0.3 (OpenSSL 1.0.0e) and NDK r8.

To build, run:
```
ndk-build
```

Upstream: https://android.googlesource.com/platform/external/openssl
Makefile patches from: https://github.com/eighthave/openssl-android
To see the patches, run:
```
git diff upstream
```

# Background
Although Android ships with OpenSSL, it (understandably) doesn't provide libcrypto and libssl as part of its public API. Thus developers needs something like this to port their OpenSSL using apps to Android.
