# Here are most useful list of android dependency 

## build.gradle(project)
    
    dependencies {
      ...
      classpath "androidx.navigation:navigation-safe-args-gradle-plugin:2.3.0-alpha04"
   ###### Dagger hilt
      classpath "com.google.dagger:hilt-android-gradle-plugin:2.28.3-alpha"
      ...
    }

## build.gradle(app)

  Add this at top of `build.gradle(app)` file
   
    apply plugin: 'kotlin-kapt'
    apply plugin: "androidx.navigation.safeargs.kotlin"
    apply plugin: 'dagger.hilt.android.plugin'

   JDK Compile Options 
   
    android {
    
      ...
        defaultConfig { 
            ...
            buildConfigField("String", "API_KEY", API_KEY)
            ...
        }
   
        compileOptions {
            sourceCompatibility JavaVersion.VERSION_1_8
            targetCompatibility JavaVersion.VERSION_1_8
        }
        kotlinOptions {
            jvmTarget = JavaVersion.VERSION_1_8.toString()
        }
        
      ...
    
    }
    
   Architectural Components
   
    def lifecycle_version = "2.2.0"
    implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:$lifecycle_version"
    implementation "androidx.lifecycle:lifecycle-runtime-ktx:$lifecycle_version"

   LifeCycle
   
    implementation "androidx.lifecycle:lifecycle-extensions:$lifecycle_version"
    implementation "androidx.lifecycle:lifecycle-livedata-ktx:$lifecycle_version"
    implementation "androidx.lifecycle:lifecycle-runtime:$lifecycle_version"

   Room
   
    def room_version = "2.2.5"
    implementation "androidx.room:room-runtime:$room_version"
    kapt "androidx.room:room-compiler:$room_version"

   Kotlin Extensions and Coroutines support for Room
   
    implementation "androidx.room:room-ktx:$room_version"

   Coroutines
   
    def coroutine_core_version = "1.3.7"
    def coroutine_android_version = "1.3.7"
    implementation "org.jetbrains.kotlinx:kotlinx-coroutines-core:$coroutine_core_version"
    implementation "org.jetbrains.kotlinx:kotlinx-coroutines-android:$coroutine_android_version"

   Retrofit
   
    def retrofit_version = "2.6.0"
    def okhttp_version = "4.5.0"
    implementation "com.squareup.retrofit2:retrofit:$retrofit_version"
    implementation "com.squareup.retrofit2:converter-gson:$retrofit_version"
    implementation "com.squareup.okhttp3:logging-interceptor:$okhttp_version"
    
   Activity KTX for viewModels()
    
    def activity_version = "1.1.0"
    implementation "androidx.activity:activity-ktx:$activity_version" 
    
   Dagger - Hilt
   
    def dagger_hilt_version = "2.28-alpha"
    implementation "com.google.dagger:hilt-android:$dagger_hilt_version"
    kapt "com.google.dagger:hilt-android-compiler:$dagger_hilt_version"
    
    def lifecycle_viewmodel = "1.0.0-alpha02"
    implementation "androidx.hilt:hilt-lifecycle-viewmodel:$lifecycle_viewmodel"
    kapt "androidx.hilt:hilt-compiler:$lifecycle_viewmodel"
    
  Timber
  
    def timber_version = "4.7.1"
    implementation "com.jakewharton.timber:timber:$timber_version"

   Navigation Components
   
    def navigation_version = "2.3.0"
    implementation "androidx.navigation:navigation-fragment-ktx:$navigation_version"
    implementation "androidx.navigation:navigation-ui-ktx:$navigation_version"
    
   Material Library
   
    def material_version = "1.3.0-alpha02"
    implementation "com.google.android.material:material:$material_version"

   Glide
   
    def glide_version = "4.11.0"
    implementation "com.github.bumptech.glide:glide:$glide_version"
    kapt "com.github.bumptech.glide:compiler:$glide_version"
