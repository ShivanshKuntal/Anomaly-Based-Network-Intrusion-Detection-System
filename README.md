# Anomaly Based Network Intrusion Detection System

Anomaly-Based Network Intrusion Detection System (NIDS)

Anomaly-Based NIDS is a machine learning powered system for detecting suspicious network activity by learning what “normal” traffic looks like and flagging deviations from it. Instead of relying only on static signatures, this project focuses on behavioral patterns, which helps identify novel and zero-day attacks.

🔍 Overview

Traditional signature-based IDS solutions struggle with:

1. Previously unseen (zero-day) attacks

2. Polymorphic / obfuscated payloads

3. Constantly changing attack patterns

This project implements an anomaly-based approach. The system learns statistical and behavioral profiles of benign traffic from historical data, then identifies potential intrusions as outliers or anomalies in real-time or batch traffic logs.




