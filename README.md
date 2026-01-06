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
