# performingrobots

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



