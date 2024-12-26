# 🎯 **Universal QA Testing Framework**  
### **Your One-Stop Shop for Testing Excellence!**  

---

## 🌟 Imagine a World of Effortless Testing  

A land where **UI**, **API**, **Performance**, and **BDD** tests coexist in harmony.  
Where reports are not just functional but a **joy to behold**.  

Welcome to **Universal QA Testing Framework** —  
**Your key to unlocking efficient, maintainable, and artistically crafted automated tests!**  

---

## 🛠️ **Why Choose Universal QA Testing Framework?**

### **🔹 Modular Design**
- Clear sections: **UI**, **API**, **Performance**, **BDD**, and **Common** for easy navigation.

### **🔹 Reusable Utilities**
- Shared functions for configuration, logging, and data management to save coding time.

### **🔹 Page Object Model (POM)**
- Keeps your UI tests clean by separating page interactions from test logic.

### **🔹 API Testing Powerhouse**
- Simplifies API requests and response validation for seamless backend testing.

### **🔹 Performance Champion**
- Analyze and optimize your application's performance like a pro.

### **🔹 Behavior-Driven Development (BDD)**
- Collaborate easily with stakeholders using Gherkin syntax.

### **🔹 Customizable & Extensible**
- Tailored to your needs, making it effortless to add new features.

### **🔹 Reporting Artistry**
- Beautiful and insightful reports for every test type.

---

## 🔎 **File Structure Overview**

```plaintext
qa-testing-framework/
├── common/             # Shared utilities, helpers, and base classes
├── ui/                 # UI testing: Pages, tests, and drivers
├── api/                # API testing: Requests, tests, and schemas
├── performance/        # Performance testing: Scripts, reports, and analysis
├── bdd/                # BDD testing: Features, steps, and hooks
├── data/               # Test data (CSV, JSON, etc.)
├── reports/            # Test reports (UI, API, Performance)
├── requirements.txt    # Project dependencies
└── pytest.ini          # Pytest configuration

```

## 🚀 **Getting Started**

### **1️⃣ Install Dependencies**
Install the required dependencies using the following command:
```bash
pip install -r requirements.txt
```

### **2️⃣ Run Your Tests**
### ***UI Tests***
Run specific test types with these commands:
```bash
pytest ui/tests/
```
### ***API Tests***
```bash
pytest api/tests/
```
### ***Performance Tests***
Run Locust or JMeter scripts from performance/scripts/:
```bash
locust -f performance/scripts/user_journey.py
```
### ***BDD Tests***
```bash
behave bdd/features/
```
### **3️⃣ View the Reports**
Test results will be stored in the reports/ directory. Navigate there to view insightful and detailed reports.

## 💡 **Code Examples**
### ***UI Test Example***
```python
from ui.pages.login_page import LoginPage

def test_login(browser):
    login_page = LoginPage(browser)
    login_page.open()
    login_page.login("username", "password")
    assert login_page.is_user_logged_in()
```
### ***API Test Example***
```python
import requests

def test_get_users():
    base_url = "https://reqres.in/api"
    response = requests.get(f"{base_url}/users?page=1")
    assert response.status_code == 200
    assert len(response.json()["data"]) > 0
```
### ***Performance Script Example***
```python
from locust import HttpUser, TaskSet, task

class UserJourney(TaskSet):
    @task
    def browse_products(self):
        self.client.get("/products")

class WebsiteUser(HttpUser):
    tasks = [UserJourney]
    min_wait = 1000
    max_wait = 5000
```
## 🧩 ***Customization Guide***
### 1. Configuration:
Modify common/config.py to set up project-specific configurations like BASE_URL, API_KEY, and test data paths.

### 2. UI Locators:
Update ui/locators.py to match the elements in your application.

### 3. New Features:

Add Gherkin-style test scenarios in bdd/features/.
Extend api/requests/ or ui/pages/ to handle new features.

## 🌈 ***Let's Build Happy Code Together!***
This framework is your playground for creating magnificent automated tests.
Dive into the code and turn your testing vision into reality!

#### ✨ ***Remember, beautiful code is happy code.*** ✨

## 📢 ***Disclaimer***
This framework is an artistic interpretation of the concept.
You may need to adjust it based on your testing tools and libraries.
