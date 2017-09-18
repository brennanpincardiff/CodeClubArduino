
# Lesson 3

# Introducing motors

# Concepts:
1. Motor(s)
2. Motor board
3. Connecting motor board & Arduino
4. Simple code to make the motor move. 

# Equpiment 
1. Breadboard
2. Arduino
3. Wires to connect
4. DC motor (and others?)
5. Motor board

# Assemble the circuit 


# Our sketch
```c for Arduino IDE
/*************************************************************
Motor Shield 1-Channel DC Motor Demo
by Randy Sarafan
For more information see:
http://www.instructables.com/id/Arduino-Motor-Shield-Tutorial/
*************************************************************/

void setup() {
  
  //Setup Channel A
  pinMode(16, OUTPUT); //Initiates Motor Channel A pin
  pinMode(10, OUTPUT); //Initiates Brake Channel A pin
  
}

void loop(){
  
  //forward @ full speed
  digitalWrite(16, HIGH); //Establishes forward direction of Channel A
  digitalWrite(10, LOW);   //Disengage the Brake for Channel A
  analogWrite(3, 255);   //Spins the motor on Channel A at full speed
  
  delay(3000);
  
  digitalWrite(10, HIGH); //Engage the Brake for Channel A

  delay(1000);
  
  //backward @ half speed
  digitalWrite(16, LOW); //Establishes backward direction of Channel A
  digitalWrite(10, LOW);   //Disengage the Brake for Channel A
  analogWrite(3, 123);   //Spins the motor on Channel A at half speed
  
  delay(3000);
  
  digitalWrite(10, HIGH); //Eengage the Brake for Channel A
  
  delay(1000);
  
}
```
