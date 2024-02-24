## PDF Viwer

### First You Implement PDF Library - 

```
implementation ("com.github.barteksc:android-pdf-viewer:3.2.0-beta.1")
```

### Go to Setting.gradle -

```
dependencyResolutionManagement {
    repositories {
        maven { url = uri("https://www.jitpack.io" ) }
        maven { url = uri ("https://jcenter.bintray.com") }
    }
}
```

### Go to gradle.properties and Paste this code-

```
android.enableJetifier=true
```


### Then go to Manifest and Use Permision -

```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
```

### Sync Now..

## XML Code -

```
<com.github.barteksc.pdfviewer.PDFView
    android:id="@+id/pdfView"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
/>

```

### App > New Folder > assets 

### Paste your pdf file for assets folder.


### Java Code -

```
PDFView pdfView = findViewById(R.id.pdfView);

// Load Form Assets
pdfView.fromAsset("simple.pdf").load();

// Load Form Internet
pdfView.fromUri("PDF_URL").load();
```


Extra

```
.enableSwipe(true) // allows to block changing pages using swipe
.swipeHorizontal(false)
.enableDoubletap(true)
.defaultPage(0)
.onTap(onTapListener)
.password(null)
.scrollHandle(null)
.nightMode(false)

.load();
```



_© All Right Reserved by Innovative Programmer ❤️_
