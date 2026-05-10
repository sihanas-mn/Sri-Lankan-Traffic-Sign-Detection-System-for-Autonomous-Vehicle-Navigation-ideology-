# Sri Lankan Traffic Sign Detection System for Autonomous Vehicle Navigation

This repository provides pretrained YOLO models for Sri Lankan traffic sign detection and the dependencies needed to run inference.

## Repository Contents

```text
.
├── model_1.pt
├── model_2.pt
├── requirements.txt
└── README.md
```

- `model_1.pt`, `model_2.pt`: pretrained model weights
- `requirements.txt`: Python dependencies for running detection applications

## Requirements

- Python 3.9+
- pip
- Optional: CUDA-capable GPU for faster inference

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/sihanas-mn/Sri-Lankan-Traffic-Sign-Detection-System-for-Autonomous-Vehicle-Navigation-ideology-.git
   cd Sri-Lankan-Traffic-Sign-Detection-System-for-Autonomous-Vehicle-Navigation-ideology-
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   source .venv/bin/activate      # Linux / macOS
   # .venv\Scripts\activate       # Windows (Command Prompt)
   # .venv\Scripts\Activate.ps1   # Windows (PowerShell)
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Quick Start (YOLO CLI Inference)

You can run inference directly with Ultralytics CLI:

```bash
yolo predict model=model_1.pt source=path/to/image_or_video
```

You can switch to `model_2.pt` the same way:

```bash
yolo predict model=model_2.pt source=path/to/image_or_video
```

## Typical Inputs and Outputs

### Inputs
- Single images (`.jpg`, `.png`)
- Video files (`.mp4`, `.avi`)
- Camera stream index (`source=0`)

### Outputs
- Detected traffic sign bounding boxes
- Class labels and confidence scores
- Saved prediction images/videos (Ultralytics default output directory)

## Troubleshooting

- `ModuleNotFoundError` or missing package errors:
  - Re-run `pip install -r requirements.txt`
- Slow inference:
  - Use a CUDA-enabled environment, or reduce image/frame size
- Model not found:
  - Ensure you run commands from the repository root or provide full model path

## Notes

If you add application code (for example, Streamlit UI or custom Python scripts), update this README with exact run commands for those files.
