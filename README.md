# Voice Analysis and Authentication Project

This repository contains a project for analyzing voice recordings to authenticate students based on a spoken password. The project involves two main tasks:
1. **Speaker Identification**: Identifying the student speaking the password.
2. **Password Identification**: Recognizing the specific password spoken by the student.

This project demonstrates principles from Digital Signal Processing (DSP) and showcases Python-based algorithms for voice analysis, developed in Jupyter Notebooks. The core goals include spectral representation, digital filtering, and keyword/speaker identification.

## Project Objectives

- **Speaker Identification**: Recognize the student speaking the password based on unique voice characteristics.
- **Password Recognition**: Identify the specific password spoken, even if it includes previously unheard words constructed from known phonetic units.
  
The project complies with course requirements for DSP, showcasing:
1. **Spectral Representation of Digital Signals**: Visualizing voice signals in the spectral domain.
2. **Digital Filters**: Applying digital filters to enhance signal quality.
3. **Voice Signal Analysis**: Techniques for both speaker and keyword identification.

## Project Structure

### 1. `Evaluation_Script.ipynb`

- **Purpose**: Evaluates a dataset of recorded passwords, identifying speakers based on their voice characteristics.
- **Details**:
  - Implements spectral analysis techniques to distinguish between speakers.
  - Uses offline analysis, as required, to process pre-recorded datasets.
  - Outputs graphical representations of the signal transformations at each stage.
- **Note**: Run `words_and_speaker_identification.ipynb` first to generate or preprocess the dataset if needed.

### 2. `words_and_speaker_identification.ipynb`

- **Purpose**: Identifies spoken words and speakers through phonetic analysis, focusing on passwords spoken by students.
- **Details**:
  - Processes audio signals to recognize phonetic components.
  - Capable of identifying unknown words constructed from familiar phonetic units.
  - Uses digital filters and other signal processing methods to prepare the data for evaluation.

## Edge Deployment Model

In addition to offline processing, this project includes a model optimized for edge deployment, allowing real-time speaker and password identification directly on edge devices. This edge model supports privacy-centric, on-device processing for efficient authentication in classroom settings.

### Edge Model Features

- **Low Latency**: Designed for quick inference, enabling real-time identification with minimal delay.
- **Privacy by Design**: Processes audio data locally, reducing risks associated with transmitting sensitive information.
- **Scalability**: Capable of running on various edge hardware, providing flexibility in deployment options.

### Usage

The edge model can be integrated with IoT-enabled classrooms for real-time student authentication based on voice recognition. The setup requirements and deployment instructions are available in the `Edge_Model` folder (if applicable).

## Usage Instructions

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>

2. **Install Dependencies**:
Ensure you have Jupyter Notebook and Python 3.x, along with the necessary audio processing libraries (e.g., `librosa`, `numpy`, `scipy`, `matplotlib`).

3. **Run the Notebooks**:
	1. First, open and execute `words_and_speaker_identification.ipynb` to create or process the dataset.
	2. Next, use `Evaluation_Script.ipynb` to evaluate the dataset and identify both the speaker and the password spoken.

## Dataset

Each group should create a custom dataset of voice samples for testing. The dataset should contain:

- Multiple samples of students saying a predefined set of phonetic units.
- Passwords composed of these phonetic units for accurate evaluation.

## Implementation Requirements

- **Offline Mode**: The developed algorithm processes audio in offline mode for this evaluation, although it is designed to run in real-time for data acquisition.
- **Generalization**: The algorithm can recognize new words formed from known phonetic sounds, enabling flexibility in password composition.
- **Documentation**: Each step of the algorithm is documented within the notebooks, with graphical representations of audio transformations.

## Output

Each notebook provides:

- **Code and Explanations**: Documented Python code and explanations for key decisions, linked to DSP concepts.
- **Graphical Results**: Visualizations showing transformations at each processing stage, enhancing interpretability.

