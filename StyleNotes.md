### Difference between textColor and textColorHint

**In Android, textColor and textColorHint are attributes used in different contexts for text display within various UI elements like TextView, EditText, etc.**

***textColor: This attribute is used to set the color of the actual text displayed in a TextView, EditText, or similar UI components. When you set textColor, it determines the color of the visible text content within the view.***

```
<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Hello, World!"
    android:textColor="@color/black" />
```

***textColorHint: This attribute is specifically used in EditText to set the color of the hint text that appears when the EditText is empty and does not have focus. It represents the color of the placeholder text that provides a hint or instructions to the user about what to enter in the EditText.***

```
<EditText
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:hint="Enter your name"
    android:textColorHint="@color/grey" />
```
