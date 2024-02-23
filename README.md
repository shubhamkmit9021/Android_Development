# Android_Development

**For setOnClickListener we are implementing like this**
````
turnOnButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent intent = new Intent(PreSplash.this, PreSplashBg.class);
                startActivity(intent);   // for start new intent
            }
        });
````

**So instead of this we can also use lambda**
````
turnOnButton.setOnClickListener(v -> {
            Intent intent = new Intent(PreSplash.this, PreSplashBg.class);
            startActivity(intent);    // for start new intent
        });
````

## For updated method to write a code block for AlertDialog box 
````
AlertDialog.Builder builder = new AlertDialog.Builder(this);
        builder.setTitle("Confirmation");
        builder.setMessage("Are you sure to not allow the permission?");

        // Retrieve the drawable using ResourcesCompat.getDrawable()
        Drawable iconDrawable = ResourcesCompat.getDrawable(getResources(), R.drawable.baseline_info_24, null);

        // Apply a color filter to change the color
        iconDrawable.setColorFilter(ContextCompat.getColor(this, R.color.lightred), PorterDuff.Mode.SRC_IN);

        // Set the colored icon
        builder.setIcon(iconDrawable);

        builder.setPositiveButton("Yes", (dialog, which) -> {
           Toast.makeText(this, "sample line", Toast.LENGTH_SHORT).show();
        });

        builder.setNegativeButton("No", (dialog, which) -> {
            Toast.makeText(this, "sample line", Toast.LENGTH_SHORT).show();
        });

        AlertDialog alertDialog = builder.create();
        alertDialog.show();
    }

// Alternate way to write this function

//        builder.setPositiveButton("Yes", new DialogInterface.OnClickListener() {
//            @Override
//            public void onClick(DialogInterface dialog, int which) {
//                Toast.makeText(this, "sample line", Toast.LENGTH_SHORT).show();
//            }
//        });

//        builder.setNegativeButton("No", new DialogInterface.OnClickListener() {
//            @Override
//            public void onClick(DialogInterface dialog, int which) {
//                Toast.makeText(this, "sample line", Toast.LENGTH_SHORT).show();
//            }
//        });

````
