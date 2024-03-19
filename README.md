# Vision Assistive Cane(VAC)
The Vision Assistive Cane project is an innovative assistive technology designed to enhance the independence and safety of individuals with visual impairments.Vision Assistive Cane integrates advanced sensors and connectivity to provide real-time assistance and improve the overall navigation experience for needed people
# About
Traditional white canes serve as mobility aids but lack modern technological features. In response to this limitation, the vision Assistive Cane integrates advanced sensors and connectivity to provide real-time assistance and improve the overall navigation experience for needed people.  The proposed work emphasizes on the cost effectiveness of the smart cane. Existing systems consist of a basic stick or a stick with several sensors and an expensive GPS unit that is difficult for them to carry about and maintain. As technology develops, this smart cane offers a potential way to improve mobility and general quality of life for those with visual impairments since it is lightweight and comfortable to handle.
# Features
* comfortable to use and easy to grip
* lightweight to avoid adding unnecessary weight to the walking stick
* Detects objects within certain range to intimate users
* Produce buzzer sounds to alert the user
# Requirements
* A light wieght cane(Bascially a stick)
* Arduino board
* Ultosonic Sensor
* Buzzer
* Battery(9V)
# Code used
```
const int trigPin = 9;
const int echoPin = 10;
const int buzzer = 11;
const int ledPin = 13;

// defines variables
long duration;
int distance;
int safetyDistance;


void setup() {
pinMode(trigPin, OUTPUT); // Sets the trigPin as an Output
pinMode(echoPin, INPUT); // Sets the echoPin as an Input
pinMode(buzzer, OUTPUT);
pinMode(ledPin, OUTPUT);
Serial.begin(9600); // Starts the serial communication
}


void loop() {
// Clears the trigPin
digitalWrite(trigPin, LOW);
delayMicroseconds(2);

// Sets the trigPin on HIGH state for 10 micro seconds
digitalWrite(trigPin, HIGH);
delayMicroseconds(10);
digitalWrite(trigPin, LOW);

// Reads the echoPin, returns the sound wave travel time in microseconds
duration = pulseIn(echoPin, HIGH);

// Calculating the distance
distance= duration*0.034/2;

safetyDistance = distance;
if (safetyDistance <= 5){
  digitalWrite(buzzer, HIGH);
  digitalWrite(ledPin, HIGH);
```
# System Architecture
![image](https://github.com/sanjay1325/Vision-assistive-cane-VAC-/assets/112951070/8703c19f-723c-442f-a223-6f14768903db)
# Output
![image](https://github.com/sanjay1325/Vision-assistive-cane-VAC-/assets/112951070/721105f6-1097-4824-9853-3838085a6df0)
![image](https://github.com/sanjay1325/Vision-assistive-cane-VAC-/assets/112951070/50c869b6-03ef-4ab5-84c2-fc785aae5006)
# Results and impacts
After conducting functional testing, physical testing, and user testing, the VAC walking stick was found to be accurate and responsive, durable and safe for regular use, and comfortable and easy to usage by people who are  blind.Environmental testing also showed that the walking stick performed well under different temperature and humidity conditions.The blind stick described in this study can help a person with low vision navigate a different surfaces and obstacles. The cane can also alert the user's carers of their whereabouts at times of emergency or other problem. An RF remote control can also be used to locate the stick. High-performing sensors and microscopic scale may be added to this to further enhance the design and reduce the amount of space required on the stick. To ensure that the sensor angles always point straight instead of at a fixed angle, a few little tweaks to their arrangement may be done to make them adapt based on the angle of the stick in relation to the ground. 

Machine learning algorithms, which can evaluate and interpret sensor data to give the user real-time situational awareness, can be added to the suggested blind stick to improve it. The stick can detect impediments and changes in terrain by using computer vision and image processing techniques. It can also provide the user haptic input via vibrating motors. Additionally, the stick may interface with a user's smartphone to exchange extra data and support by integrating Bluetooth Low Energy (BLE) technology. By adding GPS technology, which can provide carers the user's exact position in an emergency, the stick's notification system may also be made even better. The suggested blind stick can give people with visual challenges  more thorough and user-friendly navigating experience by using these cutting-edge technology.

# Refrences
1.	R. K. Kaushal, K. Tamilarasi, P. Babu, T. A. Mohanaprakash, S. E. Murthy and M. J. Kumar, "Smart Blind Stick for Visually Impaired People using IoT," 2022 International Conference on Automation, Computing and Renewable Systems (ICACRS), Pudukkottai, India, 2022, pp. 296-300.
2.	A. Shaha, S. Rewari and S. Gunasekharan, "SWSVIP-Smart Walking Stick for the Visually Impaired People using Low Latency Communication," 2018 International Conference on Smart City and Emerging Technology (ICSCET), Mumbai, India, 2018, pp. 1-5,
3.	K. Suresh, P. J, J. C, R. K, K. K and A. R, "Smart Assistive Stick for Visually Impaired Person with Image Recognition," 2022 International Conference on Power, Energy, Control and Transmission Systems (ICPECTS), Chennai, India, 2022, pp. 1-5,



