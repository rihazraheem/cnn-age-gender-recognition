# CNN Age and Gender Recognition

👤 Age & Gender Prediction using Multi-Task Learning (UTKFace)

This project implements an age and gender prediction system from facial images using multi-task learning.
Two different approaches are explored:

Custom CNN trained from scratch (baseline)

MobileNetV2 with transfer learning (improved model)

The goal is to compare how feature learning from scratch vs pretrained representations affects performance on age regression and gender classification.

📌 Problem Statement

Given a facial image, predict:

Gender (binary classification: Male / Female)

Age (regression)

Both tasks are learned simultaneously using a shared CNN backbone and task-specific output heads.

📂 Dataset

UTKFace Dataset

~15,000 facial images

Labels extracted from filenames:
age_gender_race_timestamp.jpg

Labels used:

age: integer (0–100+)

gender: 0 = Male, 1 = Female

🧠 Approach Overview
Multi-Task Learning

A single model learns shared facial features, then branches into:

Gender head → Binary classification

Age head → Regression

This improves generalization and reduces overfitting compared to training two separate models.

🏗️ Model Architectures
🔹 Approach 1: Custom CNN (Baseline)

Trained from scratch

Input size: 64×64

Lightweight CNN with ~178K parameters

No pretrained weights

Purpose:

Understand CNN fundamentals

Learn multi-task learning mechanics

Establish a baseline

🔹 Approach 2: MobileNetV2 (Transfer Learning)

Pretrained on ImageNet

Input size: 224×224

Frozen backbone + custom heads

Fine-grained facial representations

Purpose:

Improve performance

Demonstrate transfer learning benefits

Industry-ready architecture

📊 Results (Test Set)
Model	Gender Accuracy	Age MAE
Custom CNN (64×64)	~69%	~5.1 years
MobileNetV2 (224×224)	~82%	~4.7 years

📌 Key Observation
Transfer learning significantly improves both gender classification accuracy and age estimation error.
