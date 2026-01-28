# Hilt With XML
## Project Level Dependencies 
```
alias(libs.plugins.jetbrainsKotlin)  apply false
alias(libs.plugins.ksp) apply false
alias(libs.plugins.hilt) apply false
```
## Module Level Plugins 
-- Jetbrains plugins shouldn't be there here. 
```
alias(libs.plugins.ksp)
alias(libs.plugins.hilt)
```
## Module Level Dependencies
```
implementation(libs.hilt.android)
ksp(libs.hilt.compiler)
implementation(libs.hilt.navigation.compose)
```
## [VERSIONS]
```
ksp-version = "2.3.4"
hilt-version = "2.59"
kotlin = "2.1.0"
```
## [LIBRARIES]
```
hilt-android = { group = "com.google.dagger", name = "hilt-android", version.ref = "hilt-version" }
hilt-compiler = { group = "com.google.dagger", name = "hilt-android-compiler", version.ref = "hilt-version" }
hilt-navigation-compose = { group = "androidx.hilt", name = "hilt-navigation-compose", version = "1.2.0" }
```
## [PLUGINS]
```
jetbrainsKotlin = {id = "org.jetbrains.kotlin.android",version.ref ="kotlin"}
hilt = { id = "com.google.dagger.hilt.android", version.ref = "hilt-version" }
ksp = { id = "com.google.devtools.ksp", version.ref = "ksp-version" }
```
