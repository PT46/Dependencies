# Module Level App
## Plugin
```
id("com.apollographql.apollo") version "4.1.1"
id("kotlin-kapt")
```
## Android
```
compileSdk = 35
targetSdk = 35
```
```
apollo {
        service("service") {
            packageName.set("com.codegalaxy.graphqldemo.model")
            mapScalar("uuid", "java.util.UUID")
        }
    }
```
## Dependencies
```
implementation(libs.apollo.runtime)
```
# In libs.versions.toml
Versions
```
agp = "8.9.1"
apolloRuntime = "4.1.1"
```
Library
```
apollo-runtime = { module = "com.apollographql.apollo:apollo-runtime", version.ref = "apolloRuntime" }
```
