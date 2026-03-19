# DEVELOPING-AN-ANDROID-APPLICATION-FOR-ADDRESS-BOOK-

## AIM:
To develop an android application for address book.

## APPARATUS REQUIRED:
ØComputer
ØAndroid studio software


## THEORY:
The Address Book App is designed to store and display contact details such as a person's name and phone number. The user inputs the name and phone number into EditText fields, and by clicking the "Save Contact" button, the app displays the entered contact information in a TextView. This experiment introduces the basics of data handling in Android, including retrieving user input, storing it temporarily, and displaying it on the screen. It also demonstrates how to interact with basic UI components and use event listeners to respond to user actions. The Address Book App serves as a foundation for more complex applications involving data storage and manipulation.

## PROCEDURE:

1.Open Android Studio and then click on File -> New -> New project. 13. Then type the application name as “ex.no.2″ and click Next.
2.Then select the Minimum SDK as shown below and click next. 15. Then select the Empty Activity and click next.
3.Finally click Finish.
4.Click on app -> java -> com.example -> MainActivity.java
5.Now click on Text and type the program, so now the programming part of the main activity is completed.
6.Click on app -> res -> layout -> activity_main.xml.
7.Now click on Text and type the program, so now the designing part of Activity main is also completed.
8.Select the suitable available device to display the output. 22. Now run the application to see the output. 

## PROGRAM:
Main Activity JAVA
```
package com.example.addressbook;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText name, phone;
    Button save;
    TextView output;
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        name = findViewById(R.id.name);
        phone = findViewById(R.id.phone);
        save = findViewById(R.id.save);
        output = findViewById(R.id.output);

        save.setOnClickListener(v -> {
            String contact = "Name: " + name.getText().toString() +
                    "\nPhone: " + phone.getText().toString();
            output.setText(contact);
        });
   }
}
```
Actvity Main.XML
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="16dp">
 <EditText
        android:id="@+id/name"
        android:hint="Enter Name"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/phone"
        android:hint="Enter Phone"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:inputType="phone" />

    <Button
        android:id="@+id/save"
        android:text="Save Contact"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/output"
        android:paddingTop="16dp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

</LinearLayout>
```

## OUTPUT:
<img width="1291" height="682" alt="image" src="https://github.com/user-attachments/assets/57dbfbcf-03b1-40c3-9a2f-9e03f2378ba8" />


## RESULT:
Thus, the Android app for storing and displaying contacts is developed and the output is verified.





