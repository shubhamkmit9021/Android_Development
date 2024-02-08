# android:scaleType

1. **center:** This scales the image uniformly (maintaining its aspect ratio) and centers it within the ImageView. The image will be fully visible, but there might be empty space around it.
    ```xml
    android:scaleType="center"
    ```

2. **centerCrop:** This scales the image to fill the entire ImageView while maintaining its aspect ratio. It crops the image if needed to make sure the entire ImageView is covered.
    ```xml
    android:scaleType="centerCrop"
    ```

3. **centerInside:** This scales the image uniformly to fit within the bounds of the ImageView. It will be centered both horizontally and vertically, and the entire image will be visible.
    ```xml
    android:scaleType="centerInside"
    ```

4. **fitCenter:** Similar to centerInside, this scales the image uniformly to fit within the bounds of the ImageView. However, if the aspect ratio of the image differs from the aspect ratio of the ImageView, there may be empty space around the image.
    ```xml
    android:scaleType="fitCenter"
    ```

5. **fitStart:** This scales the image uniformly to fit within the bounds of the ImageView, aligning it to the top-left corner. The aspect ratio is maintained, and there may be empty space at the bottom or right.
    ```xml
    android:scaleType="fitStart"
    ```

6. **fitEnd:** Similar to fitStart, this aligns the image to the bottom-right corner, and there may be empty space at the top or left.
    ```xml
    android:scaleType="fitEnd"
    ```

7. **fitXY:** This scales the image non-uniformly to fill the entire ImageView, stretching it if necessary. This may distort the aspect ratio of the image.
    ```xml
    android:scaleType="fitXY"
    ```

8. **matrix:** This allows you to specify a custom transformation matrix for the image, giving you full control over its scaling and positioning. It's more advanced and not commonly used for simple cases.
    ```xml
    android:scaleType="matrix"
    ```





### Using cardView we can customized the layout for image easily
````
<LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="4"
        android:gravity="center"
        android:orientation="vertical" >
        
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            app:cardCornerRadius="30dp">
            
            <ImageView
                android:id="@+id/mapIcon"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:src="@drawable/route_map"
                android:scaleType="fitXY"  />

        </androidx.cardview.widget.CardView>
    </LinearLayout>
````
