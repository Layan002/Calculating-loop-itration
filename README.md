>[!NOTE]
>This concep took me hours to understand perfectly, this is may also what will happen with you. But it is very important and worthy concept to understand. It is fine to take your time with it!!


# Demo
https://github.com/user-attachments/assets/25174aa3-0f4e-42c1-bab1-324ed8204b49


# Code

``` CPP
unsigned long startTime;
unsigned long count = 0;

void setup() {
  Serial.begin(9600);
  startTime = millis();
}

void loop() {
  count++;
  if (millis() - startTime >= 1000) {  // If 1 second has passed
    Serial.print("Loops per second: ");
    Serial.println(count);
    count = 0;              // Reset count for the next second
    startTime = millis();   // Reset startTime for the next second
  }
  delay(100); // it cause 10 itrations per second
}
```

# Calculation
<img src="https://github.com/user-attachments/assets/472bf1b5-c8e1-43bc-b805-e00ee30d5eaf" alt="cal" width = 500>

