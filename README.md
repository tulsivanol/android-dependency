# android-dependency

# build.gradle(project)
    
    dependencies {
      classpath "androidx.navigation:navigation-safe-args-gradle-plugin:2.3.0-alpha04"
    }

# build.gradle(app)

  Add this at top of `build.gradle(app)` file
   
    apply plugin: 'kotlin-kapt'
    apply plugin: "androidx.navigation.safeargs.kotlin"

   JDK Compile Options 
   
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
    kotlinOptions {
        jvmTarget = JavaVersion.VERSION_1_8.toString()
    }
    
    
   Architectural Components
   
    implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:2.2.0"

   Room
   
    implementation "androidx.room:room-runtime:2.2.5"
    kapt "androidx.room:room-compiler:2.2.5"

   Kotlin Extensions and Coroutines support for Room
   
    implementation "androidx.room:room-ktx:2.2.5"

   Coroutines
   
    implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-core:1.3.5'
    implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-android:1.3.5'

   Coroutine Lifecycle Scopes
   
    implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:2.2.0"
    implementation "androidx.lifecycle:lifecycle-runtime-ktx:2.2.0"

   Retrofit
   
    implementation 'com.squareup.retrofit2:retrofit:2.6.0'
    implementation 'com.squareup.retrofit2:converter-gson:2.6.0'
    implementation "com.squareup.okhttp3:logging-interceptor:4.5.0"

   Navigation Components
   
    implementation "androidx.navigation:navigation-fragment-ktx:2.2.1"
    implementation "androidx.navigation:navigation-ui-ktx:2.2.1"

   Glide
   
    implementation 'com.github.bumptech.glide:glide:4.11.0'
    kapt 'com.github.bumptech.glide:compiler:4.11.0'
