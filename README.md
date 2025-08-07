# Detection of Fake and Clone Twitter Accounts

## 📌 Project Overview

This project is a Django-based web application that detects fake or clone Twitter accounts using a combination of rule-based classification and machine learning. It analyzes user profiles, tweets, and behavioral metrics to classify accounts as genuine or fake. The system supports data upload, visualization, account analysis, and detailed reasoning for each classification.

---

## 🗂️ Project Structure

```
Detection-of-fake-and-clone-accounts-in-Twitter/
│
├── Detection_of_fake_and_clone_accounts_in_Twitter/   # Main Django Project
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── Remote_User/                                      # Frontend: User interface
│   ├── templates/Remote_User/
│   │   ├── UploadData.html
│   │   ├── ViewYourProfile.html
│   │   ├── CheckFakeAccounts.html
│   │   └── ...
│   ├── urls.py
│   └── views.py
│
├── Service_Provider/                                 # Backend: Admin interface
│   ├── templates/Service_Provider/
│   │   ├── Train_Model.html
│   │   ├── View_All_Twitter_Data.html
│   │   ├── View_Fake_Accounts.html
│   │   └── ...
│   ├── urls.py
│   └── views.py
│
├── DB/                                               # SQLite Database
│   └── db.sqlite3
│
├── static/                                           # Static files (CSS, JS)
│
├── manage.py
└── README.md                                         # This file
```

---

## 👩‍💻 How to Run the Project

### Prerequisites

* Python 3.8+
* pip
* Django 3.x
* Pandas
* NumPy
* Scikit-learn

### Installation Steps

1. **Clone the Repository**

```bash
git clone https://github.com/your-username/Detection-of-fake-and-clone-accounts-in-Twitter.git
cd Detection-of-fake-and-clone-accounts-in-Twitter
```

2. **Create a Virtual Environment**

```bash
python -m venv env
source env/bin/activate  # On Windows use: env\Scripts\activate
```

3. **Install Required Packages**

```bash
pip install -r requirements.txt  # If you have it, otherwise manually:
pip install django pandas scikit-learn numpy
```

4. **Run Migrations**

```bash
python manage.py makemigrations
python manage.py migrate
```

5. **Start the Server**

```bash
python manage.py runserver
```

6. **Access in Browser**

* User: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
* Service Provider: [http://127.0.0.1:8000/serviceproviderlogin/](http://127.0.0.1:8000/serviceproviderlogin/)

---

## 🔧 Functionality Breakdown

### 👤 User Interface (`Remote_User`)

* Upload raw Twitter data (`UploadData.html`)
* Analyze your profile (`ViewYourProfile.html`)
* View detection result with reason (`CheckFakeAccounts.html`)

### 🛠️ Service Provider Interface (`Service_Provider`)

* View all uploaded Twitter data
* View and verify detected fake accounts
* Train detection model using Decision Tree (C4.5)
* Analyze results through visualizations (graphs, scores)

---

## 🧠 Algorithms Used

### 1. **C4.5 Decision Tree**

* A rule-based machine learning algorithm used for classifying Twitter accounts based on multiple attributes.
* It builds a tree-like model using entropy and information gain to split data and make decisions.

### 2. **Similarity Metrics**

* Used to detect clone accounts by comparing username, bio, and network features.
* Accounts with high similarity to known real users but low activity/engagement are flagged as clones.

---

## 📈 Visualizations

* Line graph of tweet categories and their scores
* Pie chart of fake vs genuine accounts
* Accuracy and result summary per account

---

## 📌 Tools Used

* **Django**: Web framework
* **SQLite**: Lightweight DB for storing user and tweet data
* **Scikit-learn**: ML model training and prediction
* **Pandas**: Data manipulation and preprocessing
* **Matplotlib/Plotly**: Data visualization

---

## 🧑‍💼 Author

**Vamsi Krishna Thokala**

