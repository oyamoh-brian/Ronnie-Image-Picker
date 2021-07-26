 # Ronnie-Image-Picker

Asks for Camera and storage permission and return uri of the images taken or picked from the gallery.

Min Api Level: 16

Build System : [Gradle](https://gradle.org/)

 [![](https://jitpack.io/v/ronnieotieno/Ronnie-Image-Picker.svg)](https://jitpack.io/#ronnieotieno/Ronnie-Image-Picker)

## Getting started

You don't need to declare the permissions in the manifests.

Add this in your root build.gradle at the end of repositories:

```groovy
allprojects {
    repositories {
        ...
       maven { url 'https://jitpack.io' }
    }
}
```
Add this to dependencies:

```groovy
dependencies {
	     implementation 'com.github.ronnieotieno:Ronnie-Image-Picker:0.4.0' //Add latest version
	}
```
Example in code, Kotlin:

```kotlin
  lateinit var imagePicker : ImagePicker
  
  //Make sure that you initialize it at Oncreate
   override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
	 //activity
	 imagePicker = ImagePicker(this)
	 
	 //fragment
        imagePicker = ImagePicker(this)
    }

    //Camera
            imagePicker.takeFromCamera { uri, err -> 
                
            }
     
     //Gallery
            imagePicker.pickFromStorage { uri, err ->

            }
        
```
