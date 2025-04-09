# HWS-Lite: Lightweight He Who Sees

HWS-Lite is a simplified yet powerful security, surveillance, and navigation system designed to provide real-time object detection, action recognition, and path planning. With its modular design and lightweight implementation, HWS-Lite is ideal for applications requiring efficient monitoring and analysis.

---

## What is HWS?

HWS (He Who Sees) is a framework designed for:
- **Security and Surveillance**: Detects objects, tracks their movement, and assesses potential risks in real-time.
- **Action Recognition**: Identifies actions such as walking, running, sitting, standing, or fighting.
- **Navigation Assistance**: Plans and communicates optimal navigation paths while avoiding obstacles.

HWS-Lite leverages cutting-edge technologies, including:
- **YOLOv8 Nano** for lightweight object detection.
- **DeepSORT** for real-time object tracking.
- **PyTorch** for action recognition.
- **A* Pathfinding Algorithm** for navigation planning.
- **Audio Event Detection** for identifying events like gunshots or screams.

It is designed to work with video inputs, analyze scenes, and provide actionable insights in real-time.

---

## How HWS Works

HWS-Lite works by integrating multiple components into a seamless system:

1. **Object Detection**:
   - Uses YOLOv8 Nano to detect objects such as people, cars, bottles, knives, and chairs in the video stream.
   - Assigns unique IDs to tracked objects for persistent monitoring.

2. **Object Tracking**:
   - Tracks moving objects using the DeepSORT tracking algorithm.
   - Identifies and announces newly detected and missing objects.

3. **Action Recognition**:
   - Processes pose sequences of tracked individuals and classifies their actions (e.g., walking, running, sitting, standing, fighting) using a lightweight neural network.

4. **Audio Event Detection**:
   - Analyzes audio input to identify events such as gunshots, screams, or explosions.
   - Simplified threshold-based scoring is used for event detection.

5. **Navigation Assistance**:
   - Generates an occupancy grid from detected obstacles.
   - Uses the A* pathfinding algorithm to plan an optimal path from a starting point to a goal while avoiding obstacles.
   - Provides spoken feedback about the planned path.

6. **Speech Output**:
   - Uses text-to-speech (TTS) to announce detected objects, actions, and navigation updates.

---

## Example Outputs of HWS in Action

Here are some examples of HWS-Lite in action:

1. **Object Detection and Tracking**:
   - "New person detected with ID 1."
   - "Knife detected with ID 5 appears abandoned."
   - "Person ID 3 is gone."

2. **Action Recognition**:
   - "Person ID 2 is walking."
   - "Person ID 4 is fighting."

3. **Navigation Assistance**:
   - "Path planned with 10 steps."

4. **Audio Event Detection**:
   - "Gunshot detected."

5. **Surveillance Insights**:
   - "Chair ID 7 appears abandoned."

---

## How to Use HWS

### Prerequisites

- A Python 3.8+ environment.
- Required Python libraries: `torch`, `numpy`, `pyttsx3`, `pygame`, `opencv-python`, `sounddevice`, `speechrecognition`, `ultralytics`, `deep-sort-realtime`, and `psutil`.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/CalebMathias/HWS.git
   cd HWS
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure your video input (e.g., webcam) is connected.

### Running HWS-Lite

1. Start the program:
   ```bash
   python HWS.py
   ```

2. Press `q` to exit the application.

### Customizing the Video Source
- By default, HWS-Lite uses the primary webcam (`video_source=0`). To use a different video source, modify the `video_source` parameter in the `HWSLite` class initialization.

---

## Features in Detail

1. **Real-Time Object Detection**:
   - Detects and classifies objects with confidence thresholds.

2. **A* Pathfinding Navigation**:
   - Plans a collision-free path based on detected obstacles.

3. **Audio Event Analysis**:
   - Detects audio anomalies like gunshots or screams.

4. **Abandoned Object Detection**:
   - Identifies objects left unattended and alerts the user.

5. **Action Recognition**:
   - Recognizes and announces actions of tracked individuals.

---

## Example Use Cases

1. **Security Systems**:
   - Monitor for suspicious activities or abandoned objects in a public space.

2. **Robotics**:
   - Navigate a robot through an environment with obstacles.

3. **Forensic Analysis**:
   - Detect and track unusual events like fights or screams.

4. **Home Automation**:
   - Alert homeowners about detected objects or actions.

---

## Contributing
Contributions are welcome! Feel free to fork the repository, make improvements, and submit a pull request.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Make sure to explore the capabilities of HWS-Lite and adapt it to your specific needs. Happy coding! 🚀
