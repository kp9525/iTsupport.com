allprojects {

    repositories {

        maven { url 'https://jitpack.io' }
   }
}
or in settings.gradle file:

dependencyResolutionManagement {

    repositories {

        maven { url 'https://jitpack.io' }
    }
}

Step 2. Add dependency:

dependencies {
    implementation 'com.github.yuriy-budiyev:code-scanner:2.3.2'
}
Add camera permission and hardware feature to AndroidManifest.xml (Don't forget about dynamic permissions on API >= 23):

<uses-permission android:name="android.permission.CAMERA"/>

<uses-feature
    android:name="android.hardware.camera"
    android:required="false"/>
Define a view in your layout file:

<?xml version="1.0" encoding="utf-8"?>
<FrameLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <com.budiyev.android.codescanner.CodeScannerView
        android:id="@+id/scanner_view"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
</FrameLayout>
