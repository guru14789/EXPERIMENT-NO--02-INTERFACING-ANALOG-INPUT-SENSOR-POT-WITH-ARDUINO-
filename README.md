## DATE: 23.02.2024
## NAME: SREEKUMAR S
## ROLL NO: 212223240157
## DEPARTMENT: AIML
 
## INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-



## AIM:  To interface an Analog  input (angular displacement sensor POT) and scale the values up on change in the input.


## COMPONENTS REQUIRED:
1.	10 KΩPOT
2.	1 KΩ resistor 
3.	Arduino Uno 
4.	USB Interfacing cable 
5.	Connecting wires 
6.	LED of choice 



**THEORY**: 

## Analog signals:

Analog signals – directly measurable quantities in terms of some other quantity.
Examples:
1. Thermometer – mercury height rises as temperature rises
2. Car Speedometer – The needle moves farther right as you accelerate
3. Stereo – Volume increases as you turn the knob
The reason for the conversion of analog to digital quantity is that as the controller or any microprocessor works with digital signals in the form of 0 and 1s, to make the signal compatible  most of the analog signals are converted into their equivalent digital level signals using an analog to digital converter.
Quantizing - breaking down analog value is a set of finite states
Encoding - assigning a digital word or number to each state and matching it to the input signal
 There are two ways to improve the accuracy of A/D conversion:
Increasing the resolution improves the accuracy of measuring the analog signal's amplitude.
Increasing the sampling rate increases the maximum frequency that can be measured.
General specifications of analog sensor
	1. Range
	2. Accuracy
	3. Linearity
	4. Compatibility
	5. signal conversion capability

## Potentiometer
A potentiometer, informally a pot, is a three-terminal resistor with a sliding or rotating contact that forms an adjustable voltage divider. If only two terminals are used, one end and the wiper, it acts as a variable resistor or rheostat.
Potentiometers are commonly used to control electrical devices such as volume controls on audio equipment. Potentiometers operated by a mechanism can be used as position transducers, for example, in a joystick. Potentiometers are rarely used to directly control significant power (more than a watt), since the power dissipated in the potentiometer would be comparable to the power in the controlled load
CIRCUIT DIAGRAM





![image](https://user-images.githubusercontent.com/36288975/163530788-eec3cdc3-95e8-4d2d-8349-6d0ea4c9439c.png)




## PROCEDURE:

1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select your board (If the board is Arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error, clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device 



## PROGRAM
 ```
int pot;
int led=7;
void setup()
{
  pinMode(led, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  pot=analogRead(A0);
  //Serial.print("Value=");
  Serial.println(pot);
  if(pot>900)
  {  
  
  digitalWrite(led, HIGH);
  delay(500); 
  digitalWrite(led, LOW);
  delay(500);
  }
}
```

## Simulation output:
## OFF CONDITION:
![Screenshot 2024-02-23 155147](https://github.com/guru14789/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/151705853/9fd2cc6e-26d1-4b45-a968-963c3d55eaf9)

## ON CONDITION:


![Screenshot 2024-02-23 155201](https://github.com/guru14789/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/151705853/7fb02a71-690c-4d5f-926c-fd8428f61988)

## GRAPH:
![Screenshot 2024-02-23 155338](https://github.com/guru14789/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/151705853/a51c54ef-496e-4f0a-a344-f44a83169690)

![Screenshot 2024-02-23 155732](https://github.com/guru14789/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/151705853/e5dc2cdf-8550-4ea3-a533-a4780750048f)






## RESULT: 
Arduino uno analog input functioning is learned and interfaced with digital input switch.
