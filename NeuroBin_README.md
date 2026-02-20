# NeuroBin

## Open-Source AI-Powered Waste Intelligence System for Sustainable Cities

NeuroBin is an AI-driven smart waste classification and embedded
automation system designed to enable intelligent waste segregation at
the point of disposal. By integrating deep learning with edge-based
embedded hardware, NeuroBin transforms conventional bins into real-time
waste intelligence units.

The system classifies waste as **Biodegradable** or
**Non-Biodegradable** using computer vision and triggers automated bin
actuation, reducing contamination and improving recycling efficiency.

NeuroBin is developed as both: - An academic research and engineering
project - An open-source foundation for scalable climate-tech deployment

------------------------------------------------------------------------

## Problem Statement

Globally, over 2 billion tonnes of municipal solid waste are generated
annually, yet inefficient source-level segregation remains one of the
largest barriers to circular economy implementation.

Existing systems rely on: - Manual sorting (labor-intensive,
inconsistent) - Public behavior compliance (low reliability) - Basic
sensor-based smart bins (limited intelligence)

Contaminated waste streams significantly reduce recycling rates and
increase landfill burden.

NeuroBin addresses this challenge using AI-powered visual classification
integrated with embedded automation.

------------------------------------------------------------------------

## Solution Overview

NeuroBin combines:

-   Deep Learning-based waste classification
-   Edge deployment using Raspberry Pi / embedded systems
-   Servo-controlled bin actuation
-   Real-time inference via camera feed
-   Open-source reproducible architecture

### Core Workflow

Camera Input → AI Model Inference → Waste Classification → Physical Bin
Actuation → Optional Data Logging

The system operates entirely at the edge, making it suitable for
deployment in:

-   Homes
-   Schools
-   Institutions
-   Smart city infrastructure
-   Research environments

------------------------------------------------------------------------

## AI Model & Training

NeuroBin uses a lightweight Convolutional Neural Network optimized for
edge deployment.

### Training Data

The model was trained using publicly available datasets totaling over
250,000 labeled waste images:

-   rayhanzamzamy/non-and-biodegradable-waste-dataset
-   sujaykapadnis/cnn-waste-classification-image-dataset
-   techsash/waste-classification-data

Datasets were used for: - Pre-training - Fine-tuning - Independent
evaluation

### Architecture

-   Three convolutional blocks with max pooling
-   Dropout regularization
-   Dense fully connected layer
-   Softmax output for binary classification

The final trained model is exported in:

-   `.keras` format
-   `.tflite` format (for embedded deployment)

------------------------------------------------------------------------

## Performance Metrics

-   Validation Accuracy: \~94%
-   Loss Function: Sparse Categorical Crossentropy
-   Optimizer: Adam
-   Evaluation performed on independent unseen dataset
-   Confusion matrix generation supported

The model demonstrates strong generalization across varied waste types.

------------------------------------------------------------------------

## Embedded System Integration

NeuroBin integrates AI inference with physical bin control:

-   Raspberry Pi / Jetson Nano / ESP32-CAM compatible
-   Servo motor-based lid actuation
-   Real-time camera feed processing
-   GPIO-based control system

This integration demonstrates practical deployment feasibility beyond
simulation environments.

------------------------------------------------------------------------

## Real-World Demonstration

Example classifications:

-   Apple → Biodegradable → Green bin opens
-   Cardboard → Biodegradable → Green bin opens
-   Tetra Pack → Non-Biodegradable → Red bin opens

Demonstration materials available in:

-   assets/Demo_video.mp4
-   assets/neurobin.jpg

------------------------------------------------------------------------

## Open-Source Philosophy

NeuroBin is released under the MIT License to encourage:

-   Academic research
-   Community-driven dataset expansion
-   Reproducible AI experimentation
-   Low-cost smart infrastructure development

The modular design enables adaptation to regional waste patterns.

------------------------------------------------------------------------

## Repository Structure

-   model_pretrain.py -- Initial large-scale training
-   model_training.py -- Fine-tuning pipeline
-   model_evaluation.py -- Evaluation and metrics
-   model_inference_demo.py -- Real-time inference demo
-   fine_tuned_waste_classifier_v2.keras -- Final trained model
-   requirements.txt -- Dependencies
-   assets/ -- Demonstration images and videos

------------------------------------------------------------------------

## How to Run

Clone the repository:

    git clone https://github.com/UtkarshGupta-22/NeuroBin-Smart-Waste-Segregator.git
    cd NeuroBin-Smart-Waste-Segregator

Install dependencies:

    pip install -r requirements.txt

Train or evaluate:

    python model_pretrain.py
    python model_training.py
    python model_evaluation.py

For quick testing:

Open model_inference_demo.py in Google Colab and upload an image.

------------------------------------------------------------------------

## Deployment

The exported `.tflite` model can be embedded into:

-   Raspberry Pi systems
-   Jetson Nano
-   Edge AI modules

Integrated with OpenCV and GPIO for physical bin actuation.

------------------------------------------------------------------------

## Global Impact & SDG Alignment

NeuroBin contributes to:

-   SDG 11 -- Sustainable Cities and Communities
-   SDG 12 -- Responsible Consumption and Production
-   SDG 13 -- Climate Action

By improving source-level waste segregation, the system reduces landfill
contamination and enhances recycling efficiency.

------------------------------------------------------------------------

## Future Roadmap

-   Multi-class waste classification (plastic, metal, paper, organic,
    e-waste)
-   Dataset expansion with geographically diverse samples
-   Edge optimization for ultra-low-power devices
-   Waste analytics dashboard for institutional monitoring
-   Federated learning for distributed model improvement

The long-term vision is to evolve NeuroBin into a distributed waste
intelligence infrastructure supporting circular economy transformation.

------------------------------------------------------------------------

## Author

Utkarsh Gupta\
B.Tech Computer Science (Data Science Specialization)\
Focus Areas: Machine Learning, Computer Vision, Embedded AI Systems

NeuroBin is developed as both an academic innovation and a scalable
AI-based environmental solution.

------------------------------------------------------------------------

## License

MIT License\
Free to use, modify, and distribute with attribution.
