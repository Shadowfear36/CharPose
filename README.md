
# 3D Character Pose Transposer

## Overview

This project is a full-stack web application that takes a video input, performs pose detection using AI, and transposes a pre-rigged 3D character model onto the detected pose in the video. The application uses a **Next.js** frontend and a **Python (FastAPI)** backend.

## Features

- **Pose Detection**: Uses AI models to detect and track body keypoints in the video.
- **3D Model Integration**: Renders pre-rigged 3D models on the frontend, synchronized with the detected pose data.
- **Video Processing**: Transposes the animated 3D model onto the original video frames, creating a seamless overlay.

## Tech Stack

### Frontend
- **Framework**: [Next.js](https://nextjs.org/)
- **3D Rendering**: [Three.js](https://threejs.org/) for loading and animating 3D models.
- **UI Components**: React-based components for user interaction and model selection.

### Backend
- **Framework**: [FastAPI](https://fastapi.tiangolo.com/) for handling API requests.
- **Pose Detection**: [YOLOv8](https://github.com/ultralytics/yolov5) or [Mediapipe](https://google.github.io/mediapipe/) for extracting pose keypoints.
- **Video Processing**: [OpenCV](https://opencv.org/) for handling video frames, and optionally [FFmpeg](https://ffmpeg.org/) for post-processing.

## Project Structure

```
.
├── backend
│   ├── app
│   │   ├── main.py        # FastAPI application and routes
│   │   ├── pose.py        # Pose detection logic
│   │   ├── models         # Directory for machine learning models
│   │   └── utils.py       # Utility functions for processing
│   ├── requirements.txt   # Python dependencies
│   └── Dockerfile         # Dockerfile for containerizing the backend
│
├── frontend
│   ├── pages              # Next.js pages
│   ├── components         # React components
│   ├── public             # Static assets
│   ├── styles             # CSS/SCSS files
│   ├── package.json       # Node.js dependencies
│   └── next.config.js     # Next.js configuration
│
└── README.md              # Project documentation
```

## Getting Started

### Prerequisites

- **Node.js**: Ensure that you have Node.js installed (v14.x or higher).
- **Python 3.8+**: Required for running the backend.
- **FFmpeg**: Optional, but recommended for video processing.

### Backend Setup

1. **Navigate to the backend directory**:
   ```bash
   cd backend
   ```

2. **Create a virtual environment and activate it**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the Python dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the FastAPI server**:
   ```bash
   ```

### Frontend Setup

1. **Navigate to the frontend directory**:
   ```bash
   cd frontend
   ```

2. **Install Node.js dependencies**:
   ```bash
   npm install
   ```

3. **Run the Next.js development server**:
   ```bash
   npm run dev
   ```

4. **Open your browser**: Go to `http://localhost:3000` to view the application.

## Usage

1. **Upload Video**: Start by uploading a video on the frontend.
2. **Select 3D Model**: Choose a pre-rigged 3D model from the available options.
3. **Process**: The backend processes the video and applies the 3D model using the detected pose.
4. **Download or View**: View the transposed video in the browser or download it.

## Future Enhancements

- **Real-time Processing**: Implement real-time pose detection and 3D model transposing.
- **Additional Models**: Add more 3D models for users to choose from.
- **Custom Model Upload**: Allow users to upload their own rigged 3D models.

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request for any feature additions or bug fixes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
