# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

##  Algorithm

1. **Start**

2. **Create a new project** in Android Studio with *Empty Activity*.

3. **Design the layout** (`activity_main.xml`):

   * Add a **Text Field** (EditText).
   * Add a **Button** labeled `"Implicit Intent"`.

4. **Go to MainActivity.java / MainActivity.kt**:

   * Initialize the button using `findViewById()`.

5. **Set OnClickListener for the button**:

   * When the button is clicked, create an **Implicit Intent** using:

     ```
     Intent intent = new Intent(Intent.ACTION_VIEW);
     intent.setData(Uri.parse("https://www.gmail.com"));
     ```

6. **Start the activity** using `startActivity(intent)` to open the default web browser.

7. **Run the application** on an emulator or mobile device.

8. **Output**:

   * When the app runs, user sees a text field and button.
   * Clicking the button opens the Gmail website (`www.gmail.com`) in the browser.

9. **Stop**

## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: SARANYA S.
Registeration Number : 212223220101
*/
```
MainActivity.java

```
package com.example.implicitintentapp;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Button btnImplicit = findViewById(R.id.btnImplicit);

        btnImplicit.setOnClickListener(v -> {
            Intent intent = new Intent(Intent.ACTION_VIEW);
            intent.setData(Uri.parse("https://www.gmail.com"));
            startActivity(intent);
        });
    }
}
```

activity_main.xml

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="20dp">

    <EditText
        android:id="@+id/editText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter something here"
        android:padding="10dp"
        android:inputType="text"
        />

    <Button
        android:id="@+id/btnImplicit"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Implicit Intent"
        android:layout_marginTop="20dp"
        />

</LinearLayout>
```

## OUTPUT

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cef3f19c-cf34-42c9-a2fa-04ab4973e467" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dc9a3970-f2b1-4ee9-8ff7-5cf8e21ac719" />


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


