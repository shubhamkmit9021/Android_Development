
### Button Alignment on different positons

````js

<Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn1"
        android:text="btn1"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"

/>
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn2"
        android:text="btn2"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"
        android:layout_alignParentRight="true"

        />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn3"
        android:text="btn3"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"
        android:layout_alignParentBottom="true"

        />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn4"
        android:text="btn4"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"
        android:layout_alignParentBottom="true"
        android:layout_alignParentRight="true"

        />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn5"
        android:text="btn5"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"
        android:layout_centerVertical="true"

        />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn6"
        android:text="btn6"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"
        android:layout_centerVertical="true"
        android:layout_alignParentRight="true"

        />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn7"
        android:text="btn7"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"
        android:layout_centerInParent="true"

        />
````
## For left, right, top and bottom possition

    ***for left - toLeftOf***
    ***for right - toRightOf***
    ***for top - above***
    ***for bottom - below***

    ````js
        <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn1"
        android:text="btn1"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"

/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn2"
        android:text="btn2"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"
        android:layout_below="@+id/btn1"

        />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn3"
        android:text="btn3"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"
        android:layout_below="@id/btn2"
        android:layout_toRightOf="@+id/btn2"

        />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn4"
        android:text="btn4"
        android:textSize="25sp"
        android:backgroundTint="#00ff00"
        android:textColor="#f00"
        android:layout_toRightOf="@id/btn3"
        android:layout_above="@+id/btn3"

        />

    ````