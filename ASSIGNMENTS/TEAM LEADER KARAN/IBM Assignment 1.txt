int MQ2pin = A0;

const int gas = 0;


void setup() {
  Serial.begin(96000);
}

void loop() {
  float sensorValue,MQ2pin;
sensorValue = analogRead(MQ2pin);
  if(sensorValue >= 470){
    digitalWrite(11,HIGH);
     digitalWrite(9,HIGH);
    Serial.print(sensorValue);
    Serial.println(" !!ALERT!!");
    
  
  }
  else{
  	digitalWrite(11,LOW);
    digitalWrite(9,LOW);
    Serial.println("Sensor Value: ");
    Serial.println(sensorValue);
  } 
  delay(1000);
}
	float getsensorValue(int pin){
  	return (analogRead(pin));
}