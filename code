const int ledpin = 6;
const int buzzpin = 12;
const int motionpin = 2;
volatile bool motion = false;

void setup() {
  Serial.begin(9600);
  Serial.println("PIR is starting up in 30 secs");
  delay(30000);
  pinMode(ledpin, OUTPUT);
  pinMode(buzzpin, OUTPUT);
  pinMode(motionpin, INPUT);

  attachInterrupt(digitalPinToInterrupt(motionpin), motionFound, RISING);
  Serial.println("PIR is ready to scan");
}

void loop() {
  if (motion) {
    Serial.println("Motion was detected!!");
    tone(buzzpin, 100);
    digitalWrite(ledpin, HIGH);

    delay(1000);

    digitalWrite(ledpin, LOW);
    noTone(buzzpin);
    motion = false;
  }
}

void motionFound() {
  motion = true;
}
