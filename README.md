# 🩺 Medical Transcription Dataset Cleaner

This project provides a cleaned version of the [mtsamples medical transcription dataset](https://www.mtsamples.com/), containing real-world clinical transcription reports. It is intended for educational and machine learning purposes, such as medical NLP, specialty classification, symptom tagging, and more.

---

## 📄 Dataset Overview

- 📊 **Total Samples:** 4,999
- 🧠 **Columns:**

| Column Name        | Description |
|--------------------|-------------|
| `description`      | A short title summarizing the case |
| `medical_specialty`| The medical field involved (e.g., Cardiology, Neurology) |
| `sample_name`      | Unique label identifying the sample |
| `transcription`    | Full medical transcription (clinical report) |
| `keywords`         | Comma-separated keywords related to the case |

> Note: The dataset originally had an index column `Unnamed: 0` which has been removed in the cleaned version.

---

## 🧹 Data Cleaning Performed

- ✅ Removed unnecessary index column (`Unnamed: 0`)
- ✅ Dropped or handled rows with null `transcription` or `keywords`
- ✅ Standardized case and spacing
- ✅ Ensured all records contain clean, usable data for NLP modeling

---

## 🧪 Usage Example



You can load and explore the cleaned dataset in a notebook:

```python
import pandas as pd

df = pd.read_csv("mtsamples.csv")

# View structure
print(df.shape)
print(df.columns)

# View sample
df.head()
```



📊 Example Records
Description	Medical Specialty	Keywords (Preview)
2-D M-Mode. Doppler.	Cardiovascular / Pulmonary	doppler, echocardiogram, heart
A 23-year-old white female...	Allergy / Immunology	allergic rhinitis, immunology
Consult for gastric bypass	Bariatrics	gastric bypass, weight loss

🤖 Potential Applications
Medical NLP (Named Entity Recognition, Classification)

Text classification (by specialty or diagnosis)

Building medical question-answering systems

Summarization of clinical notes

🛠 Requirements
Install dependencies:

bash
Copy code
pip install pandas matplotlib seaborn
📌 License
This dataset and project are intended for educational purposes only. Please refer to mtsamples.com for original data ownership and usage terms.

👤 Author
Cleaned and maintained by Yekini Khalid Kolawole
