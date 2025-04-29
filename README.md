# Edlerly Physio Datasets

This repository contains five datasets related to physiological signals including **Heart Rate (HR)**, **Sleep Stages**, and **Oxygen Saturation (SpO₂)**. These datasets are intended for research and development purposes such as predictive modeling, digital twin systems, health monitoring, and sleep analysis.

---

## 📚 Datasets Overview

### 1. Heart Rate Dataset
- **Description**: Records the heart rate (beats per minute) at specific timestamps.
- **Sample**:
  | date       | time    | bpm |
  |------------|---------|-----|
  | 25/06/2024 | 10:10:15| 73  |
  | 25/06/2024 | 10:10:20| 71  |
  | 25/06/2024 | 10:10:25| 76  |
- **Columns**:
  - `date`: Measurement date (DD/MM/YYYY)
  - `time`: Measurement time (HH:MM:SS)
  - `bpm`: Heart rate in beats per minute

---

### 2. Heart Rate and Sleep Dataset
- **Description**: Combines heart rate measurements with corresponding sleep stages per minute.
- **Sample**:
  | dateTime         | bpm | level |
  |------------------|-----|-------|
  | 6/26/2024 1:52   | 75  | deep  |
  | 6/26/2024 1:53   | 71  | deep  |
  | 6/26/2024 1:54   | 71  | deep  |
  | 6/26/2024 1:55   | 86  | deep  |
- **Columns**:
  - `dateTime`: Timestamp (MM/DD/YYYY HH:MM)
  - `bpm`: Heart rate in beats per minute
  - `level`: Sleep stage (`deep`, `light`, `rem`, `wake`, etc.)

---

### 3. Sleep Dataset
- **Description**: Records the sleep stage levels at every minute interval without heart rate data.
- **Sample**:
  ```json
  [
    {
      "dateTime": "2024-10-08T03:02:00",
      "level": "asleep"
    },
    {
      "dateTime": "2024-10-08T03:03:00",
      "level": "asleep"
    },
    {
      "dateTime": "2024-10-08T03:04:00",
      "level": "asleep"
    }
  ]
  ```
- **Fields**:
  - `dateTime`: ISO 8601 format timestamp
  - `level`: Sleep state (`asleep`, `awake`, `restless`, etc.)

---

### 4. SpO₂ Dataset
- **Description**: Contains blood oxygen saturation (SpO₂) values measured over time.
- **Sample**:
  | dateTime         | spo2_value |
  |------------------|------------|
  | 6/25/2024 10:15  | 97.3       |
  | 6/25/2024 10:16  | 50         |
  | 6/25/2024 10:17  | 50         |
  | 6/25/2024 10:18  | 50         |
- **Columns**:
  - `dateTime`: Timestamp (MM/DD/YYYY HH:MM)
  - `spo2_value`: Blood oxygen saturation percentage

---

### 5. SpO₂, Heart Rate, and Sleep Dataset
- **Description**: Integrates heart rate, SpO₂, and sleep stage data recorded simultaneously per minute.
- **Sample**:
  | dateTime         | bpm | spo2_value | level    |
  |------------------|-----|------------|----------|
  | 6/26/2024 1:58   | 109 | 95.6       | restless |
  | 6/26/2024 1:59   | 101 | 95.9       | light    |
  | 6/26/2024 2:00   | 104 | 96.9       | light    |
  | 6/26/2024 2:01   | 103 | 96.2       | light    |
  | 6/26/2024 2:02   | 103 | 96.3       | light    |
- **Columns**:
  - `dateTime`: Timestamp (MM/DD/YYYY HH:MM)
  - `bpm`: Heart rate in beats per minute
  - `spo2_value`: Blood oxygen saturation percentage
  - `level`: Sleep stage (`light`, `deep`, `rem`, `restless`, etc.)

---

## 📌 Notes
- **Timestamp Formats**: Ensure consistent parsing (ISO or localized formats depending on your processing needs).
- **Missing Values**: May exist and should be handled appropriately during preprocessing.
- **Use Cases**: Suitable for heart rate prediction, sleep pattern detection, health monitoring systems, digital twin applications, and physiological anomaly detection.

---

## 📄 License
This dataset is released for **research and educational purposes only**. Commercial use is prohibited without prior permission.
