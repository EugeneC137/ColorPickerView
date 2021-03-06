# ColorPickerView
You can use like using just ImageView and you can get color from any images.

![screenshot0](https://cloud.githubusercontent.com/assets/24237865/23684747/011279de-03e4-11e7-8cb3-3d5271efedc6.jpg)
![screenshot1](https://cloud.githubusercontent.com/assets/24237865/23684824/42e77472-03e4-11e7-9f5e-a58b7708dfd8.jpg)


## Including in your project
#### build.gradle
```java
repositories {
  mavenCentral() // or jcenter() works as well
}

dependencies {
  compile 'com.github.skydoves:colorpickerview:1.0.0'
}
```

#### or Maven
```xml
<dependency>
  <groupId>com.github.skydoves</groupId>
  <artifactId>colorpickerview</artifactId>
  <version>1.0.0</version>
</dependency>
```
    
## Usage
You can use like using just ImageView and you can get color from any images.

#### Add XML Namespace
First add below XML Namespace inside your XML layout file.

```xml
xmlns:app="http://schemas.android.com/apk/res-auto"
```

#### ColorPickerView in layout
```xml
<com.skydoves.colorpickerview.ColorPickerView
        android:id="@+id/colorPickerView"
        android:layout_width="300dp"
        android:layout_height="300dp"
        app:src="@drawable/palette"
        app:selector="@drawable/wheel" />
```

#### Attribute description
```
app:src="@drawable/palette" // set palette image
```

```
app:selector="@drawable/wheel" // set selector image. This isn't required always. If you don't need, don't use.
```

#### Color Selected Listener
```java
colorPickerView.setColorListener(new ColorPickerView.ColorListener() {
            @Override
            public void onColorSelected(int color) {

            }
        });
```

#### Methods
```java
colorPickerView.getColor() // return int what the last selected color
```
```java
colorPickerView.getColorHtml() // return String what the last selected Html color code
```
```java
colorPickerView.getColorRGB() // return int array the last selected color's RGB value. int[0] : R, int[1] : G, int[2] : B
```

# License
```xml
Copyright 2017 skydoves

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
