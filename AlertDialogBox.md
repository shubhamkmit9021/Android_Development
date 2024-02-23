## Alert Dialog Box
- **Predefined Alert Dialog Box**
- **Customized Dialog Box**

### Predefined Alert Dialog Box
- ***here maxm we can take only three buttons inside this Positive, negative and neutral buttons***
- **In Dialog Box we can't use getApplicationContext() for a reference of a context. only we can use this or className.this, for a screen overlay issues**

- ### For Single Button Dialog Box
![Single Button Dialog Box](https://firebasestorage.googleapis.com/v0/b/storagehosting-5d20e.appspot.com/o/dialogbox_oneBtn.png?alt=media&token=601219f8-1021-41fd-a73f-c94109d26445)


````
DilogSingleBtn();

private void DilogSingleBtn() {
        AlertDialog alertDialog = new AlertDialog.Builder(HomePage.this).create();
        alertDialog.setTitle("Terms & Condition");
        // alertDialog.setIcon(R.drawable.baseline_info_24);  // default color came if we use directly

        // Retrieve the drawable using ResourcesCompat.getDrawable()
        Drawable iconDrawable = ResourcesCompat.getDrawable(getResources(), R.drawable.baseline_info_24, null);

        // Apply a color filter to change the color
        iconDrawable.setColorFilter(ContextCompat.getColor(HomePage.this, R.color.lightred), PorterDuff.Mode.SRC_IN);

        // Set the colored icon
        alertDialog.setIcon(iconDrawable);

        alertDialog.setMessage("Have you read the term & condiiton");

        // Add a positive button
        alertDialog.setButton(DialogInterface.BUTTON_POSITIVE, "Yes I've Read", new DialogInterface.OnClickListener() {
            @Override
            public void onClick(DialogInterface dialog, int which) {
                Toast.makeText(HomePage.this, "button pressed", Toast.LENGTH_SHORT).show();
            }
        });

        alertDialog.show();
    }

````
