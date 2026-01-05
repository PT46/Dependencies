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
