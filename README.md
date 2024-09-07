# EyeCurser
# Eye-Controlled Mouse

This project allows you to control your mouse cursor using eye tracking. The program uses OpenCV and MediaPipe to detect your facial landmarks and track your eye movements. When you blink, the program clicks the mouse.

## Features

- Tracks eye movement to move the mouse cursor.
- Detects blinking to perform a mouse click.
- Real-time video processing using OpenCV.
- Face landmark detection using MediaPipe.

## Requirements

Before running the project, make sure you have the following dependencies installed:

- Python 3.x
- OpenCV (`opencv-python`)
- MediaPipe
- PyAutoGUI
- (Optional) AutoPy (if you wish to use it instead of PyAutoGUI)

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/eye-controlled-mouse.git
    cd eye-controlled-mouse
    ```

2. Install the required Python packages:

    ```bash
    pip install opencv-python mediapipe pyautogui
    ```

3. (Optional) Install AutoPy if needed:

    ```bash
    pip install autopy
    ```

## Usage

1. Run the script:

    ```bash
    python eye_controlled_mouse.py
    ```

2. The program will open your webcam and start tracking your eye movement. 

3. Move your eyes to control the mouse cursor. Blink to click.

## How It Works

- **Face Mesh**: MediaPipe's Face Mesh model is used to detect and track facial landmarks, specifically focusing on the eye area.
- **Cursor Movement**: The position of specific facial landmarks (points around the eyes) is mapped to the screen coordinates to move the mouse cursor.
- **Click Detection**: The difference in the vertical position of the upper and lower eyelids is monitored to detect a blink. If a blink is detected, a mouse click is triggered.

## Troubleshooting

- **Cursor Lag**: If you experience lag or jittery movement, try adjusting the screen scaling factor or ensure your system is not overloaded.
- **Incorrect Clicks**: If the program clicks when you don't intend it to, you might need to adjust the sensitivity or threshold of the blink detection.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgements

- [MediaPipe](https://google.github.io/mediapipe/) for providing the Face Mesh model.
- [OpenCV](https://opencv.org/) for real-time video processing.
- [PyAutoGUI](https://pyautogui.readthedocs.io/en/latest/) for controlling the mouse.

