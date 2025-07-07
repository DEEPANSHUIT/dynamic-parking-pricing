#  Dynamic Pricing for Urban Parking Lots

This project implements real-time pricing for urban parking lots using data streaming and machine learning logic in Python.

## 🔧 Tech Stack

- **Python 3.10+**
- **Pathway** for real-time stream processing
- **Pandas** for initial CSV handling
- **Bokeh** for data visualization
- **Google Colab / Jupyter** for development and testing

## 🧠 Project Overview

The goal is to calculate dynamic parking prices in real time using features such as:
- Occupancy
- Queue length
- Traffic level
- Special event days
- Vehicle type

Prices are calculated using 3 models:
1. **Model 1** – Linear based on occupancy
2. **Model 2** – Demand-based dynamic pricing
3. **Model 3** – Adds random competitive variation to Model 2

## 🏗️ Architecture Diagram

```mermaid
graph TD
    A[CSV File: parking_stream.csv] --> B[Pathway Stream Engine]
    B --> C[Feature Engineering]
    C --> D[Demand Calculation]
    D --> E1[Model 1 Pricing]
    D --> E2[Model 2 Pricing]
    D --> E3[Model 3 Pricing]
    E1 --> F[Final Table]
    E2 --> F
    E3 --> F
    F --> G[Bokeh Dashboard for Visualization]
