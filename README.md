# Concert-Ticket-Selling-using-Tkinter-GUI

# 🎼 Event Organizer Desktop App

A desktop-based **Event Organizer and Ticketing System** built with **Python Tkinter, MySQL, and Scikit-Learn**.
This project allows users to browse classical music events, register/login, buy tickets, manage their wallet, and receive **personalized event recommendations** using **content-based filtering with cosine similarity**.

---

## ⚠️ Important Before Running

> **IMPORTANT:** Before running this project, you **MUST update your MySQL credentials inside `sql.py` first**.

Please change this section in `sql.py`:

```python
host="localhost"
user="root"
password="your_mysql_password"
```

Adjust it to match your local MySQL configuration.

> The database will be automatically created and seeded with sample data when the application starts.

### ▶️ Only Run This File

```bash
python app2.py
```

✅ **Only run `app2.py`** as the main entry point of the application.
Other files such as `classes.py`, `functions.py`, and `sql.py` are **supporting modules only**.

---

## ✨ Features

### 👤 User Management

* User registration
* Login & logout system
* Profile editing
* Wallet balance tracking
* Top-up wallet support

### 🎟️ Ticketing System

* Browse available events
* View event details
* Buy tickets with quantity control
* Maximum 5 tickets per event per user
* Sell owned tickets back
* View personal ticket cart

### 🔍 Search, Filter, Sort

* Search events by name
* Filter by:

  * All events
  * Passed events
  * Coming soon
* Sort by:

  * Name
  * Genre
  * Price
  * Schedule
* Ascending / Descending ordering

### 💳 Payment System

* Wallet payment
* Credit card
* Debit card
* PayPal
* Bank transfer
* Payment countdown timer (1 minute)

### 🤖 Smart Recommendation System

Personalized recommendations are generated using:

* User preference vector
* Event attribute vector
* Cosine similarity
* Content-based filtering

---

## 🧠 Recommendation Algorithm

The recommendation system uses:

```python
cosine_similarity(user_preferences, event_attributes)
```

Each event has attributes such as:

* Symphony
* Concerto
* Orchestral
* Chamber
* Choral
* Ballet
* Themed

The system compares user ticket history with event genre vectors, then returns the **Top-N most similar events**.

---

## 🏗️ Project Structure

```bash
├── app2.py          # Main Tkinter application (RUN THIS FILE)
├── classes.py       # OOP models: Ticket, Event, Account
├── functions.py     # Utility functions + recommendation logic
├── sql.py           # MySQL database setup and queries
├── imgs/            # Event and UI assets
└── README.md
```

---

## 🧱 Tech Stack

* Python
* Tkinter
* MySQL
* mysql-connector-python
* Pillow
* scikit-learn
* OOP
* Content-Based Recommendation System

---

## 🚀 Installation

### 1) Clone Repository

```bash
git clone https://github.com/yourusername/event-organizer.git
cd event-organizer
```

### 2) Install Dependencies

```bash
pip install mysql-connector-python pillow scikit-learn
```

### 3) Configure MySQL Account

Open `sql.py` and update:

```python
host="localhost"
user="root"
password="your_mysql_password"
```

### 4) Run Application

```bash
python app2.py
```


## 🎯 Learning Objectives

This project demonstrates:

* Object-Oriented Programming (OOP)
* GUI application development
* MySQL database integration
* CRUD operations
* recommendation systems
* cosine similarity
* event-driven programming
* desktop software architecture
