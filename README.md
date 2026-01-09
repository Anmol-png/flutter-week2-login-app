# 📱 Flutter Week 2: Data Management & Persistent Storage

A comprehensive Flutter application demonstrating state management and local data storage concepts through practical examples.

## 🎯 About

This project is part of **Week 2** curriculum focusing on data management and persistent storage in Flutter. It includes three main components:
1. **Login Screen** - User authentication interface
2. **Counter App** - Demonstrates state management with persistent storage
3. **To-Do List App** - Full CRUD operations with local storage

---

## ✨ Features

### 🔐 Login Screen
- Email validation (must contain @)
- Password visibility toggle (eye icon)
- Form validation with error messages
- Clean and modern UI design
- "Forgot Password?" option

### 🔢 Counter App
- ➕ Increment counter
- ➖ Decrement counter
- 🔄 Reset counter
- 💾 Auto-save functionality
- 📊 Real-time state updates
- Data persists across sessions

### ✅ To-Do List App
- ➕ Add new tasks
- ✔️ Mark tasks as complete/incomplete
- 🗑️ Delete tasks
- 📊 Task statistics (total & completed count)
- 💾 Persistent storage
- 📱 Responsive list view
- 🎨 Visual feedback (strikethrough for completed tasks)

---

## 📸 Screenshots

### Login Screen
```
┌─────────────────────┐
│   🔒 (Lock Icon)    │
│       Login         │
│                     │
│  📧 Email Field     │
│  🔒 Password Field  │
│                     │
│  Forgot Password?   │
│                     │
│   [Login Button]    │
└─────────────────────┘
```

### Home Screen
```
┌─────────────────────┐
│   Welcome to Home   │
│                     │
│  [Counter App]      │
│  [To-Do List App]   │
└─────────────────────┘
```

### Counter App
```
┌─────────────────────┐
│  Current Counter:   │
│        42           │
│                     │
│    [-]    [+]       │
└─────────────────────┘
```

### To-Do List
```
┌─────────────────────┐
│  [Add Task Field]   │
│                     │
│  ☑ Buy groceries    │
│  ☐ Study Flutter    │
│  ☐ Read a book      │
└─────────────────────┘
```

---

## 🚀 Installation

### Prerequisites
- Flutter SDK (3.0.0 or higher)
- Dart SDK (3.0.0 or higher)
- Android Studio / VS Code
- Git

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/Anmol-png/flutter-week2-app.git
   cd flutter-week2-app
   ```

2. **Get dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   
   For Web:
   ```bash
   flutter run -d chrome
   ```
   
   For Android/iOS:
   ```bash
   flutter run
   ```

4. **Build APK (Android)**
   ```bash
   flutter build apk --release
   ```

---

## 💻 How to Use

### Login Screen
1. Enter a valid email (must contain @)
2. Enter a password
3. Click the eye icon to show/hide password
4. Click "Login" button to proceed

### Counter App
1. Click **+** button to increment
2. Click **-** button to decrement
3. Click refresh icon (top-right) to reset
4. Counter value saves automatically
5. Refresh the app - your counter value persists!

### To-Do List App
1. Type a task in the input field
2. Press Enter or click the **+** button to add
3. Click checkbox to mark task as complete
4. Click 🗑️ icon to delete a task
5. View statistics at the top (Total & Completed)
6. All tasks are saved automatically

---

## 📚 Week 2 Learning Objectives

### ✅ Completed Objectives:

#### 1. State Management Basics
- **Concept**: Using `setState()` to manage widget state
- **Implementation**: Counter app demonstrates real-time state updates
- **Code Example**:
  ```dart
  void _incrementCounter() {
    setState(() {
      _counter++;
    });
  }
  ```

#### 2. Persistent Data Storage
- **Concept**: Save and retrieve data locally
- **Implementation**: Storage service for saving counter and tasks
- **Features**:
  - Counter value persists across sessions
  - Tasks saved in JSON format
  - Automatic data synchronization

#### 3. Simple List App (To-Do List)
- **Features Implemented**:
  - ✅ Add tasks
  - ✅ Display tasks in ListView
  - ✅ Mark tasks as complete
  - ✅ Delete tasks
  - ✅ Save tasks using local storage
  - ✅ Task statistics

---

## 📁 Project Structure

```
lib/
├── main.dart                 # Main application file
│   ├── StorageService        # Custom storage service
│   ├── LoginScreen           # Login UI with validation
│   ├── HomeScreen            # Navigation hub
│   ├── CounterApp            # State management demo
│   └── TodoListApp           # CRUD operations demo
```

### Key Components:

**StorageService Class**
- Handles data persistence
- In-memory storage (web-compatible)
- Can be upgraded to SharedPreferences for mobile

**State Management**
- Uses `setState()` for UI updates
- Lifecycle methods (`initState`)
- Data loading on app start

**UI Components**
- TextFormField with validation
- ListView.builder for dynamic lists
- FloatingActionButton for actions
- Card widgets for task items

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **Flutter** | UI Framework |
| **Dart** | Programming Language |
| **Material Design** | UI Components |
| **setState()** | State Management |
| **JSON** | Data Serialization |
| **StorageService** | Data Persistence |

---

## 🎓 What I Learned

### Week 2 Concepts:

1. **State Management**
   - How `setState()` triggers UI rebuilds
   - Managing local state within widgets
   - Updating UI based on user interactions

2. **Data Persistence**
   - Saving data locally
   - Loading data on app startup
   - Converting objects to JSON

3. **Form Validation**
   - Using GlobalKey for form state
   - Custom validators
   - User input validation

4. **ListView Operations**
   - Dynamic list rendering
   - Adding/removing items
   - Updating list items

---

## 🐛 Known Issues

- Storage uses in-memory for web (data clears on page refresh)
- For mobile persistent storage, upgrade to SharedPreferences package

### Solution for Mobile Persistence:

1. Add to `pubspec.yaml`:
   ```yaml
   dependencies:
     shared_preferences: ^2.2.2
   ```

2. Replace StorageService with SharedPreferences implementation

## 📝 License


### Version History

- **v1.0.0** (2025-01-10)
  - Initial release
  - Login screen implementation
  - Counter app with state management
  - To-Do list with persistent storage
  - Web-compatible storage service
  ---

**Happy Coding! 🚀**

---
