
# Facial Aging Using SAM (Style-based Age Manipulation)

The **Facial Aging Using SAM (Style-based Age Manipulation)** project is a deep learning-based facial transformation system designed to predict and visualize how a person’s face changes with age. Built upon the SAM model, which extends **StyleGAN2**, this system generates highly realistic aged or de-aged versions of face images by manipulating latent vectors in the age direction while preserving identity and facial structure.

The project requires input images that are preprocessed—aligned and cropped in the **FFHQ format (1024x1024)**—and makes use of a **pretrained SAM model** for age transformation. Additionally, it relies on a **shape predictor** (typically from dlib) to detect facial landmarks during alignment.

##  Project Structure

```bash
Facial_Aging_Using_SAM/
├── config/                
├── datasets/              
├── models/              
├── notebooks/          
├── results/                 
├── scripts/
└── utils/
├── run_aging.py
└── README file                
````

##  Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/Moulya-Reddy/Facial_Aging_Using_SAM.git
cd Facial_Aging_Using_SAM
```

### 2. Create and Activate a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install - all the modules required. 
```

### 4. Download Required Models

####  Shape Predictor (dlib)

```bash
wget http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2
bzip2 -dk shape_predictor_68_face_landmarks.dat.bz2
```

Place the extracted `shape_predictor_68_face_landmarks.dat` file in a known location or your working directory.

####  Pretrained SAM Model

Download `sam_ffhq_aging.pt` and place it in the `pretrained_models/` directory.

* Example filename: `pretrained_models/sam_ffhq_aging.pt`
* This file can typically be obtained from the internet.

##  How to Use

### Step 1: Prepare Input Images

* Add your aligned and cropped face images (1024x1024, FFHQ-style) to the `datasets/` folder.
* Ensure facial alignment is handled. You may use a dlib-based **shape predictor** for this.

### Step 2: Run the Aging Script

```bash
python run_aging.py
```


##  Pretrained Models

Ensure the pretrained SAM model is placed in the `pretrained_models/` directory. You may need to download it separately.
