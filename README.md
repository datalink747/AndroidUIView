# AndroidUIView v1.0

It's a very simple custom views library according UIButton in iOS, all of the views can be automatically set a pressed effect to a button with a simple background image without writing a selector.xml

Hope you will like it :)

`UIButton` A view extends Button, like as UIButton in iOS.

`UIImageView` A view extends ImageView, like as UIButton in iOS.


## Screenshots

<img src="/screenshots/s1.png" alt="screenshot" title="screenshot" width="270" height="486" /><img src="/screenshots/s2.png" alt="screenshot" title="screenshot" width="270" height="486" />


## Usage
### Step 1
####Gradle
```groovy
dependencies {
    compile 'me.drakeet.library:androiduiview:1.0.0'
}
```

####Or

Import the library, then add it to your `/settings.gradle` and `/app/build.gradle`, if you don't know how to do it, you can read my blog for help.

[Android Studio 简介及导入 jar 包和第三方开源库方法](http://drakeet.me/android-studio)

### Step 2

It's very easy, just like this:

before using, add the namespace code to your xml:
```xml
xmlns:drakeet="http://schemas.android.com/apk/res-auto"
```

all right, 

```xml
<me.drakeet.library.UIButton
    android:layout_width="64dp"
    android:layout_height="64dp"
    android:layout_margin="16dp"
    drakeet:alpha_pressed="80"
    drakeet:color_pressed="#660303ff"
    android:background="@mipmap/ic_launcher"/>

<me.drakeet.library.UIButton
    android:layout_width="64dp"
    android:layout_height="64dp"
    android:layout_margin="16dp"
    drakeet:shape_type="round"
    android:background="@mipmap/avatar"/>
    
<me.drakeet.library.UIImageView
    android:layout_width="64dp"
    android:layout_height="64dp"
    android:layout_margin="16dp"
    drakeet:shape_type="round"
    android:src="@mipmap/avatar2"/>
```

### Customization

You can change several attributes in the XML file:

* drakeet:alpha_pressed [integer def:48 0-255] --> Alpha of the cover color when pressed
* drakeet:color_pressed [color def:#9c000000] --> Color of the cover when pressed
* drakeet:shape_type [enum (rectangle, round) def:rectangle] --> Rectangle or round of cover shape
* drakeet:radius [dimension def:2dp] --> Add a radius to the cover

## BUG

## DEMO
[apk](/sample/sample-release.apk)

## About me

My blog: http://drakeet.me

More about me: http://drakeet.me/about

License
============

    The MIT License (MIT)

    Copyright (c) 2015 drakeet

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
