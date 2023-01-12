#include <ESP8266WiFi.h>
#include <WiFiClient.h>
#include <ESP8266WebServer.h>

const int triggerPin1 = D1; //Trigger pin of the first ultrasonic sensor
const int echoPin1 = D2;    //Echo pin of the first ultrasonic sensor
const int triggerPin2 = D3; //Trigger pin of the second ultrasonic sensor
const int echoPin2 = D4;    //Echo pin of the second ultrasonic sensor
const int relayPin = D5;    //Pin connected to the base of the TIP41C transistor
const int dataPin = D6;     //Data pin of the 74HC595 shift register
const int latchPin = D7;    //Latch pin of the 74HC595 shift register
const int clockPin = D8;    //Clock pin of the 74HC595 shift register
int delayTime = 500;        //Delay time between each relay in milliseconds
int relayCount = 32;        //Number of relays to be controlled
int shiftRegisters = 2;     //Number of 74HC595 shift registers used

void setup() {
  //Initialize the relay pin as output
  pinMode(relayPin, OUTPUT);
  //Initialize the ultrasonic sensor pins as output and input
  pinMode(triggerPin1, OUTPUT);
  pinMode(echoPin1, INPUT);
  pinMode(triggerPin2, OUTPUT);
  pinMode(echoPin2, INPUT);
  //Initialize the 74HC595 shift register pins as output
  pinMode(dataPin, OUTPUT);
  pinMode(latchPin, OUTPUT);
  pinMode(clockPin, OUTPUT);
}

void loop() {
  //Measure the distance using the first ultrasonic sensor
  int distance1 = measureDistance(triggerPin1,echoPin1);
  //Measure the distance using the second ultrasonic sensor
  int distance2 = measureDistance(triggerPin2,echoPin2);
  //If the distance from both sensors is less than 30cm
  if(distance1 < 30 && distance2 < 30){
    //Turn on the relays in sequence
    for(int i=0; i<relayCount; i++){
      //shift the data to the shift register
      shiftOut(dataPin, clockPin, MSBFIRST, 1<<i);
      //latch the data
      digitalWrite(latchPin, HIGH);
      digitalWrite(latchPin, LOW);
      //Turn on the corresponding relay
      digitalWrite(relayPin, HIGH);
      delay(delayTime);
      //Turn off the corresponding relay
      digitalWrite(relayPin, LOW);
      delay(delayTime);
    }
  }
}

//Function to measure the distance using the ultrasonic sensor
int measureDistance(int trigger, int echo){
  //Send a trigger signal to the ultrasonic sensor
  digitalWrite(trigger, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigger, LOW);
  //Measure the duration of the echo signal
  long duration = pulseIn(echo, HIGH);
  //Calculate the distance
  int distance = duration*0.034/2;
  return distance;
}
