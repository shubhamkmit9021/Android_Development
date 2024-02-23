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
