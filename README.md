

### **README.md**  

```md
# Entity Classification & Email Validation  

## 📌 Overview  
This project is designed to **classify names** as **Person, Company, or Unknown** and **validate email addresses** for accuracy and deliverability. It helps clean and refine datasets by identifying **registrant names** and detecting **invalid emails**.  

## 🚀 Features  
✔️ **Name Classification**: Detects whether a given name belongs to a **person** or a **company**.  
✔️ **Handles Hindi & Arabic Names**: Uses predefined suffixes for better classification.  
✔️ **Detects Gibberish & Unknown Entries**: Filters out non-meaningful names.  
✔️ **Email Validation**: Checks if emails are correctly formatted and deliverable.  
✔️ **Dataset Processing**: Applies classification and validation to large datasets.  

## 🛠️ Installation  
Clone the repository:  
```bash
git clone https://github.com/yourusername/entity-classifier.git
cd entity-classifier
```
Install dependencies:  
```bash
pip install pandas spacy nltk email-validator
```
Download the required NLP model:  
```bash
python -m spacy download en_core_web_sm
```

## 📂 Usage  
### 1️⃣ **Classify Names**  
Run the script to classify names into **Person, Company, or Unknown**:  
```python
df['Entity_Type'] = df['Full_Name'].apply(classify_name)
```

### 2️⃣ **Validate Emails**  
Check if emails are valid and deliverable:  
```python
df['Email_validity'] = df['registrant_email'].apply(is_valid_email)
```

## 🔎 How It Works  
- **Rule-based classification**: Uses suffixes, company keywords, and NLP to differentiate **people from companies**.  
- **Gibberish detection**: Identifies names that are not meaningful.  
- **Email validation**: Ensures emails are correctly formatted and deliverable.  

## 📌 Example Output  
| Full Name        | Entity Type | Registrant Email      | Email Validity |
|------------------|------------|-----------------------|---------------|
| John Doe        | Person     | john@example.com     | ✅ Valid |
| ABC Tech LLC    | Company    | info@abctech.com     | ✅ Valid |
| Random String   | Unknown    | invalid-email        | ❌ Invalid |

## 🤝 Contributing  
Feel free to contribute! Open a pull request if you find any issues or improvements.  

## 📜 License  
This project is licensed under the **MIT License**.  

---

⭐ **If you find this project useful, give it a star!** ⭐
```
