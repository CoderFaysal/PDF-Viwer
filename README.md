## PDF Viwer Problem Solved

### First You Implement PDF Library - 

```
implementation 'com.github.barteksc:android-pdf-viewer:3.2.0-beta.1'
```

### Go to Setting.gradle -

```
dependencyResolutionManagement {
    ...
        maven {
            url ("https://jcenter.bintray.com")
        }

    }
}
```

### Go to gradle.properties and Paste this code-

```
android.enableJetifier=true
```


### Then go to Manifest and Use Permision -

```
    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
    <uses-permission android:name="android.permission.INTERNET"/>
```

### Sync Now..

## XML Code -

```
    <com.github.barteksc.pdfviewer.PDFView
        android:id="@+id/pdfView"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>

```

### App > New Folder > assets 
### Paste your pdf file for assets folder.


### Java Code -

```
        PDFView pdfView;
        pdfView = findViewById(R.id.pdfView);
        pdfView.fromAsset("simple.pdf").load();

```



_© All Right Reserved by Innovative Programmer ❤️_
