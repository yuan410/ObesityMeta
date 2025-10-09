# Overview
This repository contains the datasets, code scripts, and instructions for running the code implemented in the paper: *"Machine Learning-Based Identification of Abnormal Functional Connectivity in Obesity Across Different Metabolic States."*
Please note that this repository provides MOCK datasets and scripts. **For the actual code implementation, refer to the Docker image as outlined in the instructions below.**
- The full mock dataset can be found in `datasets/MOCKED_data`.
- The demo mock dataset is available in `datasets/Demo_MOCKED_data`.
- The code script is in 'CodeScript.ipynb'
Please be aware that using the mock data may lead to results different from those reported in the paper, as the actual study uses real data. The demo dataset is provided solely for the purpose of running the code scripts and should not be used to draw any scientific conclusions, as the results generated are not representative of the actual findings.

# System Requirements

## Hardware Requirements
- To run the demo dataset, a standard computer with sufficient RAM is required for in-memory operations.
- To run the full dataset, a computer with at least 14.8+ GB of *free RAM* is necessary.

## Software Requirements
- **Docker**: Install Docker Desktop from [here](https://www.docker.com/products/docker-desktop) to run the code scripts.

### OS Requirements
- No specific OS requirement, as everything runs via a Docker container. 
- The package has been tested on Ubuntu 23.04 and Windows 10.

#### Python Dependencies
- pandas==1.5.2
- numpy==1.23.3
- scikit-learn==1.4.1.post1
- matplotlib==3.7.3
- seaborn==0.11.2
- nilearn==0.10.2
- scipy==1.10.1
- statistics
- statannotations==0.6.0
- statsmodels==0.14.0
- statannot==0.2.3


# Docker Implementation

1. **Download Docker**: Install Docker Desktop from [here](https://www.docker.com/products/docker-desktop).

2. **Pull Image from Dockerhub**:
   - Open a command line and type the following commands:
     - `docker pull yueyu445/obesity_jupyter_image`
     - `docker run -it -p 8888:8888 yueyu445/obesity_jupyter_image`
   - Copy the URL generated (e.g., `http://(0de284ecf0cd or 127.0.0.1):8888/?token=...`) and paste it into your browser.
   - Navigate to `notebooks/MockedDataResults.ipynb` and click **Run > Run All Cells** to execute the code. By default, this script will run on the **demo dataset**.

3. **To run on the full dataset**:
   - In cells 4, 6, and 8, COMMENT OUT the line referencing `Demo_MOCKED_data` and UNCOMMENT the line for `MOCKED_data`.
   - Example in cell 8:
     - COMMENT OUT: `for directory in [f"/home/otagouni/yuan_obesity/notebooks/datasets/Demo_MOCKED_data/BL/T{time}"]`
     - UNCOMMENT: `for directory in [f"/home/otagouni/yuan_obesity/notebooks/datasets/MOCKED_data/BL/T{time}"]`

Refer to the images below for guidance on adjusting cells:
- Cell 4: ![image](https://github.com/user-attachments/assets/cd7631ff-361d-4f13-a46f-c1a295a2f700)
- Cell 6: ![image](https://github.com/user-attachments/assets/0e57b4d8-3726-4e2f-ae1b-fce4d3cf67db)
- Cell 8: ![image](https://github.com/user-attachments/assets/c2a3cbfe-2c80-42ba-b666-82fb8f145f97)

# License

This project is open-source and is licensed under Apache 2.0.





