# MineSafe Risk Evaluator

**MineSafe Risk Evaluator** is a **Python Tkinter application** designed for **automated risk assessment** in mining environments. It uses **NLP-based hazard detection** (via Hugging Face’s `facebook/bart-large-mnli` model) and maps risks to **mitigation strategies** compliant with **CMR 2017 (Coal Mines Regulations)**.

---

## 📸 Screenshots

| Home Screen | Risk Evaluation Result |
| :---: | :---: |
| ![Screenshot 2025-04-28 093934](https://github.com/user-attachments/assets/ce747a06-9fc6-4e20-a1a1-08883d3cf1c7) | ![Screenshot 2025-04-28 094133](https://github.com/user-attachments/assets/3cb6a144-7497-46b7-a44b-90eac76e42f3) |

---

## 🚀 Features

- **Automated Hazard Detection**  
  Uses Zero-Shot Learning (BART NLI Model) to classify free-text hazard descriptions into known hazard categories.
  
- **Risk Scoring System**  
  Calculates risk score based on user input (Consequence × Exposure × Probability).

- **Dynamic Risk Level Assignment**  
  Assigns risk levels (Low, Medium, High, Critical) and suggests corresponding protocols.

- **Regulatory Control Mapping**  
  Links hazards to **CMR 2017** standards and recommended control measures.

- **Data Export**  
  Exports all evaluated risk entries into an **Excel file** for record-keeping.

---

## 🛠️ Tech Stack

- **Python 3.8+**
- **Tkinter** (for GUI)
- **Hugging Face Transformers** (`facebook/bart-large-mnli`)
- **Pandas** (for data handling and Excel export)

---

## 🧰 Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/minesafe-risk-evaluator.git
   cd minesafe-risk-evaluator
   ```

2. **Install Dependencies**
   ```bash
   pip install tkinter pandas transformers
   ```

3. **Run the Application**
   ```bash
   python minesafe_risk_evaluator.py
   ```

---

## ⚙️ How It Works

1. **Input**  
   - Enter a description of the hazard observed.
   - Enter ratings (1-10) for:
     - Consequence
     - Exposure
     - Probability

2. **Hazard Detection**  
   The app identifies the hazard category using **Zero-Shot Classification**.

3. **Risk Evaluation**  
   Calculates the **risk score** and **assigns a level** based on thresholds.

4. **Control Suggestion**  
   Displays the **appropriate CMR reference** and **recommended mitigation**.

5. **Data Management**  
   Optionally export the evaluations into an Excel spreadsheet.

---

## 📋 Risk Level Thresholds

| Risk Score | Level | Action |
|:-----------|:------|:-------|
| 1–20       | Low   | Monitor hazard |
| 21–200     | Medium| Prepare mitigation |
| 201–500    | High  | Apply safety controls |
| >500       | Critical | Suspend operations & notify authority |

---

## 📚 References

- **CMR 2017**: Coal Mines Regulations (India)
- **Hugging Face**: [facebook/bart-large-mnli](https://huggingface.co/facebook/bart-large-mnli)

---

## 📌 Future Improvements

- Add user authentication.
- Maintain historical records with timestamps.
- Visual analytics dashboard (risk heatmaps).
- Cloud integration for collaborative mining sites.

---
