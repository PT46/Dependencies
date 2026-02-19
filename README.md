# Dependencies

## Retrofit
```
implementation("com.squareup.retrofit2:retrofit:2.10.0")
implementation("com.squareup.retrofit2:converter-gson:2.10.0")
implementation("com.squareup.okhttp3:logging-interceptor:4.12.0")
```

## Coroutines
```
implementation("org.jetbrains.kotlinx:kotlinx-coroutines-android:1.8.0")
```

## Glide
```
implementation ("com.github.bumptech.glide:glide:5.0.5")
```

## ViewModel (Not for Dagger VM)
```
implementation("androidx.lifecycle:lifecycle-viewmodel-ktx:2.8.1")
```

## Room DB
```
implementation("androidx.room:room-runtime:2.7.0")
implementation("androidx.room:room-ktx:2.7.0")
kapt("androidx.room:room-compiler:2.7.0")
```
```
plugins {
    id("kotlin-kapt")
}
```
## Work Manager
```
implementation("androidx.work:work-runtime-ktx:2.9.0")
implementation("androidx.hilt:hilt-work:1.0.0")
ksp("androidx.hilt:hilt-compiler:1.3.0")
```

# Jetpack Compose
Project Level
```
alias(libs.plugins.ksp) apply false
alias(libs.plugins.hilt) apply false
```
Module Level
```
plugins {
    alias(libs.plugins.ksp)
    alias(libs.plugins.hilt)
}
```
```
dependencies {
    implementation(libs.hilt.android)
    ksp(libs.hilt.compiler)
    implementation(libs.hilt.navigation.compose)
}
```
libs.versions.toml
- [versions]
``` 
ksp-version = "2.1.0-1.0.29"
hilt-version = "2.57.2"
kotlin = "2.1.0"
```
- [libraries]
```
hilt-android = { group = "com.google.dagger", name = "hilt-android", version.ref = "hilt-version" }
hilt-compiler = { group = "com.google.dagger", name = "hilt-android-compiler", version.ref = "hilt-version" }
hilt-navigation-compose = { group = "androidx.hilt", name = "hilt-navigation-compose", version = "1.2.0" }
```
- [plugins]
```
hilt = { id = "com.google.dagger.hilt.android", version.ref = "hilt-version" }
ksp = { id = "com.google.devtools.ksp", version.ref = "ksp-version" }
```

## ViewPager
```
 // ViewPager2
implementation("androidx.viewpager2:viewpager2:1.0.0")

 // TabLayout (Material)
implementation("com.google.android.material:material:1.11.0")

```

## Testing 
## Mock
```
testImplementation ('io.mockk:mockk:1.13.2')
    testImplementation ("org.jetbrains.kotlinx:kotlinx-coroutines-test:1.5.0")
    testImplementation ('androidx.arch.core:core-testing:2.1.0')

```
## Jetpack Testing
```
androidTestImplementation("androidx.compose.ui:ui-test-junit4")

debugImplementation("androidx.compose.ui:ui-test-manifest")
```

## Safe Args -- Navgraph
- [Project Level]
``` 
buildscript {
    repositories {
        google()
    }
    dependencies {
        val nav_version = "2.9.7"
        classpath("androidx.navigation:navigation-safe-args-gradle-plugin:$nav_version")
    }
}
```

- [App Level]
``` 
id("androidx.navigation.safeargs")
```

## Navgraph
``` 
// Navigation Component (Fragment + UI)
implementation("androidx.navigation:navigation-fragment-ktx:2.8.6")
implementation("androidx.navigation:navigation-ui-ktx:2.8.6")

```


## viewModels() depedency
``` 
implementation("androidx.activity:activity-ktx:1.9.0")
implementation("androidx.fragment:fragment-ktx:1.8.2")

```

## GraphQl depedency

## Project Level

``` 

buildscript {
    dependencies {
        classpath("com.apollographql.apollo3:apollo-gradle-plugin:3.8.5")
    }
}

```

## App Level

``` 

implementation("com.apollographql.apollo3:apollo-runtime:3.8.5")

```

## After Android{}

``` 

apollo {
    service("service") {
        packageName.set("com.example.graphql")
    }

```



