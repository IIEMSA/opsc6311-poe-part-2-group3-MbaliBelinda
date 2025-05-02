Personal Budget Tracker App — Part 2: Prototype Development

📱 Overview

The Personal Budget Tracker is an Android app developed using Kotlin and RoomDB. It helps users log expenses, manage budgets, and track their financial habits through a clean, user-friendly interface. This prototype lays the foundation for the final app, focusing on core functionality, offline data persistence, and intuitive design.

✅ Key Features Implemented

🔐 User Authentication: Secure login with username and password.

🗂️ Custom Categories: Create and manage expense categories (e.g. Groceries, Transport).

🧾 Expense Entries: Add entries with:

Amount

Date

Description

Category

Optional receipt photo attachment

🎯 Budget Goals: Set minimum and maximum monthly spending goals.

📆 View by Period: Filter expenses by a user-selectable date range.

📊 Category Totals: See total spending per category for selected periods.

💾 Offline Support: All data stored using RoomDB (local SQLite-based persistence).

🧪 Automated Testing

Integrated unit tests for core functions (e.g., category creation, data persistence).

GitHub Actions used to automate testing and ensure compatibility across machines.

🛠️ Technologies Used

Kotlin

Android SDK

RoomDB

ViewModel + LiveData

Git & GitHub

GitHub Actions for CI/CD

🧪 GitHub Actions

This repository uses GitHub Actions to:

Automatically build the APK

Run unit tests

Verify code stability

Sample Workflow:

yaml
Copy
Edit
name: Android CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    name: Build APK and Run Tests
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Set up JDK
        uses: actions/setup-java@v2
        with:
          java-version: '11'
      - name: Build with Gradle
        run: ./gradlew build
