# DexHelper

[中文版](README_CN.md)

Simple Gradle Plugin to analyze per-dex in an Android Package, which generated by assemble command, to aid in getting under the 65,536 referenced method limit.

## Integration

### Dependencies 

```gradle
buildscript {
    repositories {
        jcenter()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:2.3.3'
        classpath 'com.ximsfei:dexhelper:0.0.1'
    }
}
```

### Apply Plugin

```gradle
apply plugin: 'com.android.application'
apply plugin: 'com.ximsfei.dexhelper'
```

### Run With Gradle

```
$ ./gradlew assemble -q
  DexHelper: apk file -> app-debug.apk
  DexHelper: dex file -> classes.dex
  DexHelper: method size -> 27022
  DexHelper: apk file -> app-release-unsigned.apk
  DexHelper: dex file -> classes.dex
  DexHelper: method size -> 27021
```
 
## [License Apache](LICENSE)
