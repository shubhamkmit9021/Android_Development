 ## For bydefault Toast
 ````
Toast.makeText(this, "Toast Message", Toast.LENGTH_SHORT).show();
````

## For custom Toast layout
**res -> layout -> rightClick -> new -> layout Resource file -> custom_toast_layout -> enter**

- ***using this one layout file is created custom_toast_layout.xml***
- ***Now we can design this layout according to our requirement like background color icon and text etc like anythinng we can use here***
- ***inside this layout which data we used we can use this everywhere as hardocoaded by calling this on any another page else using this id we can dynamically update this value***
````
<LinearLayout>
 <ImageView />
 <TextView />
</LinearLayout>
````
- ***Now on Java file we use use this like***
- **Inside onCreate method we can use this or implement this on any button setOnClickListener  .... ShowCustomToast();**
````
private void ShowCustomToast() {
        Toast toast = new Toast(getApplicationContext());
        View view = getLayoutInflater().inflate(R.layout.custom_toast_layout, (ViewGroup) findViewById(R.id.customToastbox));
        toast.setView(view);

        //  toast.setGravity(Gravity.TOP | Gravity.END,0,80);
        toast.setGravity(Gravity.TOP,0,80);
        toast.setDuration(Toast.LENGTH_LONG);

        // for update text
        TextView toastText = view.findViewById(R.id.toastText);
        toastText.setText("Changed text");

        // for update image
        ImageView toastImg = view.findViewById(R.id.toastImg);
        toastImg.setImageResource(R.drawable.baseline_emoji_emotions_24);

        // Update the color of the icon in the ImageView
        toastImg.setColorFilter(ContextCompat.getColor(getApplicationContext(), R.color.yellow), PorterDuff.Mode.SRC_IN);

        toast.show();
    }
````
