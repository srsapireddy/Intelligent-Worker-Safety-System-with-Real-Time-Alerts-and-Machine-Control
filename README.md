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

### Project Workflow

The workflow for the **Intelligent Worker Safety System with Real-Time Alerts and Machine Control** project is designed to enhance worker safety through real-time monitoring and automated machine control. The key stages are:

1. **Data Collection** → Collection of initial data from IP cameras and sensors in the production line.
2. **Data Augmentation** → Application of augmentation techniques to improve model robustness.
3. **Annotation** → Labeling of data to indicate worker hands, safety boundaries, and machinery.
4. **Model Training** → Training SSD MobileNetV2 on annotated data for reliable detection.
5. **Model Validation** → Validation of the model to ensure high accuracy in detecting safety boundary breaches.
6. **Real-Time Monitoring** → Deployment of the trained model for active monitoring of the production line.
7. **Safety Action (Alert / Machine Control)**:
    - **Alarm Trigger** (Safety Line Breach): Activates an alarm if a worker crosses the safety line.
    - **Machine Shutoff** (Boundary Line Breach): Automatically shuts down the machinery if a worker crosses the boundary line.

![hack_2](https://github.com/user-attachments/assets/7d3ad2e4-becc-4b2e-9f0d-ba6dbf99404f)


---

### Workflow Diagram

![Workflow Diagram](path/to/your/workflow_image.png)

This diagram illustrates the flow from data collection to real-time safety actions, providing a comprehensive safety solution for the production environment.


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


