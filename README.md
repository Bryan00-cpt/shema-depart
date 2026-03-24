const int buzzerPin = 25;

void setup() {
  ledcAttach(buzzerPin, 2000, 8);
}

void playTone() {
  ledcWriteTone(buzzerPin, 1000);
  delay(300);
  ledcWriteTone(buzzerPin, 0);
  delay(50);
}

void loop() {
  playTone();
}
