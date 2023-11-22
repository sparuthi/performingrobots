

Repository for "Performing Robots Fall 2023" by Professor Michael Shiloh

## Sketching Assignment with Partner (09/12)

Aadhar and I aimed to develop something both straightforward and imaginative. While exploring ideas at the IM lab, we stumbled upon the humorous concept of "cat-cus." Inspired by this playfulness, we envisioned creating something akin but in the realm of corporate innovation. Thus, we proudly introduce Robo Corp, a playful nod to "Robocop" infused with corporate functionalities.

![Rough sketch](https://github.com/sparuthi/performingrobots/assets/99080736/35130533-be05-4fb5-93b8-3efaa3da12d0)

Date: 12th September, 2023

Partner: Aadhar Wasti 

## Reading Assignment (09/18) 

Chapter 7 of "Entangled: Technology and the Transformation of Performance" by Chris Salter explores the theme of "Machines/Mechanicals" in the context of performance art. In this chapter, Salter delves into the intersection of technology and performance, focusing on the use of machines and mechanical devices as integral elements of artistic expression.

One key concept discussed in this chapter is the idea that machines and mechanical systems in performance art can serve as more than just tools or props. They can become active participants, co-performers, or even autonomous agents, blurring the boundaries between human and machine. This notion challenges traditional notions of authorship, agency, and control within the realm of performance.

What intrigued me the most in this chapter is the exploration of how technology and machines can contribute to the creation of unpredictable and emergent performances. The idea that artists can relinquish some degree of control and allow machines to influence the artistic outcome is fascinating. It highlights the potential for serendipitous and novel experiences in the realm of performance, which may not be achievable through human agency alone. This opens up new possibilities for creativity and pushes the boundaries of what performance can be.

The chapter emphasizes the dynamic relationship between humans and machines in the context of performance art, shedding light on the transformative power of technology in shaping the future of artistic expression. It underscores the idea that embracing the unpredictability and agency of machines can lead to innovative and thought-provoking performances that challenge our perceptions and expectations.

## Base ready (09/12) 

We started with a basic yet essential element: a wooden base. This unpretentious piece of wood became the core of our project, connecting the wheels to our motors and forming the foundation for our Arduino and h-bridge system.

This wooden base was carefully crafted for stability and support, enabling our robot to navigate various terrains effortlessly. The wheels were securely attached to this base, giving our robot its mobility.

On this wooden canvas, we meticulously assembled the intricate components that brought our robot to life. Motors, crucial for movement, were firmly anchored to the base, ready to follow commands from our Arduino controller. The h-bridge, essential for motor control, seamlessly integrated into our system, thanks to the solid platform provided by the wooden base.

As our robot evolved, this unassuming wooden foundation remained crucial, supporting our vision and allowing us to explore the endless possibilities of robotics. It showcased how even the simplest elements could serve as the foundation for innovation and technological progress, blending creativity and engineering seamlessly.


https://github.com/sparuthi/performingrobots/assets/99080736/d55add87-70df-4da5-b9b3-714d33569ee

https://github.com/sparuthi/performingrobots/assets/99080736/f8f98f31-2640-4b4f-a4b1-157a0c75c470

## Adding the caster and making the robot dance (09/14) 

We took an innovative turn by adding casters to our base, giving it mobility. We carefully attached the casters with strong wood and screws, creating exciting possibilities.

As we entered the coding phase, our team was filled with excitement. The challenge of making our base move and dance was thrilling. We coded algorithms to bring our vision to life, turning the code into the conductor of our mechanical dance.

This is the code that we used: 

```
// Defining the pins
const int motor1Pin1 = 2;  // Connect to the input
const int motor1Pin2 = 3;  // Connect to the input
const int motor2Pin1 = 4;  // Connect to the input
const int motor2Pin2 = 5;  // Connect to the input

void setup() {
  // Setting the motor control pins as OUTPUT
  pinMode(motor1Pin1, OUTPUT);
  pinMode(motor1Pin2, OUTPUT);
  pinMode(motor2Pin1, OUTPUT);
  pinMode(motor2Pin2, OUTPUT);
}

void loop() {
  // Moving the motors forward
  digitalWrite(motor1Pin1, HIGH);
  digitalWrite(motor1Pin2, LOW);
  digitalWrite(motor2Pin1, HIGH);
  digitalWrite(motor2Pin2, LOW);

  // Delay for a few seconds
  delay(2000);

  // Stop the motors
  digitalWrite(motor1Pin1, LOW);
  digitalWrite(motor1Pin2, LOW);
  digitalWrite(motor2Pin1, LOW);
  digitalWrite(motor2Pin2, LOW);

  // Delay for a few seconds
  delay(2000);

  // Moving the motors backward
  digitalWrite(motor1Pin1, LOW);
  digitalWrite(motor1Pin2, HIGH);
  digitalWrite(motor2Pin1, LOW);
  digitalWrite(motor2Pin2, HIGH);

  // Delay for a few seconds
  delay(2000);

  // Stop the motors
  digitalWrite(motor1Pin1, LOW);
  digitalWrite(motor1Pin2, LOW);
  digitalWrite(motor2Pin1, LOW);
  digitalWrite(motor2Pin2, LOW);

  // Delay for a few seconds
  delay(2000);
}
```
Seeing our creation come to life was like magic. Our once-static base now moved gracefully, responding to our coded commands.

This blend of mechanics and coding opened up new possibilities and exceeded our expectations. It showcased our teamwork, innovation, and determination to bring our idea to life.

In the end, adding casters and coding for movement turned our project into a captivating spectacle. It proved that combining hardware and software can create truly enchanting results.


https://github.com/sparuthi/performingrobots/assets/99080736/e73078c1-7fce-4a69-bed7-c8547b0b66cd

## Story of a robot using motions (09/25) 

Creating a story using motion alone for a robot with limited capabilities like a plank with three wheels can be a creative challenge. When I look at the stage at which I am at building the robot I get reminded of NASA's Mars Curiosity Rover which inspired me to depict the following story: 

Title: "The Curious Explorer"

Scene 1:
- The robot starts at one end of the room.
- It moves forward with curiosity, exploring its surroundings.

Scene 2:
- The robot suddenly stops and appears to "look" around, changing direction as if it has found something interesting.

Scene 3:
- It moves towards an imaginary object, hesitates for a moment, and then seems to pick it up (you can simulate this with a slight tilting motion).

Scene 4:
- The robot continues its journey, now carrying the "object."

Scene 5:
- It encounters a small obstacle (a raised surface or an object in its path).
- The robot maneuvers around the obstacle, showing determination.

Scene 6:
- The robot reaches its destination, symbolized by a marked spot on the floor.
- It carefully places the "object" down.

Scene 7:
- With a sense of accomplishment, the robot turns around and heads back to its starting point.

This story conveys the idea of a curious robot exploring its environment, discovering something interesting, overcoming obstacles, and finally achieving its mission. 

Here is the code on Arduino for the story: 

```
// Defining motor control pins
int motor1Pin1 = 2; // Motor 1 control pin 1
int motor1Pin2 = 3; // Motor 1 control pin 2
int motor2Pin1 = 4; // Motor 2 control pin 1
int motor2Pin2 = 5; // Motor 2 control pin 2

void setup() {
  // Initialize motor control pins as outputs
  pinMode(motor1Pin1, OUTPUT);
  pinMode(motor1Pin2, OUTPUT);
  pinMode(motor2Pin1, OUTPUT);
  pinMode(motor2Pin2, OUTPUT);
}

void loop() {
  // Start exploring
  moveForward();
  delay(1000); // Move forward for 1 second
  
  // Change direction
  stopMotors();
  delay(500); // Pause for 0.5 seconds
  
  // Continue exploring
  turnRight();
  delay(1000); // Turn right for 1 second
  
  stopMotors();
  delay(500); // Pause for 0.5 seconds
  
  // Overcome an obstacle (simulate with motion)
  moveForward();
  delay(1000); // Move forward for 1 second
  
  // Return to starting point
  turnAround();
  delay(1000); // Turn around for 1 second
}

// Define motor control functions
void moveForward() {
  digitalWrite(motor1Pin1, HIGH);
  digitalWrite(motor1Pin2, LOW);
  digitalWrite(motor2Pin1, HIGH);
  digitalWrite(motor2Pin2, LOW);
}

void turnRight() {
  digitalWrite(motor1Pin1, LOW);
  digitalWrite(motor1Pin2, LOW);
  digitalWrite(motor2Pin1, HIGH);
  digitalWrite(motor2Pin2, LOW);
}

void stopMotors() {
  digitalWrite(motor1Pin1, LOW);
  digitalWrite(motor1Pin2, LOW);
  digitalWrite(motor2Pin1, LOW);
  digitalWrite(motor2Pin2, LOW);
}

void turnAround() {
  digitalWrite(motor1Pin1, LOW);
  digitalWrite(motor1Pin2, HIGH);
  digitalWrite(motor2Pin1, HIGH);
  digitalWrite(motor2Pin2, LOW);
}
```
Here is the video of the story: 


## Hobby RC Remote Control (02/10) 
We linked wheels to a motor and employing a Hobby RC system to control its movements. This endeavor necessitated a meticulous integration process, involving the Arduino Uno, a motor shield, and an H-bridge.

The pivotal step revolved around the assembly of the motor and wheels, ensuring a seamless connection for optimal functionality. The Arduino Uno acted as the central hub, orchestrating the entire operation. To facilitate motor control, I incorporated a motor shield, meticulously soldering it into the H-bridge for enhanced precision and stability.

Utilizing the Hobby RC system, I orchestrated the intricate dance between motor and wheels, fine-tuning the movements with precision. The synergy between the Arduino Uno, motor shield, and H-bridge was instrumental in translating the signals from the Hobby RC system into tangible actions, steering the wheels' motion with finesse.

This intricate process not only unveiled the technical prowess of these components but also highlighted the intricacies of merging hardware elements for a cohesive, controlled outcome. It was a compelling exploration that showcased the harmonious collaboration between hardware and programming for a tangible, controllable output.

[IMG_0925.mov.zip](https://github.com/sparuthi/performingrobots/files/13442393/IMG_0925.mov.zip)
![![IMG_1363](https://github.com/sparuthi/performingrobots/assets/99080736/5283de25-c42f-4c41-be8a-3d6ec64b05b3)
![IMG_1361](https://github.com/sparuthi/performingrobots/assets/99080736/bb0f3977-c054-4080-81ad-fb90b7f7c65e)


Here is the code that we used to test our Hobby RC: 
```
/*
   Minimal decoding of multiple RC channels using pin change interrupts

   Does not check for reasonable values or timeouts

   Based on https://ryanboland.com/blog/reading-rc-receiver-values

  change log

  02 may 2022 - ms - initial entry
  24 may 2022 - ms - changed RC_CHx_PIN names
  15 sep 2022 - ms - changed pin numbers to new assignments

*/



// install this library from the library manager
// by Mike "GreyGnome" Schwager
#include <EnableInterrupt.h>

#define SERIAL_PORT_SPEED 9600
#define RC_NUM_CHANNELS  4

//DON"T CHANGE THIS 
#define RC_CH1  0
#define RC_CH2  1
#define RC_CH3  2
#define RC_CH4  3

#define RC_CH1_PIN  2
#define RC_CH2_PIN  3
#define RC_CH3_PIN  4
#define RC_CH4_PIN  5

uint16_t rc_values[RC_NUM_CHANNELS];
uint32_t rc_start[RC_NUM_CHANNELS];
volatile uint16_t rc_shared[RC_NUM_CHANNELS];

void rc_read_values() {
  noInterrupts();
  memcpy(rc_values, (const void *)rc_shared, sizeof(rc_shared));
  interrupts();
}

void calc_input(uint8_t channel, uint8_t input_pin) {
  if (digitalRead(input_pin) == HIGH) {
    rc_start[channel] = micros();
  } else {
    uint16_t rc_compare = (uint16_t)(micros() - rc_start[channel]);
    rc_shared[channel] = rc_compare;
  }
}

void calc_ch1() {
  calc_input(RC_CH1, RC_CH1_PIN);
}
void calc_ch2() {
  calc_input(RC_CH2, RC_CH2_PIN);
}
void calc_ch3() {
  calc_input(RC_CH3, RC_CH3_PIN);
}
void calc_ch4() {
  calc_input(RC_CH4, RC_CH4_PIN);
}

void setup() {
  Serial.begin(SERIAL_PORT_SPEED);

  pinMode(RC_CH1_PIN, INPUT);
  pinMode(RC_CH2_PIN, INPUT);
  pinMode(RC_CH3_PIN, INPUT);
  pinMode(RC_CH4_PIN, INPUT);

  enableInterrupt(RC_CH1_PIN, calc_ch1, CHANGE);
  enableInterrupt(RC_CH2_PIN, calc_ch2, CHANGE);
  enableInterrupt(RC_CH3_PIN, calc_ch3, CHANGE);
  enableInterrupt(RC_CH4_PIN, calc_ch4, CHANGE);


  pinMode(9,OUTPUT);
  pinMode(10,OUTPUT);
  pinMode(11,OUTPUT);
  pinMode(12,OUTPUT);
}

void loop() {
  rc_read_values();

  Serial.print("CH1:"); Serial.print(rc_values[RC_CH1]); Serial.print("\t");
  Serial.print("CH2:"); Serial.print(rc_values[RC_CH2]); Serial.print("\t");
  Serial.print("CH3:"); Serial.print(rc_values[RC_CH3]); Serial.print("\t");
  Serial.print("CH4:"); Serial.println(rc_values[RC_CH4]);

// use whichever channel is the trigger to control forward and reverse movement
if (rc_values[RC_CH3] < 1000) reverse();
if (rc_values[RC_CH3] > 2000) forward();
if ((rc_values[RC_CH3] > 1400) && (rc_values[RC_CH3] < 1540)) stop();

// use whichever channel is the steering wheel to turn:
if (rc_values[RC_CH4] > 2000) turnRight();

  delay(200);
}

void reverse(){
digitalWrite(9,LOW);
digitalWrite(10,HIGH);
digitalWrite(11,LOW);
digitalWrite(12,HIGH);
}

void forward(){
digitalWrite(9,HIGH);
digitalWrite(10,LOW);
digitalWrite(11,HIGH);
digitalWrite(12,LOW);
}

void turnRight(){
  digitalWrite(9,LOW);
  digitalWrite(10,LOW);
  digitalWrite(11,HIGH);
  digitalWrite(12,LOW);
}

void stop(){
  digitalWrite(9,LOW);
  digitalWrite(10,LOW);
  digitalWrite(11,LOW);
  digitalWrite(12,LOW);
}

```


## Music Maker Shield plays audio (04/10) 

Today was an exciting venture into the realm of music using Arduino's Music Maker Shield. I embarked on this journey to delve into the capabilities of the Music Maker Shield, aiming to play music through an Arduino board. The process unfolded seamlessly, resulting in an enriching experience.

The first step was to acquire a track from the internet, selecting a piece that resonated with my interest. Once downloaded, I proceeded to transfer the track onto the SD card, which would serve as the storage medium for the Music Maker Shield. This step was pivotal as the SD card acts as the repository for audio files accessible by the Music Maker Shield.

With the track securely placed on the SD card, I inserted it into the Music Maker Shield, ready to begin the playback process. Utilizing the 'player_simple' example provided within the Adafruit_VS1053 library, the setup and initialization were straightforward. The example code facilitated the interaction between the Arduino board and the Music Maker Shield, enabling the decoding and playing of audio files stored on the SD card.

As I uploaded the 'player_simple' example onto the Arduino board, the magic unfolded. The Music Maker Shield seamlessly retrieved the audio track from the SD card and initiated playback. It was a moment of sheer joy as the musical notes reverberated through the speakers, filling the room with the chosen melody.

This successful endeavor with the Music Maker Shield not only allowed me to play music using Arduino but also unveiled the incredible potential of incorporating audio into Arduino-based projects. The simplicity and efficiency of the process, coupled with the immersive musical output, affirmed the Music Maker Shield as a versatile tool for audio applications in the Arduino ecosystem.

This experience served as an inspiring introduction to the possibilities that emerge when merging technology, creativity, and music. It encouraged me to explore further avenues where Arduino and the Music Maker Shield can harmoniously converge to create immersive auditory experiences in various projects.

[IMG_1359.MOV.zip](https://github.com/sparuthi/performingrobots/files/13442467/IMG_1359.MOV.zip)

## Building a Demo Robot (09/10) 

Engaging with students from NYUAD Tel Aviv was an enriching experience that encapsulated collaborative learning and creativity. Our endeavor centered around crafting a demo robot, which took the charming form of a cat. Leveraging cardboard and our existing robot base, we meticulously shaped its defining features, infusing it with feline characteristics.

The highlight was bringing our cardboard-crafted cat to life, orchestrating its movements using Hobby RC to animate it and give it the delightful ability to walk around. This hands-on process wasn't just about building a robot; it was an amalgamation of imagination and technical application, a testament to our collective efforts.

During our interaction with the students, we shared insights and lessons gleaned from our class learnings. From discussing foundational concepts to practical applications, the exchange was a forum for knowledge dissemination and collaborative exploration.

Through this collaborative project and knowledge-sharing session, we not only brought a cardboard cat robot to existence but also fostered a vibrant exchange of ideas, bridging our experiences and learnings from our classes with our peers at NYUAD Tel Aviv.

![IMG_6510](https://github.com/sparuthi/performingrobots/assets/99080736/01b1dfe6-09fc-4cf2-8667-581f1e8703f8)
![IMG_9465](https://github.com/sparuthi/performingrobots/assets/99080736/952435b7-8733-4627-9003-56fc628658e8)

## Proposal for the play [in the document seperately] (16/10) 

## Robot Design (28/10) 
In our pursuit of creating Norman, the Robocorp's design, we've embarked on an exciting journey. Our vision for Norman encompasses a multifunctional design, focusing on enhancing both form and function. This robot will boast moveable arms and elbows, facilitating a range of dynamic movements and interactions. The ability to turn its head adds a layer of realism, enhancing its capacity to engage with its environment and users.

Moreover, the incorporation of interactive facial features through four Neopixel matrices signifies a leap forward in its communicative abilities. These features enable Norman to convey emotions, expressions, and messages effectively, establishing a deeper connection with its audience.

This design amalgamates innovative functionalities with a user-centric approach, aiming to create an engaging and lifelike robot capable of meaningful interactions. As we move forward with this blueprint, we're eager to witness Norman's development and its potential to redefine interactive robotics.

Here is our design for the robot: 
![IMG_7316](https://github.com/sparuthi/performingrobots/assets/99080736/44cfcfae-908a-402e-8423-1c5131c4096b)
![IMG_7314](https://github.com/sparuthi/performingrobots/assets/99080736/75e32d8b-bb3f-4795-8d92-696ccccf5235)
![IMG_7313](https://github.com/sparuthi/performingrobots/assets/99080736/60ba27d5-5860-4576-bdc8-94b04964a082)


## Presentation of Paper 1 [in the document seperately] (28/10) 


