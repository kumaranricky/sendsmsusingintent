
# Ex.No:4 Design an android application Send SMS using Intent.


## AIM:
To create and design an android application Send SMS using Intent using Android Studio.

## EQUIPMENTS REQUIRED:
Android Studio(Min. required Artic Fox)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.
Step 2: Then type the Application name as “ex.no.4″ and click Next. 
Step 3: Then select the Minimum SDK as shown below and click Next.
Step 4: Then select the Empty Activity and click Next. Finally click Finish.
Step 5: Design layout in activity_main.xml.
Step 6: Send SMS and Display details give in MainActivity file.
Step 7: Save and run the application.

## PROGRAM:
/*
Developed by: Kumaran.B\
Registeration Number : 212220230026
*/
## activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <Button
        android:id="@+id/send_sms"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="sendsms"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java
```java
package com.example.intent;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button mButton=(Button) findViewById(R.id.button);
        mButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(Intent.ACTION_VIEW, Uri.fromParts("sms","7890457389",null));
                intent.putExtra("sms_body","Hello...");
                startActivity(intent);
            }
        });
    }
}
```

## <br><br><br><br><br><br><br><br><br><br><br><br>OUTPUT
![Screenshot (120)](https://user-images.githubusercontent.com/75243072/166181626-04e9cd61-369c-4d8b-9959-e22ddf8eda47.png)
![Screenshot (119)](https://user-images.githubusercontent.com/75243072/166181635-f1788a64-a0b5-450a-8940-1cd0362338f5.png)

## RESULT
Thus,an android application to Send SMS using Intent using Android Studio is developed and executed successfully.
