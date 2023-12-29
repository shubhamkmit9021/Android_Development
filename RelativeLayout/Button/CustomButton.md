# Create Custom Button example

### Create a drawable resource file (button_style.xml):

***Navigate to your res/drawable directory and create a new XML file (e.g., button_style.xml) to define the button's style.***
```
<!-- button_style.xml -->
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">
    <!-- Background color for the button -->
    <solid android:color="@color/purple_200" />
    
    <!-- Border color and width -->
    <stroke
        android:width="2dp"
        android:color="@color/black" />

    <!-- Corner radius for the button -->
    <corners android:radius="8dp" />
</shape>
```
***Apply the style to the button:***
```
<androidx.appcompat.widget.AppCompatButton
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="Reset"
    android:layout_marginStart="40dp"
    android:layout_marginEnd="40dp"
    android:layout_marginBottom="16dp"
    android:textColor="@color/your_text_color"
    android:background="@drawable/button_style" />
```
