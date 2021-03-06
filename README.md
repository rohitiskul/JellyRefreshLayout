# JellyRefreshLayout
A pull-down-to-refresh layout inspired by Lollipop overscrolled effects

Preview
--------
[![Preview](http://img.youtube.com/vi/mW7Y43dNpNM/0.jpg)](https://www.youtube.com/watch?v=mW7Y43dNpNM "Jelly preview")

Download
--------
Gradle:
```groovy
repositories {
    maven {
        url "https://jitpack.io"
    }
}
dependencies {
    compile 'com.github.rohitiskul:JellyRefreshLayout:1.0.1'
}
```
or Maven
```xml
<repository>
	<id>jitpack.io</id>
	<url>https://jitpack.io</url>
</repository>
```

```xml
<dependency>
    <groupId>com.github.rohitiskul</groupId>
    <artifactId>JellyRefreshLayout</artifactId>
    <version>1.0.1</version>
</dependency>
```

Usage
--------
Wrap any RecyclerView/ScrollView/ListView with JellyRefreshLayout

```xml
<com.rohitiskul.jellyrefresh.JellyRefreshLayout
    xmlns:app="http://schemas.android.com/apk/res-auto"
    app:progressBarColor="@color/your_progress_bar_color"
    app:jellyColor="@color/your_jelly_color"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <ListView
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
    
</com.rohitiskul.jellyrefresh.JellyRefreshLayout>
```

Call back when triggering refresh:
```java
mJellyLayout.setRefreshListener(new JellyRefreshLayout.JellyRefreshListener() {
    @Override
    public void onRefresh(final JellyRefreshLayout jellyRefreshLayout) {
        // your code here
    }
});
```
and finish refreshing when you are done:
```java
mJellyLayout.finishRefreshing();
```

You can also find more usages in the sample app included

Thanks to
--------
1. [JellyRefreshLayout](https://github.com/allan1st/JellyRefreshLayout) for Jelly Refresh Layout
2. [materialish-progress](https://github.com/pnikosis/materialish-progress) for Material Progress bar 

License
--------
    The MIT License (MIT)

    Copyright (c) 2015 Rohit Kulkarni

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
