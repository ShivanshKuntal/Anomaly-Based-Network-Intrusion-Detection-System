# Anomaly Based Network Intrusion Detection System

Anomaly-Based Network Intrusion Detection System (NIDS)

Anomaly-Based NIDS is a machine learning powered system for detecting suspicious network activity by learning what “normal” traffic looks like and flagging deviations from it. Instead of relying only on static signatures, this project focuses on behavioral patterns, which helps identify novel and zero-day attacks.

🔍 Overview

Traditional signature-based IDS solutions struggle with:

Previously unseen (zero-day) attacks

Polymorphic / obfuscated payloads

Constantly changing attack patterns

This project implements an anomaly-based approach. The system learns statistical and behavioral profiles of benign traffic from historical data, then identifies potential intrusions as outliers or anomalies in real-time or batch traffic logs.

✨ Key Features

Anomaly-based detection using ML models

Feature extraction from raw network flows (e.g., duration, bytes, packets, flags, protocol)

Support for multiple algorithms (e.g., Isolation Forest, One-Class SVM, Autoencoders depending on configuration)

Configurable thresholds to control sensitivity vs false positives

Modular pipeline for:

Data loading & preprocessing

Feature engineering & scaling

Model training & evaluation

Inference on live / offline traffic

Evaluation metrics (precision, recall, F1-score, ROC-AUC, confusion matrix)

Command-line / scriptable interface for automation and integration

🧱 Architecture

High-level workflow:

Data Ingestion

Imports traffic data from PCAP-derived CSVs, NetFlow/IPFIX exports, or benchmark datasets (e.g., NSL-KDD, CICIDS* depending on configuration).

Preprocessing & Feature Engineering

Cleans missing / invalid values

Encodes categorical features (protocol, flags, service, etc.)

Normalizes / standardizes numerical features

Optionally performs dimensionality reduction (e.g., PCA)

Model Training (Anomaly Detection)

Trains on benign or mostly benign traffic to learn “normal” behavior

Uses one or more unsupervised / semi-supervised algorithms

Persists trained models for later reuse

Detection / Inference

Scores new network flows and assigns an anomaly score

Labels flows as:

Normal

Suspicious / anomalous (above configurable threshold)

Reporting & Logging

Generates detection logs with timestamps, source/destination IP, ports, anomaly scores, and predicted label

Can be integrated with SIEM / log management tools
