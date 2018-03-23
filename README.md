# simple-splash-screen-kotlin
An example project to show how to implement a simple splash screen

You start by creating a new activity called SplashActivity and define it as the Launcher Activity, then you set the SplashTheme in the activity definition in AndroidManifest.xml

```
<activity
    android:name=".SplashActivity"
    android:theme="@style/SplashTheme">
    <intent-filter>
        <action android:name="android.intent.action.MAIN" />
        <category android:name="android.intent.category.LAUNCHER" />
    </intent-filter>
</activity>
```

In res -> values -> styles.xml you create a new style with SplashTheme name and define an item called android:windowBackground that will be a drawable that you will create in the next step.

```
<style name="SplashTheme" parent="Theme.AppCompat.NoActionBar">
    <item name="android:windowBackground">@drawable/background_splash</item>
</style>
```

In res -> drawable folder you will create a background_splash.xml with two layers, a white background and the launcher icon in the center. You can customize this xml file the way you want.

```
<?xml version="1.0" encoding="utf-8"?>
<layer-list xmlns:android="http://schemas.android.com/apk/res/android">
    <item
        android:drawable="@color/white"/>
    <item>
        <bitmap
            android:gravity="center"
            android:src="@drawable/ic_launcher"/>
    </item>
</layer-list>
```
