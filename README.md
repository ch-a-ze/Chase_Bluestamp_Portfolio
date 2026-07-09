# Chase_Bluestamp_Portfolio
 
Portfolio site for my BlueStamp Engineering summer 2026 project: a gyro-controlled drawing robot. The site is live at https://ch-a-ze.github.io/Chase_Bluestamp_Portfolio/.
 
The robot uses a gyroscope to steer itself as it moves, so it can trace shapes onto paper. It runs on an Arduino Nano ESP32 with encoder motors, a BNO055 IMU, and a servo pen lift. Milestone write-ups, schematics, and the full bill of materials are on the site.
 
The repo is a GitHub Pages site built with Jekyll. All page content lives in `index.md`, the custom navy and red theme lives in `assets/css/style.scss`, and `_config.yml` holds the Jekyll config. Colors are set by the CSS variables at the top of the stylesheet, so changing `--red` recolors every accent at once.
 
Inspired by [lingib's Gyro Controlled Robot Plotter](https://www.instructables.com/Gyro-Controlled-Robot-Plotter/).
