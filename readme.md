## Cinema:Compare repository, Release v1.0

A simple viewer that compares several Cinema Spec D databases. It can also be used to view a single database, and is easily customizable to include other elements through direct editing of the `html` or `json`.

## A Note on Browser Security
To use Cinema:Compare, you must allow local file access. Do this in the following way, but be sure to reset these options when you are done:

- **Firefox** 
    - in ```about:config```, set ```privacy.file_unique_origin``` to **false**
        This is essential for cinema to work
    - in ```about:config```, set ```security.fileuri.strict_origin_policy``` to **false**
        This allows loading of a file from any folder
- **Safari** 
    - Safari->Preferences->Advanced->Show Develop menu in menu bar
    - Safari->Develop->Disable Local File Restrictions (on)
- **Chrome** 
    - open **chrome** with the option ```--disable-web-security``` 
    - Mac example:
        - ```open -na "Google Chrome" cinema_compare.html --args --user-data-dir="YOUR_PATH_TO_REPO" --disable-web-security```

## Using the viewer

To use the viewer, edit the `cinema_compare.html` file, and change the value of the array named `dataSets` to include the path to your Cinema Spec D database.  Uncomment the appropriate line to choose to view the single example database (a sphere) or the multiple example databases (a Sedov blast wave).  


```
// START: Array of databases to view
// Single example Cinema database -- comment out for multiple example test
 var dataSets = [  "data/sphere.cdb"];

// Multiple example Cinema databases -- comment out for single example test
// var dataSets = [  "data/sedov1.cdb" , "data/sedov2.cdb" , "data/sedov3.cdb"];
// END : Array of databases to view

```   			

Then, view the `cinema_compare.html` file in the Firefox browser.  The single database will show the example sphere, with one slider present for every column in the Cinema databse:

<img src="doc/img/single.png" width="300" border="1"/>

The multiple database comparison has the same data rendered in different colormaps and opacity settings.  Setting phi=-60 and theta=0, you can see the blast wave develop as you increase time:

<img src="doc/img/triple.png" width="400" border="1"/>

## Contact

Contact `cinema-info@lanl.gov` for more information.
