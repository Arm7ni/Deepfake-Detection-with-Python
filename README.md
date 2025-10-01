<p align="center">
  <h1 align="center">Deepfake Detection with Python</h1>
  <p align="center">
    For this project, Developed a Deepfake detection pipeline in Python that extracts frames from real and fake videos using OpenCV. Implemented image comparison techniques with Mean Squared Error (MSE) and Structural Similarity Index (SSIM) to identify visual inconsistencies between frames. Visualized results with Matplotlib, demonstrating the ability to detect manipulated media through computer vision and machine learning techniques.<br />
  </p>
</p>

## Features


- **TensorFlow**
- **Python**
- **NumPy**
- **OpenCV**
- **Matplotlib**
- **MTCNN**
- **Scikit-image**


## Step 1.
To begin this project, I set up a clean project structure with code/, data/, and out/frames folders to separate scripts, input videos, and generated frames. I then created a virtual environment to isolate dependencies and installed the required Python libraries, including OpenCV, NumPy, Matplotlib, and scikit-image. I also installed TensorFlow and MTCNN to support face-only deepfake detection.


## Step 2.
I then used a Python script that uses OpenCV to read both the real and manipulated videos. The script automatically extracts frames at a set interval, converts them to grayscale, and resizes them to a standard size to ensure frame-by-frame alignment. This allowed me to normalize both videos and prepare them for fair comparison.

<img width="1195" height="794" alt="Screenshot 2025-09-16 at 11 20 41 PM" src="https://github.com/user-attachments/assets/a3fe0303-2966-4e77-b613-7d3da1964571" />

## Step 3. 
After extracting the frames, the script compared each frame pair using MSE and SSIM. These calculations used NumPy for the pixel-level math and scikit-image for SSIM scoring, giving a clear numerical picture of how similar or different the two videos were frame by frame.
<img width="1668" height="319" alt="Screenshot 2025-09-16 232902" src="https://github.com/user-attachments/assets/e3324653-c482-4208-ac71-8abd5c06c5da" />


## Step 4.
Next I enabled face-only detection using MTCNN with a TensorFlow backend. This step focused the comparison on the face regions, which are the areas most likely to be manipulated, making the results more accurate for detecting deepfake content.


# Step 5.
The script then automatically sorted the results and used Matplotlib to display the most different frames side by side. This visual output made it easy to review where the differences occurred and to see the manipulated parts of the video.
<img width="845" height="488" alt="deepfake2" src="https://github.com/user-attachments/assets/e08fa890-0bec-445d-9979-fe1fa336b9cb" />

<img width="834" height="160" alt="deepfake3" src="https://github.com/user-attachments/assets/fa6c3fe9-f68e-441f-880e-9bdedf82a343" />


# Step 6.
After it successfully ran, I tested the project with multiple video pairs. The output highlighted the frames with the biggest differences and clearly indicated which video was most likely fake, making the solution practical for quickly identifying and reviewing deepfakes.
