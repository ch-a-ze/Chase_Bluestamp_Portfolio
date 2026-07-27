# Bluestamp Engineering Drawing Robot

This is a drawing robot that uses a gyroscope to steer itself as it moves, so it can trace shapes and drawings onto paper. It runs on an Arduino Nano ESP32 and brings together a few different systems: motors with encoders, a gyro to track direction, a servo to lift the pen, and a bluetooth website to send it commands. 

<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Chase L | Mtn View | Electrical Engineering | Incoming Junior |

<!--- Replace the logo below with a photo of yourself and your project once it's further along. Guide: https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html -->

![Bluestamp Engineering Logo](Logo2.svg)

<!--- Second Milestone and Final Milestone are commented out until they're done. The section headers and videos are kept so the structure stays in place. -->

<!---
# Final Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE
-->

# Final Milestone

My final milestone was the finished drawing robot. It is able to interpret g-code and draw based on it's instructions. This changes for this milestone were done mostly on the software side, with a few tweaks made to the robot itself. The most notable of these tweaks were finding a perfectly-sized screw to mount into the motor holders and to stop the motor from shifting around. Another major hardware tweak was switching out the normal HB Ticonderoga pencil for a specialized 8B pencil, making it show up as a much bolder line that reduces friction. The rest was pretty much software and a ton of calibration, adjusting variables such as COUNTS_PER_MM to track distance and Backlash for adjusting the degrees for each individual motor.



# Second Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/yjryAOpf4do?si=zad5AjHtgDM9Otye" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My second milestone was a fully functional, wired robot that had all the major components in place, such as the pencil lift, the breadboards, and the DC Motors. This was a big change from the first milestone where I just had a breadboard with a bunch of wires providing connection, but there was no actual robot that could function. Now, the website my arduino shares allows me to send it commands to move forward/backward, turn both directions, lift/lower the pencil using the servo motor, and track distance traveled using the encoders. Here is what my website looks like at the second milestone:


A huge part of this milestone was attaching the components to the base of the robot. I'm using an acrylic base, and initially I was going to go put the wheels on the longer sides of the robot, but due to poor measurements, I had to reformat so the robot drives straight. It's now much wider than it is long, but it has the pen lift directly in the center so it can spin around the tip as a pivot point. One other thing that I did was change it from one long breadboard to two mini breadboards, which involved rewiring every single connection.

Another challenge was that the wheels kept getting stuck. This was because the initial motor mounts that I had didn't stop the wheels from rubbing against the base, creating enough friction to stop them from turning altogether. I had to go back and re-cad the mounts and get them reprinted in order to keep the robot running smoothly.

<!--- Before/after swapper for the motor mount. Click the arrows to flip between
      the original mount and the re-CADded one. Every image is in the DOM the
      whole time, only the active one is shown. -->

<div class="swap" data-i="0">
  <img class="swap-img is-on" src="BluestampMotorMount.png" alt="Original motor mount, wheels rubbing the base">
  <img class="swap-img" src="CADMotorMount.png" alt="Re-CADded motor mount with clearance">

  <button class="swap-arrow swap-prev" aria-label="Previous image">&#10094;</button>
  <button class="swap-arrow swap-next" aria-label="Next image">&#10095;</button>

  <span class="swap-label">Before</span>
</div>

<!--- The labels the swapper cycles through, in the same order as the images -->
<script>window.swapLabels = ["Before", "After"];</script>

For the next milestone, I'm going to have to dive into the software a lot, and work on converting drawings into shapes. I'm also going to have to calibrate pretty much every part of the robot to ensure it is as accurate as possible in making drawings.


# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/nFOEWR1XK8A?si=o8Ssw78IqVJhE14k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My first milestone was planning out the full build and getting all the electronics figured out before putting the robot together.

The robot has a few main parts that all have to work with each other. The Arduino Nano is the brain that controls everything. Two N20 motors with encoders drive the wheels and keep track of how far the robot has moved. A BNO055 gyro measures which way the robot is facing so it can turn accurately. An SG90 servo raises and lowers the pencil/drawing utensil, a L9110 motor driver sits between the Arduino and the motors and controls their speed and direction.

The biggest challenge at this stage was getting started. Initially, the wiring diagrams looked way too complicated to understand, so it took a few days to really start to get it, and I didn't start wiring with the breadboard until about a week in. However, it wasn't just the wires. I also had to figure out what all the parts I mentioned above actually did. We were also initially going to use an Arduino UNO, TB6612FNG motor driver, and an HC-05 for bluetooth, but we switched all of those things out for the ESP32 nano & L9110 driver, so I had to get a deeper understanding of how to wire them. Eventually, I did get it and now I have a fully functioning circuit:

<!--- Two-up grid -->
<div class="img-grid">
  <figure>
    <img src="SideViewLongBreadboard.jpg" alt="Completed circuit, side view">
    <figcaption>Completed circuit, side view</figcaption>
  </figure>
  <figure>
    <img src="TopviewLongBreadboard.jpg" alt="Completed circuit, top view">
    <figcaption>Completed circuit, top view</figcaption>
  </figure>
</div>

For my next milestones I plan to attach everything to the base (involves transferring the entire circuit to two smaller breadboards), get the motors and gyro working together so the robot can drive straight, and then attach the pen-lift so it can actually draw.

# Schematics

<!--- Add your schematic image here once it's made. Tinkercad (https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and Fritzing (https://fritzing.org/learning/) are both good options. BSE recommends Tinkercad since it runs free in the browser. -->
![Full circuit diagram, completed version](FullCircuitDiagramChase.svg){: .plate }

# Code

## Code at Milestone II

```cpp
#include <WiFi.h>
#include <WebServer.h>
#include <Wire.h>
#include <Adafruit_Sensor.h>
#include <Adafruit_BNO055.h>
#include <Servo.h>

//Wi-Fi Configuration
const char* ssid     = "WIFI_NETWORK";
const char* password = "WIFI_PASSWORD";

WebServer server(80); 

//Hardware Pin Assignments (Nano ESP32 Layout)
const int A1A = 6;  
const int A1B = A0; 
const int B1A = A1; 
const int B1B = 11;

const int encA1 = 2; 
const int encA2 = 4; 
const int encB1 = 3; 
const int encB2 = 5; 

volatile long encACount = 0;
volatile long encBCount = 0;

//Distance tracking - needs to be calibrated
const float COUNTS_PER_MM = 3.7;   //encoder counts per 1 mm of travel

//Sensor & Control Variables
Adafruit_BNO055 bno = Adafruit_BNO055(55);
float targetHeading = 0.0;
const float Kp = 3.5;       
int baseSpeed = 100;
const int MOTOR_TRIM = 0;   //+ boosts motor A to match B - tune until it drives straight open-loop
int rampSpeed = 0;              //working speed during a controlled stop
const int STOP_STEP = 8;        //how fast the ramp bleeds off - lower = gentler
const int STOP_FLOOR = 40;      //brake once it is below motor deadband is 
int motorState = 0; //0 = Stop, 1 = Drive Straight, 2 = Left, 3 = Right

//Servo (pen-lift) setup
Servo penServo;
const int SERVO_PIN  = 10;   //D10  
const int SERVO_UP   = 25+90;   //pen up - straight-up position
const int SERVO_DOWN = 25;    //pen down - 90 deg to sideways
bool servoDown = false;      //tracks which position the servo is in

void setup() {
  Serial.begin(115200);
  
  pinMode(A1A, OUTPUT); pinMode(A1B, OUTPUT);
  pinMode(B1A, OUTPUT); pinMode(B1B, OUTPUT);
  
  pinMode(encA1, INPUT_PULLUP); pinMode(encA2, INPUT_PULLUP);
  pinMode(encB1, INPUT_PULLUP); pinMode(encB2, INPUT_PULLUP);
  
  attachInterrupt(digitalPinToInterrupt(encA1), ISR_A, CHANGE);
  attachInterrupt(digitalPinToInterrupt(encB1), ISR_B, CHANGE);

  //home the servo straight-up, then detach so it stops buzzing/drawing current
  penServo.attach(SERVO_PIN, 1000, 2000);
  penServo.write(SERVO_UP);
  delay(400);              //let it actually reach the position
  penServo.detach();       //cut the pulses - servo goes quiet and limp

  if(!bno.begin()) {
    Serial.println("No BNO055 detected! Check I2C wiring.");
    while(1);
  }
  delay(500);
  bno.setExtCrystalUse(true);

  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) {
    delay(500);
    Serial.print(".");
  }
  Serial.println("\n Wi-Fi Connected!");
  Serial.print("Robot IP Address: http://");
  Serial.println(WiFi.localIP());

  //Web Server Route Bindings
  server.on("/", handleRoot);
  server.on("/forward", handleForward);
  server.on("/backward", handleBackward);
  server.on("/left", handleLeft);
  server.on("/right", handleRight);
  server.on("/stop", handleStop);
  server.on("/telemetry", handleTelemetry); 
  server.on("/reset", handleReset);
  server.on("/faster", handleFaster);
  server.on("/slower", handleSlower);
  server.on("/servo", handleServo);


  
  server.begin(); 
}

void loop() {
  server.handleClient(); 

  if (motorState == 1) { //DRIVE STRAIGHT (Using Gyro Loop)
    sensors_event_t event;
    bno.getEvent(&event);
    float currentHeading = event.orientation.x;
    
    float error = targetHeading - currentHeading;
    if (error > 180)  error -= 360;
    if (error < -180) error += 360;

    int correction = error * Kp;
    setMotorA(baseSpeed - correction + MOTOR_TRIM, true);
    setMotorB(baseSpeed + correction, true);

  } 
  else if (motorState == 2) { //TURN LEFT
    setMotorA(baseSpeed, true); 
    setMotorB(baseSpeed, false);
  }
  else if (motorState == 3) { //TURN RIGHT
    setMotorA(baseSpeed, false); 
    setMotorB(baseSpeed, true);
  }
  else if (motorState == 4) { //DRIVE BACKWARD (Gyro Loop)
    sensors_event_t event;
    bno.getEvent(&event);
    float currentHeading = event.orientation.x;

    float error = targetHeading - currentHeading;
    if (error > 180)  error -= 360;
    if (error < -180) error += 360;

    int correction = error * Kp;
    setMotorA(baseSpeed + correction, false);
    setMotorB(baseSpeed - correction, false);
  }
  else if (motorState == 5) { //CONTROLLED STOP - forward (hold heading while slowing)
    sensors_event_t event;
    bno.getEvent(&event);
    float currentHeading = event.orientation.x;

    float error = targetHeading - currentHeading;
    if (error > 180)  error -= 360;
    if (error < -180) error += 360;

    int correction = error * Kp * (rampSpeed / (float)baseSpeed);   //scale with speed so it can't dominate as we slow
    setMotorA(rampSpeed - correction + MOTOR_TRIM, true);
    setMotorB(rampSpeed + correction, true);

    rampSpeed -= STOP_STEP;
    if (rampSpeed <= STOP_FLOOR) { motorState = 0; setMotorA(0, true); setMotorB(0, true); }
  }
  else if (motorState == 6) { //CONTROLLED STOP - backward (ramp down in reverse)
    sensors_event_t event;
    bno.getEvent(&event);
    float currentHeading = event.orientation.x;

    float error = targetHeading - currentHeading;
    if (error > 180)  error -= 360;
    if (error < -180) error += 360;

    int correction = error * Kp * (rampSpeed / (float)baseSpeed);   //scale with speed so it can't dominate as we slow
    setMotorA(rampSpeed - correction + MOTOR_TRIM, true);
    setMotorB(rampSpeed + correction, true);

    rampSpeed -= STOP_STEP;
    if (rampSpeed <= STOP_FLOOR) { motorState = 0; setMotorA(0, true); setMotorB(0, true); }
  }
  delay(20);
}

//UI coding
void handleRoot() {
  String html = "<!DOCTYPE html><html><head>";
  //setup
  html += "<meta name='viewport' content='width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no'>";
  html += "<title>ROBOT CONTROL</title>";
  html += "<style>";
  html += "* { box-sizing: border-box; margin: 0; padding: 0; }";
  html += "html, body { width: 100%; height: 100%; background-color: #010307; font-family: 'Segoe UI', Arial, sans-serif; overflow: hidden; display: flex; align-items: center; justify-content: center; }";
  html += "#bgCanvas { position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1; pointer-events: none; }";
  html += ".dashboard { position: relative; z-index: 2; width: 92%; max-width: 500px; padding: 35px 25px; background: rgba(2, 5, 12, 0.92); border: 2px solid #00aaff; box-shadow: 0 0 35px rgba(0, 170, 255, 0.4); border-radius: 14px; backdrop-filter: blur(8px); text-align: center; }";
  
  //red status bar at top
  html += ".status-bar { width: 100%; padding: 14px; margin-bottom: 25px; border-radius: 8px; font-weight: bold; font-size: 15px; letter-spacing: 2px; text-transform: uppercase; border: 1px solid #f44336; color: #ff5252; background: rgba(244, 67, 54, 0.15); transition: all 0.3s ease; }";
  html += ".status-bar.active { border: 1px solid #00ffdd; color: #00ffdd; background: rgba(0, 255, 221, 0.15); box-shadow: 0 0 15px rgba(0,255,221,0.2); }";
  
  //button configurations
  html += ".control-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-bottom: 20px; }";
  html += ".drive-row, .stop-row { grid-column: span 2; }";
  html += ".btn { display: block; width: 100%; padding: 20px; font-size: 18px; font-weight: 800; text-transform: uppercase; letter-spacing: 2px; text-decoration: none; border-radius: 8px; border: 2px solid transparent; transition: all 0.2s ease; cursor: pointer; user-select: none; -webkit-user-select: none; }";
  html += ".btn-drive { color: #02050d; background-color: #00ffdd; box-shadow: 0 0 20px rgba(0, 255, 221, 0.4); }";
  html += ".btn-turn { color: #ffffff; background-color: rgba(0, 136, 255, 0.25); border-color: #0088ff; box-shadow: 0 0 15px rgba(0, 136, 255, 0.2); }";
  html += ".btn-stop { color: #ffffff; background-color: #e63946; box-shadow: 0 0 20px rgba(230, 57, 70, 0.4); }";
  html += ".btn:hover { transform: translateY(-2px); filter: brightness(1.2); }";
  html += ".btn:active { transform: translateY(1px); }";
  html += ".telemetry { margin-top: 20px; font-size: 13px; color: #526d82; letter-spacing: 1px; font-family: monospace; }";
  html += "</style></head><body>";
  
  html += "<canvas id='bgCanvas'></canvas>";
  
  //updates status bar when buttons clicked
  html += "<div class='dashboard'>";
  html += "<div id='statusText' class='status-bar'>STATUS: STOPPED</div>";
  
  html += "<div class='control-grid'>";
  html += "<div class='drive-row'><button onclick='sendCommand(\"/forward\",\"STATUS: DRIVING\")' class='btn btn-drive'>Drive</button></div>";
  html += "<div class='drive-row'><button onclick='sendCommand(\"/backward\",\"STATUS: REVERSING\")' class='btn btn-turn'>Backward</button></div>";
  html += "<div><button onclick='sendCommand(\"/left\",\"STATUS: TURNING LEFT\")' class='btn btn-turn'>Turn Left</button></div>";
  html += "<div><button onclick='sendCommand(\"/right\",\"STATUS: TURNING RIGHT\")' class='btn btn-turn'>Turn Right</button></div>";
  html += "<div class='stop-row'><button onclick='sendCommand(\"/stop\",\"STATUS: STOPPED\")' class='btn btn-stop'>Stop</button></div>";
  html += "<div class='stop-row'><button onclick='sendCommand(\"/reset\",\"STATUS: STOPPED\")' class='btn btn-turn'>Reset Distance</button></div>";
  //toggles pen between up and sideways - empty label so status bar is untouched
  html += "<div class='stop-row'><button onclick='sendCommand(\"/servo\",\"\")' class='btn btn-turn'>Toggle Pen</button></div>";
  html += "<div><button onclick='sendCommand(\"/slower\",\"\")' class='btn btn-turn'>Slower</button></div>";
  html += "<div><button onclick='sendCommand(\"/faster\",\"\")' class='btn btn-turn'>Faster</button></div>";
  html += "</div>";
  

  html += "<div id='distanceText' class='telemetry' style='font-size:16px; color:#00ffdd; margin-bottom:6px;'>DISTANCE: 0.0 cm</div>";
  html += "<div id='telemetryText' class='telemetry'>ENC_A: 0 | ENC_B: 0</div>";
  html += "</div>";
  
  //moving dot network
  html += "<script>";
  html += "const canvas = document.getElementById('bgCanvas'); const ctx = canvas.getContext('2d');";
  html += "let points = []; ";
  html += "const numPoints = 120; "; 
  html += "const maxDist = 300; "; 
  
  html += "function init() { ";
  html += "  canvas.width = window.innerWidth; canvas.height = window.innerHeight; points = []; ";
  html += "  for(let i=0; i<numPoints; i++) { ";
  html += "    let isRedNet = (i > numPoints * 0.52); "; 
  html += "    points.push({ ";
  html += "      x: Math.random()*canvas.width, y: Math.random()*canvas.height, ";
  //micro-adjustment to speed to keep vectors crisp
  html += "      vx: (Math.random()-0.5)*0.5, vy: (Math.random()-0.5)*0.5, ";
  html += "      type: isRedNet ? 'red' : 'cyan' ";
  html += "    }); ";
  html += "  } ";
  html += "}";
  
  html += "function draw() { ";
  html += "  ctx.clearRect(0, 0, canvas.width, canvas.height);";
  html += "  for(let i=0; i<numPoints; i++) { ";
  html += "    let p = points[i]; p.x += p.vx; p.y += p.vy; ";
  html += "    if(p.x<0||p.x>canvas.width) p.vx*=-1; if(p.y<0||p.y>canvas.height) p.vy*=-1;";
  
  html += "    ctx.fillStyle = (p.type === 'red') ? '#ff2233' : '#00ffdd'; ";
  html += "    ctx.beginPath(); ctx.arc(p.x, p.y, p.type === 'red' ? 2.5 : 2.0, 0, Math.PI*2); ctx.fill();";
  
  html += "    for(let j=i+1; j<numPoints; j++) { ";
  html += "      let p2 = points[j]; ";
  html += "      if(p.type === p2.type) { "; 
  html += "        let dist = Math.hypot(p.x-p2.x, p.y-p2.y);";
  html += "        if(dist < maxDist) { ";
  //opacity formula for the dots
  html += "          let alpha = (1 - dist/maxDist) * 0.65; "; 
  html += "          ctx.strokeStyle = (p.type === 'red') ? `rgba(255, 45, 15, ${alpha})` : `rgba(0, 160, 255, ${alpha})`; ";
  html += "          ctx.lineWidth = 1.5; "; // Thickened from 1 to 1.5 for presence
  html += "          ctx.beginPath(); ctx.moveTo(p.x, p.y); ctx.lineTo(p2.x, p2.y); ctx.stroke(); ";
  html += "        } ";
  html += "      } ";
  html += "    } ";
  html += "  } ";
  html += "  requestAnimationFrame(draw); ";
  html += "}";
  
  html += "window.addEventListener('resize', init); init(); draw();";
  
  html += "function sendCommand(route, labelText) {";
  html += "  fetch(route);";
  html += "  if(labelText === '') return;";        // speed buttons: fire request, don't touch status
  html += "  const sBox = document.getElementById('statusText');";
  html += "  sBox.innerText = labelText;";
  html += "  if(labelText.includes('STOPPED')) sBox.classList.remove('active'); else sBox.classList.add('active');";
  html += "}";

  
  html += "setInterval(() => {";
  html += "  fetch('/telemetry').then(res => res.json()).then(data => {";
  html += "    let cmA = (data.da/10).toFixed(1); let cmB = (data.db/10).toFixed(1); let cmAvg = (data.dist/10).toFixed(1);";
  html += "    document.getElementById('distanceText').innerText = `DISTANCE: ${cmAvg} cm  (A ${cmA} | B ${cmB})`;";
  html += "    document.getElementById('telemetryText').innerText = `ENC_A: ${data.a} | ENC_B: ${data.b}`;";
  html += "    document.getElementById('telemetryText').innerText = `SPD: ${data.spd} | ENC_A: ${data.a} | ENC_B: ${data.b}`;";
  html += "    const sBox = document.getElementById('statusText');";
  html += "    if(data.s == 0) { sBox.innerText = 'STATUS: STOPPED'; sBox.classList.remove('active'); }";
  html += "    else if(data.s == 1) { sBox.innerText = 'STATUS: DRIVING'; sBox.classList.add('active'); }";
  html += "    else if(data.s == 2) { sBox.innerText = 'STATUS: TURNING LEFT'; sBox.classList.add('active'); }";
  html += "    else if(data.s == 3) { sBox.innerText = 'STATUS: TURNING RIGHT'; sBox.classList.add('active'); }";
  html += "    else if(data.s == 4) { sBox.innerText = 'STATUS: REVERSING'; sBox.classList.add('active'); }";
  html += "  });";
  html += "}, 300);"; 
  html += "</script></body></html>";
  
  server.send(200, "text/html", html);
}

//background directional controls
void handleForward() {
  sensors_event_t event;
  bno.getEvent(&event);
  targetHeading = event.orientation.x; 
  motorState = 1;
  server.send(200, "text/plain", "OK"); 
}

void handleBackward() {
  sensors_event_t event;
  bno.getEvent(&event);
  targetHeading = event.orientation.x;
  motorState = 4;
  server.send(200, "text/plain", "OK");
}

void handleLeft()  { motorState = 2; server.send(200, "text/plain", "OK"); }
void handleRight() { motorState = 3; server.send(200, "text/plain", "OK"); }

//stopping
//stopping - pick the right controlled stop based on how we were moving
void handleStop() {
  sensors_event_t event;
  bno.getEvent(&event);

  if (motorState == 1) {          //was driving forward
    targetHeading = event.orientation.x;
    rampSpeed = baseSpeed;
    motorState = 5;               //5 = controlled stop, forward
  }
  else if (motorState == 4) {     //was driving backward
    targetHeading = event.orientation.x;
    rampSpeed = baseSpeed;
    motorState = 6;               //6 = controlled stop, backward
  }
  else {                          //turning or already stopped - just brake
    motorState = 0;
    setMotorA(0, true);
    setMotorB(0, true);
  }
  server.send(200, "text/plain", "OK");
}


//servo toggle - flips the pen between up and sideways
void handleServo() {
  servoDown = !servoDown;
  penServo.attach(SERVO_PIN, 1000, 2000);   //re-attach for the move
  if (servoDown) {
    penServo.write(SERVO_DOWN);   //rotate down to sideways
  } else {
    penServo.write(SERVO_UP);     //back to straight-up
  }
  delay(400);                     //give it time to actually get there
  penServo.detach();              //stop pulsing so it stops buzzing/drawing
  server.send(200, "text/plain", "OK");
}


void handleTelemetry() {
  float distA   = encACount / COUNTS_PER_MM;      // mm
  float distB   = encBCount / COUNTS_PER_MM;      // mm
  float distAvg = (distA + distB) / 2.0;          // mm (forward travel)

  String json = "{\"a\":" + String(encACount) +
                ",\"b\":" + String(encBCount) +
                ",\"da\":" + String(distA, 1) +
                ",\"db\":" + String(distB, 1) +
                ",\"dist\":" + String(distAvg, 1) +
                ",\"spd\":" + String(baseSpeed) +
                ",\"s\":" + String(motorState) + "}";
  server.send(200, "application/json", json);
}

void handleReset() {
  noInterrupts();
  encACount = 0;
  encBCount = 0;
  interrupts();
  server.send(200, "text/plain", "OK");
}

//Core Motor Phase Controls
void setMotorA(int speed, bool forward) {
  speed = constrain(speed, 0, 255);
  if (forward) {
    digitalWrite(A1B, HIGH);
    analogWrite(A1A, 255 - speed);
  } else {
    digitalWrite(A1B, LOW);
    analogWrite(A1A, speed);
  }
}

void setMotorB(int speed, bool forward) {
  speed = constrain(speed, 0, 255);
  if (forward) {
    digitalWrite(B1A, LOW);
    analogWrite(B1B, speed);
  } else {
    digitalWrite(B1A, HIGH);
    analogWrite(B1B, 255 - speed);
  }
}

//speed controls
void handleFaster() {
  baseSpeed = constrain(baseSpeed + 20, 60, 255);
  server.send(200, "text/plain", "OK");
}
void handleSlower() {
  baseSpeed = constrain(baseSpeed - 20, 60, 255);
  server.send(200, "text/plain", "OK");
}

//Interrupt Service Routines (monitors sensor pins for the main loop)
void ISR_A() {
  if (digitalRead(encA1) == digitalRead(encA2)) {
    encACount++;
  } else {
    encACount--;
  }
}

void ISR_B() {
  if (digitalRead(encB1) == digitalRead(encB2)) {
    encBCount--;
  } else {
    encBCount++;
  }
}

```

# Bill of Materials

<!--- Prices below are typical hobbyist estimates and will vary by seller. Replace each price and the Link with the actual item and price you purchased. -->

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino NANO ESP32 | Main microcontroller that runs the plotter and the g-code interpreter | $20 | <a href="https://store-usa.arduino.cc/products/nano-esp32-with-headers?utm_source=google&utm_medium=cpc&utm_campaign=US-Pmax&gad_source=1&gad_campaignid=21317508903&gbraid=0AAAAACbEa85s_ViD5yIHHsZGsDyVVrjz4&gclid=CjwKCAjwpK3SBhASEiwAtV1SPNicdazsvQfAH9B3H2CtwpTZcjwmq57zrKEi2BHB2wUEBoWZIpqFXhoCz2MQAvD_BwE"> Link </a> |
| BNO055 Sensor Fusion Module | 9-axis IMU/gyro used for accurate heading and turns | $35 | <a href="https://www.adafruit.com/product/2472"> Link </a> |
| N20 6V 60 RPM DC Motor with Encoder (x2) | Drive motors for the two wheels; encoders track distance | $18 | <a href="https://www.amazon.com/Gearmotor-Robotics-Encoder-Replacement-150-3000RPM/dp/B0GDV14XL5"> Link </a> |
| L9110 Motor Driver | Controls speed/direction of the two N20 motors | $2 | <a href="https://www.aliexpress.us/item/3256808109455456.html?src=google&snps=y&src=google&albch=shopping&acnt=708-803-3821&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=UneMJZVf&gclsrc=aw.ds&albagn=888888&ds_e_adid=&ds_e_matchtype=&ds_e_device=c&ds_e_network=x&ds_e_product_group_id=&ds_e_product_id=en3256808109455456&ds_e_product_merchant_id=5446116119&ds_e_product_country=US&ds_e_product_language=en&ds_e_product_channel=online&ds_e_product_store_id=&ds_url_v=2&albcp=20542171667&albag=&isSmbAutoCall=false&needSmbHouyi=false&gad_source=1&gad_campaignid=18545443176&gbraid=0AAAAAD6I-hFqyMngN-HgL9GtY3F8WiNtV&gclid=CjwKCAjwpK3SBhASEiwAtV1SPHCXWt39-iCecfV2K0ml8IJ9ynNHOuoJVXt9ARZU8BudB5oY3XCx1xoCa5AQAvD_BwE&gatewayAdapt=glo2usa"> Link </a> |
| SG90 Micro Servo | Pen-lift mechanism (raises and lowers the pen) | $2 | <a href="https://www.amazon.com/s?k=SG90+micro+servo"> Link </a> |
| 7806 6V Voltage Regulator | Regulated 6V rail for the motors and servo | $8 | <a href="https://www.amazon.com/Parts-Express-7806-Voltage-Regulator/dp/B0002ZPXJG"> Link </a> |
| 9V Battery | Powers the Arduino and the 6V regulator | $2 | <a href="https://www.amazon.com/s?k=9V+battery"> Link </a> |
| 1N4007 Diode (x2)| Reverse-polarity protection on the power input | $1 | <a href="https://www.amazon.com/s?k=1N4007+diode"> Link </a> |
| Toggle Switch | Main on/off power switch | $3 | <a href="https://www.amazon.com/s?k=SPDT+toggle+switch"> Link </a> |
| Screw Terminal Block | Connection point for the 9V power input wires | $1 | <a href="https://www.amazon.com/s?k=2+pin+screw+terminal+block+5mm"> Link </a> |
| Jumper / Hookup Wires | Wiring between all components | $7 | <a href="https://www.amazon.com/s?k=dupont+jumper+wire+kit"> Link </a> |
| Acrylic Sheet (base) | Flat platform that all components bolt onto | $2 | <a href="https://www.amazon.com/s?k=acrylic+sheet"> Link </a> |
| Wheels (x2) | Driven by the N20 motors to move the plotter | $5 | <a href="https://www.amazon.com/s?k=N20+motor+wheels"> Link </a> |
| Misc. Hardware (screws, bolts, nuts) | Mounts servo bracket, motors, and other parts | $5 | <a href="https://www.amazon.com/s?k=M2+M3+screw+standoff+assortment+kit"> Link </a> |
| 3D Printed Parts (pen-lift assembly, battery holder, 2 glides) | Printed from the included STL files; cost is filament only | $2 | <a href="https://www.instructables.com/Gyro-Controlled-Robot-Plotter/"> STL files </a> |
| Pencil / Fibre-tip Pen | The drawing instrument held by the pen-lift tube | $1 | <a href="https://www.amazon.com/s?k=pencil"> Link </a> |

Estimated total: ~$93 at the prices above. The original project lists an estimated cost of under $100 excluding shipping, so the total will depend on which clone/branded parts you buy.

# Starter Project

<iframe width="560" height="315" src="https://www.youtube.com/embed/lCnJr1lV2uc?si=LOnjVyLKFEXgHM3o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My Starter Project was the LED Slider that was pretty much just soldering practice. The end goal was intended to be three different sliders that increase/decrease resistance for red, green, and blue parts of an LED, changing the color.

However, when I soldered everything on, it wouldn't work. I de-soldered and re-soldered pretty much every connection but it would never work. I even tried flipping the orientation of the light bulb, yet it still wouldn't turn on. In the end, I had to unfortunately give up to begin working on my intensive project, the Drawing Robot. However, my soldering skills greatly improved throughout the process because although there were initially less than 30 connections, I ended up working on around 100 different solders. I also used these skills in the main project, so it was a very good introduction, even if I didn't get the end product.

# Other Resources & Examples
Obviously, this is not the only drawing robot that exists. I took inspiration for this project from lingib's gyro-controlled drawing robot. This is what I used for the circuit diagrams, 3d printed parts, and many of the materials, although I did make a good amount of changes to key materials/pieces and the circuits as well:
- [lingib's Gyro Controlled Robot Plotter](https://www.instructables.com/Gyro-Controlled-Robot-Plotter/#discuss)

Other examples of drawing robots can be found below:
- [Hackaday Drawing Robot](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Ken Olsen's Arduino Robot](https://www.instructables.com/Arduino-Drawing-Robot/)
- [Antonio Mancuso's 3D Printed Drawing Robot](https://www.electromaker.io/blog/article/create-a-3d-printed-drawing-robot-with-arduino-54?srsltid=AfmBOoqwb62AfsNsCO_mHoxaW_undO1t0-Qz6ZHX5Y_PsWbkRKjaG6-v)



<!--- Drives the image swapper. Runs for every .swap block on the page, so you
      can drop in more comparisons later without touching this. Wraps around at
      both ends, so the arrows never dead-end. -->

<script>
document.querySelectorAll('.swap').forEach(function (box) {
  var imgs = box.querySelectorAll('.swap-img');
  var label = box.querySelector('.swap-label');
  var labels = window.swapLabels || [];

  function show(next) {
    var i = (next + imgs.length) % imgs.length;   //wrap around both directions
    box.dataset.i = i;
    imgs.forEach(function (img, n) {
      img.classList.toggle('is-on', n === i);
    });
    if (label && labels[i]) {
      label.textContent = labels[i];
    }
  }

  box.querySelector('.swap-prev').addEventListener('click', function () {
    show(Number(box.dataset.i) - 1);
  });
  box.querySelector('.swap-next').addEventListener('click', function () {
    show(Number(box.dataset.i) + 1);
  });
});
</script>
