# Hand-Gesture-Math-Solver

## Overview
- This project demonstrates a real-time hand gesture recognition system using Python, OpenCV, and Gemini AI by Google.
- The system allows users to solve math problems by drawing them in the air.
- The repository contains all the code and resources needed to implement this project.

## Features

- Real-time hand detection and tracking using OpenCV and cvzone.
- Recognition of specific hand gestures to perform actions like drawing, clearing canvas, and requesting math problem solutions.
- Integration with Gemini AI for solving math problems based on gestures.

## Technologies/Tools

* Python 3.10.12
* cvzone `pip install cvzone`
* OpenCV `pip install opencv-python`  
* Gemini AI `pip install google-generativeai`
* Python packages
  * numpy `pip install numpy` 
  * pillow `pip install pillow`
 
![Python](https://img.shields.io/badge/python-3670A0?logo=python&logoColor=FFFF00)
![cvzone](https://img.shields.io/badge/cvzone_-orange)
![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?logo=opencv&logoColor=white)
![Gemini AI](https://img.shields.io/badge/Gemini%20AI_-%238E75B2?logo=googlegemini&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?logo=numpy&logoColor=white)
![pillow](https://img.shields.io/badge/pillow_-blue)

* C++ compiler - install [Visual Studio](https://visualstudio.microsoft.com/downloads/)

## Installation
 
  1. **Clone the repository:**
 
     ```bash
     git clone https://github.com/LasithaAmarasinghe/Hand-Gesture-Math-Solver.git
     cd Hand-Gesture-Math-Solver
     ```
 
  2. **Create and activate a virtual environment (optional but recommended):**

     ```bash
     python -m venv venv
     source venv/bin/activate   # On Windows use `venv\Scripts\activate`
     ```
 
  3. **Install the required packages:**
 
     ```bash
     pip install -r requirements.txt
     ```
## Usage

  1. **Get a Gemini API key**

     You can get an API key from [here](https://aistudio.google.com/app/apikey)

  2. **Replace API key in the code with the obtained API key**
     
  3. **Execute the main script**

```bash
python math_solver.py
```
 4. **Interact with the Application**
   
     * **Live Feed**
        * The application will display the live feed from your webcam.
     * **Perform Hand Gestures**
        * Draw: Use one finger to draw on the canvas.
        * Clear: Use one finger to clear the canvas.
        * Solve Math Problem: Use all fingers except the thumb to submit a math problem for solving.
      
## Code Explanation

  1. **getHandInfo(img)**

     * **Purpose:** Detects and tracks the user's hand in each frame of the webcam feed.
     * **Implementation:** Uses the HandTrackingModule to identify and monitor hand movements.

  2. **draw(info, prev_pos, canvas)**

     * **Purpose:** Draws on the canvas based on the detected hand gestures.
     * **Parameters:**
          * `info`: Information about the detected hand gestures.
          * `prev_pos`: Previous position of the drawing.
          * `canvas`: Canvas to draw on.

  3. **sendToAI(model, canvas, fingers)**

     * **Purpose:** Sends the drawn content to Google's Generative AI for math problem solving based on recognized gestures.
     * **Parameters:**
          * `model`: Instance of the Generative AI model.
          * `canvas`: Canvas containing the drawn content.
          * `fingers`: Array indicating the state of fingers (e.g., for gesture recognition).



## Hand Detection Concept

<img src="https://github.com/LasithaAmarasinghe/Hand-Gesture-Math-Solver/assets/106037441/196a14ec-6067-494c-8e06-69873fa418f3" >

___

**Left-Right Hand Detection**

<img src="https://github.com/LasithaAmarasinghe/Hand-Gesture-Math-Solver/assets/106037441/c0eaf562-bb89-4b47-b9f8-4bb96ec3e442" width="400" height="240">
<img src="https://github.com/LasithaAmarasinghe/Hand-Gesture-Math-Solver/assets/106037441/a7c1a542-8b85-42a2-87fa-bb20ff280a1e" width="400" height="240">

___

**Hand Gesture Detection**

<img src="https://github.com/LasithaAmarasinghe/Hand-Gesture-Math-Solver/assets/106037441/56434be0-8338-41e2-b060-5b14e69f6325" width="400" height="280">
<img src="https://github.com/LasithaAmarasinghe/Hand-Gesture-Math-Solver/assets/106037441/b66a3d35-f7f7-4b75-b7db-c93ee40d6841" width="400" height="280">

## Results

**Math Expression Detection & Canvas** 

<img src="https://github.com/LasithaAmarasinghe/Hand-Gesture-Math-Solver/assets/106037441/e9558800-a17f-432d-a4f5-d00d0a352cfb" width="400" height="240">
<img src="https://github.com/LasithaAmarasinghe/Hand-Gesture-Math-Solver/assets/106037441/64664179-a2cc-43a2-af2b-409a6beb4325" width="400" height="240">

## License
 
 * This project is licensed under the MIT License. See the [LICENSE](MIT-LICENSE.txt) file for details.

