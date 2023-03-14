# Getting Error During Development

### Duplicate class error
````
 Duplicate class androidx.lifecycle.ViewModelLazy found in modules lifecycle-viewmodel-2.4.0-runtime (androidx.lifecycle:lifecycle-viewmodel:2.4.0) and lifecycle-viewmodel-ktx-2.3.1-runtime (androidx.lifecycle:lifecycle-viewmodel-ktx:2.3.1)

Add below dependency
In Gradle Scripts file -> build.gradle (Module:app) -> dependencies -> 

def lifecycle_version = "2.4.0"
implementation "androidx.lifecycle:lifecycle-viewmodel:$lifecycle_version"
implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:$lifecycle_version"

````
