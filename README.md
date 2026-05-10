# Sri Lankan Traffic Sign Detection System for Autonomous Vehicle Navigation

This project focuses on detecting Sri Lankan traffic signs using a **YOLOv8-based model** trained with local traffic sign data on top of a base model.

It is intended to help developers and researchers quickly run sign detection for autonomous vehicle navigation experiments.

---

## Project Goals

- Detect Sri Lankan traffic signs in images/video streams.
- Provide a ready-to-run inference setup.
- Support further fine-tuning and research on local traffic environments.

---

## Current Repository Status

At the moment, this repository is being prepared.  
The complete source files, model files, and runnable scripts can be added/updated after upload.

This README is designed as a user guide so the project can be used immediately once those files are available.

---

## Planned / Expected Repository Structure

```text
.
├── models/                  # Trained model weights (e.g., best.pt)
├── src/                     # Python source code for inference/training utilities
├── data/                    # Dataset configs / sample inputs (optional)
├── requirements.txt         # Python dependencies
└── README.md
```

> If your uploaded files use a different structure, update this section to match the final layout.

---

## Requirements

- Python 3.9+ (recommended)
- pip
- (Optional) CUDA-enabled GPU for faster inference

---

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/sihanas-mn/Sri-Lankan-Traffic-Sign-Detection-System-for-Autonomous-Vehicle-Navigation-ideology-.git
   cd Sri-Lankan-Traffic-Sign-Detection-System-for-Autonomous-Vehicle-Navigation-ideology-
   ```

2. **Create and activate a virtual environment**

   ```bash
   python -m venv .venv
   source .venv/bin/activate     # Linux / macOS
   # .venv\Scripts\activate      # Windows (PowerShell)
   ```

3. **Install dependencies** (after `requirements.txt` is uploaded)

   ```bash
   pip install -r requirements.txt
   ```

---

## How to Use

After uploading the project files, run inference using your main script.  
For example (adjust to your actual script names/paths):

```bash
python src/infer.py \
  --weights models/best.pt \
  --source path/to/image_or_video
```

### Typical Inputs

- Single image (`.jpg`, `.png`)
- Video file (`.mp4`, `.avi`)
- Camera/stream source (if supported by your script)

### Typical Outputs

- Bounding boxes around detected traffic signs
- Class labels
- Confidence scores
- Optional saved output images/videos

---

## Training / Fine-Tuning (Optional)

If training scripts are included after upload, document:

- Dataset format and folder structure
- YAML data configuration location
- Training command
- Checkpoint save path
- Evaluation method

Example training command (placeholder):

```bash
python src/train.py --data data/data.yaml --epochs 100 --imgsz 640
```

---

## Troubleshooting

- **`requirements.txt` not found**  
  Ensure all project files are uploaded and located at the repository root.

- **Model file not found (`best.pt`)**  
  Confirm model weights are placed in the expected `models/` folder (or update command path).

- **Low FPS / slow inference**  
  Use GPU acceleration, reduce image size, or process fewer frames.

---

## Contribution

Contributions are welcome. Suggested workflow:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a pull request

---

## License

Please add the project license file (`LICENSE`) and update this section accordingly.

---

## Acknowledgement

- Ultralytics YOLOv8 ecosystem
- Local Sri Lankan traffic sign data collection efforts
