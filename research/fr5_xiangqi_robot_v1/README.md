# FR5 Xiangqi Robot

An autonomous Chinese Chess (Xiangqi) playing robot system using a camera + YOLO occupancy detection, Pygame UI, AI engines, and a robotic manipulator. The runtime is currently deployed for the Fairino FR5 robot with a JODELL/ERG gripper via `MoveGripper`.

> **Note:** The parameters in `config.py` are sample configurations from a specific setup. IP camera addresses, offsets, Z heights, gripper positions, teaching points, or API tokens must be calibrated for each individual hardware setup.

---

## 1. System Architecture

```text
Camera / Video Source
        ↓
YOLO occupancy model + perspective transform
        ↓
SnapshotDetector: compares T1 baseline with T2 after pressing SPACE
        ↓
GameState + Xiangqi rules + FEN representation
        ↓
AI Engine → Robot Move Execution → Update T1 Baseline
```

### Module Breakdown:

| Module | Role |
|---|---|
| `main.py` | Main loop: UI rendering, inputs, AI turn processing, robot movement execution, baseline updates. |
| `config.py` | Runtime configurations: Camera source, robot TCP/IP, gripper parameters, AI engine, physical coordinate mapping. |
| `src/core/` | Xiangqi game rules, FEN parsing, game state management, and rollback mechanisms. |
| `src/vision/` | Video capture, YOLO inference, perspective transform mapping, and snapshot detection. |
| `src/hardware/` | Robotic manipulator motion commands, gripper adapter, hardware coordination, and Fairino SDK integrations. |
| `src/ai/` | Cloud engine API adapter, Moonfish local engine integration, and AI move controllers. |
| `src/ui/` | Pygame graphical interface, control buttons, keyboard and mouse event handlers. |
| `tests/` | Unit tests and manual calibration tools sorted by module. |

---

## 2. Directory Structure

```text
fr5_xiangqi_robot/
├── main.py
├── config.py
├── README.md
│
├── assets/
│   ├── models/
│   │   └── best.pt                  # Runtime YOLO weights
│   ├── perspective.npy              # Generated after camera calibration
│   ├── videos/                      # Raw video recordings for dataset generation
│   ├── custom_dataset/              # Labeled custom dataset for YOLO training
│   ├── debug_outputs/               # Debug output frames from the vision pipeline
│   └── droidcam_outputs/            # Saved camera capture outputs
│
├── src/
│   ├── ai/
│   ├── api/
│   ├── core/
│   ├── hardware/
│   ├── ui/
│   └── vision/
│
├── tests/
│   ├── 00_camera/
│   ├── 01_yolo_dataset_tools/
│   ├── 02_yolo_pipeline_debug/
│   ├── 03_robot_math/
│   ├── 04_robot_motion_manual/
│   └── 05_gripper_manual/
│
└── moonfish/                         # Local engine repository
```

---

## 3. Environment Setup

### 3.1. Python Environment

Using Conda:
```bash
conda create -n fr5v6 python=3.10 -y
conda activate fr5v6
cd fr5_xiangqi_robot
```

Using venv:
```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
```

### 3.2. Install Dependencies

```bash
pip install numpy opencv-python pygame ultralytics requests pillow
```

If utilizing GPU acceleration for YOLO, install the PyTorch build matching your local CUDA version.

---

## 4. Key Configurations (`config.py`)

### 4.1. Run Mode
- `DRY_RUN = True`: Runs without connecting to physical hardware. Excellent for testing UI, game rules, and AI movements using the mouse.
- `DRY_RUN = False`: Executes real-world deployment (Camera + YOLO + Robotic Manipulator).

### 4.2. Z Height & TCP Orientation
- `SAFE_Z`: Safe height for horizontal moves to avoid colliding with game pieces.
- `PICK_Z`: Target grasping depth (should kneed piece without crashing into the board).
- `PLACE_Z`: Target release height.
- `ROTATION`: Main orientation angle array for the gripper TCP.

### 4.3. AI Engine Selection
- `CLOUD`: Connects to remote API endpoints for the best move calculations.
- `LOCAL`: Launches the offline UCCI/Moonfish Python engine.
- `HYBRID`: Prioritizes Cloud API calls with an automatic offline Local fallback.

---

## 5. Security & Git Guidelines

**Do not commit the following elements if the repository is public:**
- Live active API tokens or credentials in `config.py`
- Heavy video datasets
- Training outputs (e.g. `runs/` directory)
- Compiled python bytecode (`__pycache__`)
- Local engine binary builds
