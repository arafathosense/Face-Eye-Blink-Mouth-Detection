# Face-Eye-Blink-Mouth-Detection

## Project Overview

This project uses **OpenCV** and **MediaPipe** to perform real-time detection and counting of eye blinks and mouth openings for multiple faces in a webcam feed. It leverages face mesh landmarks for accurate blink and mouth state detection. The solution supports concurrent tracking of several faces, live FPS monitoring, and a user-friendly overlay with statistics for each detected face.


## Output

<img width="1365" height="725" alt="image" src="https://github.com/user-attachments/assets/16b99486-edc3-4a79-aa1e-35852687d331" />
<img width="1365" height="726" alt="image" src="https://github.com/user-attachments/assets/d026cf40-f547-4e95-a286-dcce0df96fac" />
<img width="1365" height="728" alt="image" src="https://github.com/user-attachments/assets/6e97afbd-1455-4d4d-aa52-2ca148bc1807" />
<img width="1365" height="727" alt="image" src="https://github.com/user-attachments/assets/370332e1-a3c7-42d5-8c84-2935f6d82bd5" />


## Key Features

- **Multi-face tracking** with live bounding boxes
- **Eye Blink Detection:** Uses Eye Aspect Ratio (EAR) for each eye
- **Mouth Open Detection:** Detects mouth state using normalized lip distances
- **Counters** for blinks and mouth opens, tracked per face
- **Real-time FPS display**
- Colored overlays for eyes, lips, bounding boxes, and statistics for quick visualization

## Dependencies

Make sure these Python libraries are installed before running the notebook:
```bash
pip install opencv-python mediapipe numpy scipy
```

## How It Works

1. The webcam feed is processed using OpenCV; MediaPipe FaceMesh generates face landmarks.
2. EAR (eye aspect ratio) and MAR (mouth aspect ratio) are calculated for each face.
3. Blinks are detected using threshold logic on EAR, and mouth opens using MAR.
4. Results, including face statistics, are displayed with colored overlays live.
5. FPS is shown in the top left corner for performance monitoring.


## Usage Instructions

1. Clone the repository or download the notebook to your environment.
2. Ensure a webcam is connected and dependencies are installed.
3. Run all cells in the Jupyter notebook.
4. Press `q` to close the live window and terminate the program.

## Main Code Highlights

- **EAR/MAR thresholds:** Tunable via configuration (`EARTHRESHOLD`, `MARTHRESHOLD`)
- **Face mesh landmark indices:** Used for eye and mouth calculations
- **Helper functions:** Modular code for EAR/MAR, pixel conversion, bounding box, and drawing

## Notes

- Tested on Python 3.x
- Requires a working webcam
- For best results, run in environments with adequate lighting

## License

This project is open source and available for educational and personal use.
