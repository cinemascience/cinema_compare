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

To use the viewer, select the database you want to see from the dropdown "Select a database". Test sphere should look like:
<img src="cinema/testImages/sphere.png" width="300" border="1"/>

while test sedov should look like:
<img src="cinema/testImages/sedov.png" width="300" border="1"/>


## Adding a database to the viewer
To add a database, you must edit the file data/data.json. The first entry in that file describes each of the tages needed. The file has two examples: 1) shere test, for a single dataset and 2) sedov test for comparing 3 datasets.



## Contact

Contact `cinema-info@lanl.gov` for more information.
