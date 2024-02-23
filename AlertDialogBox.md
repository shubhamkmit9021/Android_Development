## Alert Dialog Box
- **Predefined Alert Dialog Box**
- **Customized Dialog Box**

### Predefined Alert Dialog Box
- ***here maxm we can take only three buttons inside this Positive, negative and neutral buttons***
- **In Dialog Box we can't use getApplicationContext() for a reference of a context. only we can use this or className.this, for a screen overlay issues**

- ### For Single Button Dialog Box
<img src="https://firebasestorage.googleapis.com/v0/b/storagehosting-5d20e.appspot.com/o/dialogbox_oneBtn.png?alt=media&token=601219f8-1021-41fd-a73f-c94109d26445" alt="Single Button Dialog Box" width="200" height="400">

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
- ### For Two Button Dialog Box
<img src="https://firebasestorage.googleapis.com/v0/b/storagehosting-5d20e.appspot.com/o/dialogbox_twoBtn.png?alt=media&token=c56a37cf-c80b-4018-bae3-61dcc507dfa2" alt="Two Button Dialog Box" width="200" height="400">

````
DilogBoxTwoBtn();

private void DilogBoxTwoBtn() {
        AlertDialog.Builder alertDialogBuilder = new AlertDialog.Builder(HomePage.this);
        alertDialogBuilder.setTitle("Delete");
        // alertDialogBuilder.setIcon(R.drawable.baseline_delete_24);
        alertDialogBuilder.setMessage("Are you sure want to delete ?");

        // Retrieve the drawable using ResourcesCompat.getDrawable()
        Drawable iconDrawable = ResourcesCompat.getDrawable(getResources(), R.drawable.baseline_delete_24, null);

        // Apply a color filter to change the color
        iconDrawable.setColorFilter(ContextCompat.getColor(HomePage.this, R.color.lightred), PorterDuff.Mode.SRC_IN);

        // Set the colored icon
        alertDialogBuilder.setIcon(iconDrawable);

        // Set the positive button and its click listener
        alertDialogBuilder.setPositiveButton("Yes", new DialogInterface.OnClickListener() {
            public void onClick(DialogInterface dialog, int which) {
                Toast.makeText(HomePage.this, "Delete Button pressed", Toast.LENGTH_SHORT).show();
            }
        });

        // Set the negative button and its click listener
        alertDialogBuilder.setNegativeButton("No", new DialogInterface.OnClickListener() {
            public void onClick(DialogInterface dialog, int which) {
                Toast.makeText(HomePage.this, "Canceled Delete", Toast.LENGTH_SHORT).show();
            }
        });

        // Create and show the AlertDialog
        AlertDialog alertDialog = alertDialogBuilder.create();
        alertDialog.show();

    }
````

- ### For Three Button Dialog Box
<img src="https://firebasestorage.googleapis.com/v0/b/storagehosting-5d20e.appspot.com/o/dialogbox_threeBtn.png?alt=media&token=c3c63e5e-ed38-45d8-a64f-7df7c03999ef" alt="Three Button Dialog Box" width="200" height="400">

````
DilogBoxThreeBtn();

private void DilogBoxThreeBtn() {
        AlertDialog.Builder alertDialogBuilder = new AlertDialog.Builder(HomePage.this);
        alertDialogBuilder.setTitle("Exit");
        // alertDialogBuilder.setIcon(R.drawable.baseline_exit_to_app_24);
        alertDialogBuilder.setMessage("Are you sure want to exit?");

        // Retrieve the drawable using ResourcesCompat.getDrawable()
        Drawable iconDrawable = ResourcesCompat.getDrawable(getResources(), R.drawable.baseline_exit_to_app_24, null);

        // Apply a color filter to change the color
        iconDrawable.setColorFilter(ContextCompat.getColor(HomePage.this, R.color.secondary), PorterDuff.Mode.SRC_IN);

        // Set the colored icon
        alertDialogBuilder.setIcon(iconDrawable);

        // Set the positive button and its click listener
        alertDialogBuilder.setPositiveButton("Yes", new DialogInterface.OnClickListener() {
            public void onClick(DialogInterface dialog, int which) {
                Toast.makeText(HomePage.this, "yess pressed", Toast.LENGTH_SHORT).show();
                // MainActivity.super.onBackPressed();  // if on first page then we can go back like this
            }
        });

        // Set the negative button and its click listener
        alertDialogBuilder.setNegativeButton("No", new DialogInterface.OnClickListener() {
            public void onClick(DialogInterface dialog, int which) {
                Toast.makeText(HomePage.this, "Noo pressed", Toast.LENGTH_SHORT).show();
            }
        });

        // Set the neutral button and its click listener
        alertDialogBuilder.setNeutralButton("Maybe", new DialogInterface.OnClickListener() {
            public void onClick(DialogInterface dialog, int which) {
                Toast.makeText(HomePage.this, "Cancel pressed", Toast.LENGTH_SHORT).show();
            }
        });

        // Create and show the AlertDialog
        AlertDialog alertDialog = alertDialogBuilder.create();
        alertDialog.show();

    }
````

## For Custom Dialog Box
- **Create custom dialog box :- layout -> rightclick -> new -> layout resource file -> custom_dialog_layout.xml**
- **dialog.setConcealable(false);**  // for disalbe auto hiding dialog box when user press outside of the dialog box
- **dialog.dismiss();**  // for close dialog box

<img src="https://firebasestorage.googleapis.com/v0/b/storagehosting-5d20e.appspot.com/o/custom_dialogBox.png?alt=media&token=91cb58f8-b078-45d3-83f6-58cdaf5961c8" alt="Custom Dialog Box" width="200" height="400">

 ````
ShowCustomDialogBox();

private void ShowCustomDialogBox() {
        Dialog dialog = new Dialog(this);
        dialog.setContentView(R.layout.custom_dialog_layout);
        dialog.setCancelable(false);  // for disable automatically closing dialogbox when user click outside the dialog

        // for button activity
        Button doneBtn = dialog.findViewById(R.id.doneBtn);
        doneBtn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Toast.makeText(HomePage.this, "Toast message", Toast.LENGTH_SHORT).show();
                dialog.dismiss();   // for close the dialog box
            }
        });

        dialog.show();

    }

````


