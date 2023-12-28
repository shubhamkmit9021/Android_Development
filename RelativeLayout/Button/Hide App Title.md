### Hide App Title in the Manifest (for the entire application):

**Open your AndroidManifest.xml file and locate the <application> tag. Add the android:label attribute with an empty string to hide the app title for the entire application:**

```
<application
    android:label=""
    ... >
    <!-- Other application configurations -->
</application>

```

***Setting android:label="" will hide the app title for all activities within the application.***

## Hide App Title in a Specific Activity (in Java code):

**If you want to hide the app title for a specific activity programmatically, you can do so in the Java code for that activity using the getSupportActionBar() method (if using AppCompatActivity) or getActionBar() (if using Activity) and set the title to null:**
***For AppCompatActivity:***
```
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.your_layout);
        **But this will not hide the title area this will hide only title text**
    if (getSupportActionBar() != null) {
        getSupportActionBar().setDisplayShowTitleEnabled(false);
    }
}
```

**In Short** 
**this will work simply hide the all title bar and its space also**
```
 @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        getSupportActionBar().hide();
    }
```

***For Activity:***
```
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.your_layout);

    ActionBar actionBar = getActionBar();
    if (actionBar != null) {
        actionBar.setDisplayShowTitleEnabled(false);
    }
}
```
***Replace your_layout with the layout file you're using for that specific activity.***
***By setting setDisplayShowTitleEnabled(false), you hide the app title for the specific activity's action bar.***
