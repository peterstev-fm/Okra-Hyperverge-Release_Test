# Foobar

Steps to reproduce error

1. Enable minify
```
android {
    buildTypes {
        release {
            minifyEnabled true
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
        }
    }
}
```

2. Generate an app bundle in release mode
result:

```
Duplicate class a.a.a.a.a found in modules jetified-offlinekyc-1.2.9-runtime (co.hyperverge:offlinekyc:1.2.9) and jetified-okra-android-sdk-v2.64-runtime (com.github.okraHQ:okra-android-sdk:v2.64)
Duplicate class a.a.a.a.b found in modules jetified-offlinekyc-1.2.9-runtime (co.hyperverge:offlinekyc:1.2.9) and jetified-okra-android-sdk-v2.64-runtime (com.github.okraHQ:okra-android-sdk:v2.64)

```
