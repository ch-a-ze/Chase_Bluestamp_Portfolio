# Gyro-Controlled Drawing Robot

I'm building a two-wheeled robot that draws using gyroscope-based heading correction instead of stepper-driven rails. It runs on an Arduino Uno R3, using a BNO055 IMU to hold accurate headings, quadrature-encoded motors to track distance, an HC-05 Bluetooth module to receive commands, and a servo to lift and lower the pen. Right now I'm in the thick of getting the circuit fully working, from soldering the gyro board to testing the servo and motors on a breadboard.

<!---
You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
-->

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Chase L | Mtn View | Electrical Engineering | Incoming Junior |

<!--- Replace the BlueStamp logo below with an image of yourself and your completed project once you have one. -->
![Headstone Image](logo.svg)

<!---
# Final Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE
-->

<!---
# Second Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone
-->

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

My project is a gyro-controlled drawing robot: a two-wheeled plotter built around an Arduino Uno R3, a BNO055 IMU for heading, quadrature-encoded N20 motors for distance tracking, an HC-05 Bluetooth module for wireless commands, and an SG90 micro servo to lift and lower the pen. A TB6612FNG motor driver controls the two drive motors, and everything runs off a 9V battery stepped down to 6V for the motors and servo.

After finishing my starter project (an RGB slider that never quite worked, but taught me a lot about troubleshooting), I moved into planning the drawing robot. I got my build plan approved, mapped out where every part needed to go, and started soldering, getting the BNO055 and the I2C logic level shifter onto their pins. From there I built out the circuit on a breadboard and worked through it piece by piece: I got the servo running cleanly first, then moved on to wiring in the motors.

The biggest challenge has been the sheer complexity of the circuit. I hadn't built anything this involved on my own before, and there were a lot of ways for things to go wrong: a shaky common ground, a servo that kept throwing errors, and parts that worked fine on the Arduino Uno but needed extra troubleshooting when I was testing with a Nano ESP32. Multimeters became my best friend this week.

Before my next milestone, I still need to:
- Finalize the circuit and move it from the breadboard onto a soldered perfboard
- Get the motors fully wired in and running, not just the servo
- Start coding the motors so the wheels actually turn
- Mount everything onto the base once the wiring is solid

<!---
# Schematics
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resources to create professional schematic diagrams, though BSE recommends Tinkercad because it can be done easily and for free in the browser.
-->

<!---
# Code
Here's where you'll put your code once you have it written.
```c++
void setup() {
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {

}
```
-->

# Bill of Materials

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino UNO R3 | Main microcontroller that runs the plotter and the g-code interpreter | $28 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| BNO055 Sensor Fusion Module | 9-axis IMU/gyro used for accurate heading and turns | $20 | <a href="https://www.amazon.com/GY-BNO055-Absolute-Orientation-Breakout-Gyroscope/dp/B0CKS1W63K"> Link </a> |
| N20 6V 60 RPM DC Motor with Encoder (x2) | Drive motors for the two wheels; encoders track distance | $18 | <a href="https://www.amazon.com/Gearmotor-Robotics-Encoder-Replacement-150-3000RPM/dp/B0GDV14XL5"> Link </a> |
| TB6612FNG Motor Driver | Controls speed/direction of the two N20 motors | $8 | <a href="https://www.amazon.com/NOYITO-Driver-TB6612FNG-Arduino-Microcontroller/dp/B07DS2FG8K"> Link </a> |
| HC-05 Bluetooth Module | Wireless connection to send drawings/commands from a PC or phone | $8 | <a href="https://www.amazon.com/HiLetgo-Wireless-Bluetooth-Transceiver-Arduino/dp/B071YJG8DR"> Link </a> |
| SG90 Micro Servo | Pen-lift mechanism (raises and lowers the pen) | $4 | <a href="https://www.amazon.com/s?k=SG90+micro+servo"> Link </a> |
| I2C Logic Level Shifter | Shifts 3V/5V logic for the BNO055 I2C connection | $3 | <a href="https://www.amazon.com/s?k=I2C+logic+level+converter+bi-directional"> Link </a> |
| 6V Voltage Regulator | Regulated 6V rail for the motors and servo | $3 | <a href="https://www.amazon.com/s?k=6V+voltage+regulator+module"> Link </a> |
| 9V Battery | Powers the Arduino and the 6V regulator | $5 | <a href="https://www.amazon.com/s?k=9V+battery"> Link </a> |
| 1N4007 Diode | Reverse-polarity protection on the power input | $1 | <a href="https://www.amazon.com/s?k=1N4007+diode"> Link </a> |
| Toggle Switch | Main on/off power switch | $3 | <a href="https://www.amazon.com/s?k=SPDT+toggle+switch"> Link </a> |
| Screw Terminal Block | Connection point for the 9V power input wires | $2 | <a href="https://www.amazon.com/s?k=2+pin+screw+terminal+block+5mm"> Link </a> |
| Jumper / Hookup Wire | Wiring between all components | $7 | <a href="https://www.amazon.com/s?k=dupont+jumper+wire+kit"> Link </a> |
| Acrylic Sheet (base) | Flat platform that all components bolt onto | $8 | <a href="https://www.amazon.com/s?k=acrylic+sheet"> Link </a> |
| Wheels (x2) | Driven by the N20 motors to move the plotter | $5 | <a href="https://www.amazon.com/s?k=N20+motor+wheels"> Link </a> |
| Misc. Hardware (screws, bolts, nuts) | Mounts servo bracket, motors, and other parts | $5 | <a href="https://www.amazon.com/s?k=M2+M3+screw+standoff+assortment+kit"> Link </a> |
| 3D Printed Parts (pen-lift assembly, battery tray, 2 glides) | Printed from the included STL files; cost is filament only | $2 | <a href="https://www.instructables.com/Gyro-Controlled-Robot-Plotter/"> STL files </a> |
| Pencil / Fibre-tip Pen | The drawing instrument held by the pen-lift tube | $1 | <a href="https://www.amazon.com/s?k=pencil"> Link </a> |

<!--- Estimated total: ~$131 at the prices above. -->
