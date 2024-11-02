# Intelligent Worker Safety System with Real-Time Alerts and Machine Control

### Overview
The **Intelligent Worker Safety System with Real-Time Alerts and Machine Control** aims to enhance worker safety on production lines by implementing an automated alert and machine control system. Prioritizing worker safety not only promotes a secure work environment but also builds confidence among employees, ultimately contributing to company growth. This system leverages IP cameras, microcontrollers, and relays to monitor worker proximity to hazardous areas, automatically triggering alerts or shutting down machinery when necessary.

### System Features
1. **Safety Line Alert**: If a worker’s hand crosses the designated safety line, a continuous alarm is triggered. This serves as an immediate warning for the worker to maintain a safe distance from the machinery, reducing the risk of accidents.

2. **Boundary Line Control**: If a worker crosses the boundary line, the system automatically shuts down the machinery. This action is executed through commands from the microcontroller, providing a secondary layer of protection to prevent any hazardous interactions.

### Model Selection and Optimization
For detecting worker movements, object detection models were evaluated:
- **Faster RCNN** was tested but provided unrealistic Mean Average Precision (MAP) values for this specific application.
- **SSD MobileNetV2** was chosen for its performance and computational efficiency, achieving a MAP score between 60 and 70, making it suitable for real-time safety monitoring.

### Technical Components
- **Real-Time Processing**: The system uses SSD MobileNetV2 to analyze video feeds and detect worker movements in real time.
- **Modular Design**: Key components include:
  - **IP Camera** for video capture
  - **Microcontroller** to process alerts based on boundary detections
  - **Relays** for machine power control
- **Automated Machine Control**: When a worker crosses the boundary line, the microcontroller immediately shuts down the machine, preventing accidents.
- **Continuous Alerts**: An audio alarm is activated upon crossing the safety line, ensuring workers are constantly aware of safe working distances.

### Getting Started
To deploy the system:
1. Set up the IP camera for live video feed.
2. Configure the microcontroller to handle alarm and machine control commands.
3. Load and deploy the SSD MobileNetV2 model for real-time monitoring.
4. Connect relays to the microcontroller for automated control of machinery.

# Project Workflow

This project follows a structured workflow for training and deploying a machine learning model. Below are the key steps:

1. **Data Collection**: 
   - The process begins with gathering raw data relevant to the task. This data serves as the foundation for model training.

2. **Data Augmentation**:
   - To increase the robustness and generalization of the model, various data augmentation techniques are applied. This step helps in expanding the dataset and improving model performance.

3. **Annotation**:
   - The augmented data is then annotated to provide labels, bounding boxes, or other necessary information required for supervised learning.

4. **Model Training**:
   - Using the annotated data, the model is trained to learn the features and patterns required to perform the desired task accurately.

5. **Model Validation**:
   - The trained model undergoes validation to evaluate its performance on unseen data. This step helps in assessing the model's accuracy and generalization capability.

6. **Model Deployment With Different Devices**:
   - After validation, the model is deployed on various devices for practical use. This deployment step ensures that the model functions effectively in real-world scenarios.

### Workflow Diagram

![Workflow Diagram](path/to/your/image.png)

This diagram illustrates the flow of data through each stage in the process, showing how each component contributes to developing a robust and deployable machine learning model.


### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/srsapireddy/srsapireddy-Intelligent-Worker-Safety-System-with-Real-Time-Alerts-and-Machine-Control.git
   cd srsapireddy-Intelligent-Worker-Safety-System-with-Real-Time-Alerts-and-Machine-Control

2. **Install necessary dependencies:**
   ```bash
   pip install -r requirements.txt

3. Create a separate Conda environment:
   ```bash
   conda create -n computer_vision python=3.6 -y

4. Activate the environment:
   ```bash
   conda activate computer_vision

5. Install the object detection library:
   ```bash
   pip install object-detection

6. Run the Program:
   ```bash
   python hand_detection.py

### Technology Stack
- TensorFlow 1.x
- Object Detection
- OpenCV
- Faster RCNN
- SSD MobileNetV2

### Future Enhancements
#### Potential improvements include:

- Integrating advanced machine learning models for enhanced accuracy
- Exploring different sensor types for robust safety monitoring
- Implementing data analytics to track and analyze safety incidents

### Contributing
Contributions are welcome! Please submit a pull request or open an issue for any suggestions or bug reports.


