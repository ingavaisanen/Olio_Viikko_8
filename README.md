package com.example.olioviikko8;

import androidx.appcompat.app.AppCompatActivity;
import androidx.core.app.ShareCompat;

import android.os.Bundle;
import android.view.View;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    private EditText number1;
    private EditText number2;
    private TextView outputNum;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        number1 = findViewById(R.id.firstNumber);
        number2 = findViewById(R.id.secondNumber);
        outputNum = findViewById(R.id.output);
    }

    public void addNumbers(View view) {
        int num1 = Integer.parseInt(number1.getText().toString());
        int num2 = Integer.parseInt(number2.getText().toString());

        int sum = num1 + num2;
        outputNum.setText(String.valueOf(sum));
    }

    public void subtractNumbers(View view) {
        int num1 = Integer.parseInt(number1.getText().toString());
        int num2 = Integer.parseInt(number2.getText().toString());

        int subtraction = num1 - num2;
        outputNum.setText(String.valueOf(subtraction));
    }

    public void multiplyNumbers(View view) {
        int num1 = Integer.parseInt(number1.getText().toString());
        int num2 = Integer.parseInt(number2.getText().toString());

        int multiplication = num1 * num2;
        outputNum.setText(String.valueOf(multiplication));
    }

    public void divideNumbers(View view) {
        int num1 = Integer.parseInt(number1.getText().toString());
        int num2 = Integer.parseInt(number2.getText().toString());

        int division = num1 / num2;
        outputNum.setText(String.valueOf(division));
    }
}
