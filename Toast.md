 ## For bydefault Toast

 - <img src="https://firebasestorage.googleapis.com/v0/b/storagehosting-5d20e.appspot.com/o/predefined_sampleToast.png?alt=media&token=7633bff7-bb5e-48b3-b9ae-0fcc6cb75d10" alt="For default sample Toast" width="200" height="400">

 ````
Toast.makeText(this, "Toast Message", Toast.LENGTH_SHORT).show();
````

## For custom Toast layout

**res -> layout -> rightClick -> new -> layout Resource file -> custom_toast_layout -> enter**

- ***using this one layout file is created custom_toast_layout.xml***
- ***Now we can design this layout according to our requirement like background color icon and text etc like anythinng we can use here***
  - <img src="https://firebasestorage.googleapis.com/v0/b/storagehosting-5d20e.appspot.com/o/hardcoded_customToast.png?alt=media&token=c5ec5b04-cb83-4bd9-b130-2f47f5d174a3" alt="For default sample Toast" width="200" height="400">
- ***inside this layout which data we used we can use this everywhere as hardocoaded by calling this on any another page else using this id we can dynamically update this value***
  - <img src="https://firebasestorage.googleapis.com/v0/b/storagehosting-5d20e.appspot.com/o/dynamic_customToast.png?alt=media&token=e96140cc-b8a0-4fd2-831e-7239860ac704" alt="For default sample Toast" width="200" height="400">
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
