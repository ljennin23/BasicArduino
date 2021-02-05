# BasicArduino
I'm going to learn how to use an Arduino, and make awesome things with it!


## TableofContents
* [TableOfContents](#TableOfContents)
* [HelloArduino](#HelloArduino)
* [FiniteLEDBlink](#FiniteLEDBlink)
* [VariableLEDBlink](#VariableLEDBlink)
* [OneButtonOneLED](#OneButtonOneLED)
* [TwoButtonTwoLED](#TwoButtonTwoLED)
* [Servo](#Servo)

## HelloArduino

### Description & Code

```C++

  /*
  Blink

  Turns an LED on for half a second, then off for half a second, repeatedly.
  
  modified 8 May 2014  by Scott Fitzgerald
 
  http://www.arduino.cc/en/Tutorial/Blink
*/


// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin 13 as an output.
  pinMode(13, OUTPUT);
  Serial.begin(9600); // This turns on my Serial Monitor
  Serial.print("Hello World!");
  Serial.print("1...");
  Serial.print("2...");
  Serial.print("3...");
}

// the loop function runs over and over again forever
void loop() {
  Serial.println("Blink!");

  digitalWrite(13, HIGH);           // turn the LED on (HIGH is the voltage level)
  delay(250);                       // wait for a second
  digitalWrite(13, LOW);            // turn the LED off by making the voltage LOW
  delay(250);                       // wait for a second
}

```

### Evidence
[Here is my code on Arduino Create](https://create.arduino.cc/editor/helmstk1/9a3831dd-4b86-42f2-be49-c28b84874092/preview)

### Image or Wiring
![arduinowiring](images/arduinowiring.png)

### Reflection

this was hard for me to figure out at first but then once I figured out what the parts of the code mean it made more sense. i realized that high meant on and low meant off and then you could use the void loop for the delay.


## FiniteLEDBlink

### Description & Code

```C++
int ledPin = 13;
int blinkTime = 500;

void setup()
{
  pinMode(ledPin, OUTPUT);
  blinkyBlinky(5, blinkTime); // 5 is number of blinks, blinkTime is the milliseconds in each state from above: int blinkTime = 500;
}

void loop()
{
  //
}

void blinkyBlinky(int repeats, int time)
{
  for (int i = 0; i < repeats; i++)
  {
    digitalWrite(ledPin, HIGH);
    delay(time);
    digitalWrite(ledPin, LOW);
    delay(time);
  }
}
```

### Evidence
[here is my code in arduino create] https://create.arduino.cc/editor/ljennin23/bc0252e0-3b0a-4cd7-9429-e219adb2909f 

### Image or Wiring
![arduinowiring](images/arduinowiring.png)

### Reflection
This assignment made me realise that I definitely like CAD better than arduio. I had a hard time figuring out this code so I went on google and looked on the arduino website https://forum.arduino.cc/index.php?topic=273575.0 and looked at some code there. This helped me figure out this code.





## VariableLEDBlink

### Description & Code

```C++
/* Karl Helmstetter
  variable LED BLink
  This should blink an LED faster and faster, until it reaches 5 blinks per second
*/

int ledPin = 8;
int delayVar = 1000;  //this variable is used for my delays.

void setup() {
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  Serial.println(delayVar);

  digitalWrite(ledPin, HIGH);           // turn the ledPin on (HIGH is the voltage level)
  delay(delayVar);                   // pause for (delayVar) milliseconds
  digitalWrite(ledPin, LOW);            // turn the ledPin off by making the voltage LOW
  delay(delayVar);                   // pause for (delayVar) milliseconds

if(delayVar > 100){
  delayVar = delayVar - 100;
}
  //
  //as long as the delay is longer than 100 ms, we should continue to blink,
  // and we should also reduce delayVar by 100 ms.
  // (this way, once delayVar hits 100, we stop reducing it.)

}
```


### Evidence
https://create.arduino.cc/editor/ljennin23/9015e9cc-f054-4798-8797-6e66fcd742d5


### Image or Wiring
![arduinowiring](images/arduinowiring.png)

### Reflection

I had trouble with this assignment and had to ask Mr. Helmstetter to help me. He gave me his code and looked over it to make sure everything made sense and it did. This code was very similar to the finite LED blink, and we had to do a if statement to make sure the blinkng gets as fast as possible. then I i figured it out.

## OneButtonOneLED

### Description & Code


### Evidence
 

### Image or Wiring


### Reflection

## TwoButtonTwoLED

### Description & Code


### Evidence
 

### Image or Wiring


### Reflection

## Servo

### Description & Code


### Evidence
 

### Image or Wiring


### Reflection
