# Adaptive Stress Management

### A Human-in-the-Loop Framework using Active Learning and Physiological Computing

AI-driven personalized stress monitoring using physiological signals, uncertainty-aware machine learning, and conversational interaction.

---

## Overview

This project develops a real-time adaptive stress monitoring system that learns individual stress patterns over time.

Unlike static stress classifiers, this system:

* Detects stress from physiological signals
* Measures prediction uncertainty
* Asks the user when unsure
* Continuously personalizes the model

The result is a closed-loop, human-in-the-loop framework for personalized stress management.

---

## Key Features

* Real-time physiological stress detection
* Entropy-based uncertainty quantification
* Active Learning personalization
* LLM-based conversational feedback
* Human-in-the-loop adaptive framework

## System Architecture
<img width="577" height="348" alt="image" src="https://github.com/user-attachments/assets/527b0b60-6f12-40ea-91d5-9f16d8097559" />

---

## [Real-Time Monitoring](https://github.com/prachi0711/Stress-Management-using-Active-Learning/blob/main/real_time_monitoring/README.md)

The system processes physiological signals such as:

* Electrodermal Activity (EDA)
* Inter-Beat Interval (IBI) 

Pipeline:

1. Signal acquisition
2. Preprocessing & feature extraction
3. Sliding window classification
4. Stress prediction output

The system can operate on:

* Public datasets (e.g., WESAD)
* Simulated streams
* Real-time wearable data (e.g., Emotibit)


---

## [Active Learning](https://github.com/prachi0711/Stress-Management-using-Active-Learning/blob/main/active_learning/README.md)

A key contribution of this project is uncertainty-driven personalization.

After each prediction:

* Prediction probabilities are computed
* Entropy is used to measure uncertainty

Decision logic:

* **Low uncertainty** → Deliver stress intervention
* **High uncertainty** → Ask the user for clarification

User feedback is then:

* Added as labeled data
* Used to update the model
* Improving personalization over time

This reduces the need for large labeled datasets and adapts to individual physiological differences.

---

## [Dialogue Manager](https://github.com/prachi0711/Stress-Management-using-Active-Learning/blob/main/dialogue_manager/README.md)

When uncertainty is high, the system does not issue a rigid alert.
Instead, it triggers a natural language interaction powered by a Large Language Model (LLM).

Example interaction:

> “I’m noticing some changes in your signals. Are you feeling stressed right now or just physically active?”

The dialogue manager:

* Generates empathetic queries
* Interprets user responses
* Extracts feedback labels
* Feeds them back into the learning loop

This transforms the system from a passive detector into an interactive stress assistant.

---

For further informantion; please refer the following [report]()



