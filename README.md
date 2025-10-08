# workshop-MUID-
# Aim
To design and develop an Android application that takes two numbers as input from the user, performs addition, and displays the result.

# Procedure

1. Open Android Studio and create a new project with Empty Activity.

2. Design the layout in activity_main.xml with two EditText, one Button, and one TextView.

3. Open MainActivity.java and declare EditText, Button, and TextView objects.

4. Link the XML components with Java using findViewById().

5. Write setOnClickListener() for the Button to perform addition.

6. Fetch numbers from EditText, convert to integers, and calculate the sum.

7. Display the result in the TextView.

8. Run the application on an emulator or connected device.

# Program
```
Developed by: Bakkiyalakshmi E
Reg No: 212223220012
```
## activity.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="number" />

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="number" />

    <Button
        android:id="@+id/addBtn"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="ADD" />

    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Result will be shown here"
        android:textSize="18sp"
        android:paddingTop="20dp" />

</LinearLayout>

```
## MainActivity.java
```
package com.example.workshop;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import com.example.workshop.R;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button addBtn;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        addBtn = findViewById(R.id.addBtn);
        result = findViewById(R.id.result);

        addBtn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                int a = Integer.parseInt(num1.getText().toString());
                int b = Integer.parseInt(num2.getText().toString());
                int sum = a + b;
                result.setText("Result: " + sum);
            }
        });
    }
}
```
 # Result
Thus, the Android application for the Addition of Two Numbers was successfully created and executed.
 
