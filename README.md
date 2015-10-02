Orfox
=====

This is a new privacy-enhanced browser for Android, based on Mozilla Firefox,
configured by default to work with Orbot: Tor for Android.

You can learn more about the design of Tor Browser here:
https://www.torproject.org/projects/torbrowser/design/

Review the "Orfox Spec" document in this repo for more information on the
design goals and defaults for this browser.

Building
--------

You can find the source information on building "Fennec" for Android (aka
Firefox) from source here:
https://wiki.mozilla.org/Mobile/Fennec/Android#Building_Fennec

Additionally, it is easiest to build when using a specific Android SDK setup
to make sure that the version of things are correct, like the Support libs.

    cd /opt
    wget https://dl.google.com/android/android-sdk_r24.3.4-linux.tgz
    tar xzf android-sdk_r24.3.4-linux.tgz
    export ANDROID_HOME=/opt/android-sdk-linux
    export PATH="$ANDROID_HOME/tools:$PATH"
    android update sdk --no-ui --filter tools,platform-tools,build-tools-23.0.1,android-22
    cd $ANDROID_HOME
    mkdir -p extras/android
    cd extras/android
    wget https://dl.google.com/android/repository/support_r22.2.1.zip
    unzip support_r22.2.1.zip
    chmod -R a+rX $ANDROID_HOME
    find $ANDROID_HOME -executable |xargs chmod a+x
