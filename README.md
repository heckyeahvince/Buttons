# Buttons Demo

This assignment illustrates the 3 main button handling methods in Android. 


## Keypoints:

* "xml onClick" method:
```xml
android:onClick="onClickImageButton"
```

```Java
    // Handle imageButton
    public void onClickImageButton(View view){
        Toast.makeText(getBaseContext(), "imageButton was clicked!",
                Toast.LENGTH_SHORT).show();
    }
```

* "Button instantiation - setOnClickListener()"  method:
```Java
   // Handle the first image text button
        Button image_btn1 = (Button) findViewById(R.id.imageTextButton1);
        image_btn1.setOnClickListener(new View.OnClickListener() {
            public void onClick(View view) {
                Toast.makeText(getBaseContext(), "imageTextButton1 was clicked!",
                        Toast.LENGTH_SHORT).show();
            }
        });
```

* "Button instantiation - anonymous OnClickListener class" method:
```Java
 // Button handling with anonymous class for the rest
        Button image_btn2 = (Button) findViewById(R.id.imageTextButton2);
        image_btn2.setOnClickListener(btnListener);

        Button image_btn3 = (Button) findViewById(R.id.imageTextButton3);
        image_btn3.setOnClickListener(btnListener);

        Button image_btn4 = (Button) findViewById(R.id.imageTextButton4);
        image_btn4.setOnClickListener(btnListener);
        
        ...
        
        private View.OnClickListener btnListener = new View.OnClickListener() {
        public void onClick(View view)
        {
            Toast.makeText(getBaseContext(),
                    ((Button) view).getText() + " was clicked!",
                    Toast.LENGTH_LONG).show();
        }
    };
```
