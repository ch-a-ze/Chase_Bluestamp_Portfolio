# Bluestamp Engineering Drawing Robot
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| FirstName LastInitialOnly | School Name | Electrical Engineering | Incoming Senior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 

# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your first milestone, describe what your project is and how you plan to build it. You can include:
- An explanation about the different components of your project and how they will all integrate together
- Technical progress you've made so far
- Challenges you're facing and solving in your future milestones
- What your plan is to complete your project

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials

<!--- Prices below are typical hobbyist estimates and will vary by seller. Replace each price and the Link with the actual item and price you purchased. -->

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

<!--- Estimated total: ~$131 at the prices above. The original project lists an estimated cost of under $100 excluding shipping, so your total will depend on which clone/branded parts you buy. -->

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
