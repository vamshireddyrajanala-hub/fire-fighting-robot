# Fire Fighting Robot

An autonomous fire detection and suppression robot with live video streaming and remote control.

## Hardware
- Raspberry Pi 3B — main controller (Python, GPIO)
- ESP32-CAM — live video streaming + WebSocket motor control
- Flame sensor — autonomous fire detection
- Gas sensor — smoke/gas detection
- Relay module — drives water pump
- Dual DC motors with PWM speed control
- Water tank + pump

## How It Works
1. Python GPIO loop on RPi polls flame and gas sensors continuously
2. On fire detection → relay triggers water pump + buzzer automatically (<200ms latency)
3. ESP32-CAM streams 640×480 live video over WiFi
4. Operator can remotely drive the robot via browser WebSocket interface

## Files
- `src/fire_fighting_robot.ino` — Flame sensor polling, relay/pump control, alarm logic

## Demo
See portfolio: [vamshireddyrajanala-hub.github.io/portfolio](https://vamshireddyrajanala-hub.github.io/portfolio/)
