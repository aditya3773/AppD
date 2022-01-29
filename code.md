package com.example.adityakumarappd

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.view.View
import android.widget.Button
import android.widget.EditText
import android.widget.Toast

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val inputName: EditText=findViewById(R.id.name)
        val inputAge: EditText=findViewById(R.id.age)

        val btn:Button=findViewById(R.id.but_enter)
        btn.setOnClickListener(View.OnClickListener {
            if (inputName.text.toString().isNullOrBlank()) {

                Toast.makeText(this, "Please Enter Your Name", Toast.LENGTH_SHORT).show()


            } else {

                Toast.makeText(this, "Hi " + inputName.text + "\nGo corona Go", Toast.LENGTH_SHORT)
                    .show()
                inputName.setText("")
                inputAge.setText("")

            }
        })

        }
    }

