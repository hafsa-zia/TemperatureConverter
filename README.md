# Temperature Converter — Failure Injection (Option B: Software Bug)

This project is a single-page modern dark-themed web app that converts temperatures from **Fahrenheit (°F) to Celsius (°C)**.  
It includes a **Failure Injection Toggle** that simulates a **Software Bug**, producing incorrect results and structured error logs.

The assignment requirement “Simulate Real-World Failures in a Tiny Web App” is fully implemented.

---

## 🚀 Features

### ✅ Normal Mode (Failure OFF)
- Uses **correct formula**:  
  **(F − 32) × 5/9**
- Displays accurate Celsius output
- No error banners
- No error logs

### ❌ Failure Mode (Failure ON)
Simulates a **Software Bug** (Option B):

- Uses **wrong formula**:  
  **(F − 32) / 1.5**
- Displays a red crash banner:  
  **“Calculation anomaly detected (BUG: wrong formula)”**
- Prints a **JSON structured error log** in the browser console

---

## 🎨 UI / Styling
- Premium **dark theme**
- Glassmorphism card container
- Smooth animations & hover interactions
- Highlighted result box
- Failure banner with glow

---

## 📦 How to Run
1. Download or clone the project.
2. Open **index.html** in any browser (Chrome, Firefox, Edge, etc.).
3. No server required — it is a pure static web app.

---

## 🧪 How to Trigger the Failure
1. Check the box labeled:  
   **“Inject Failure (Wrong Formula Bug)”**
2. Enter any Fahrenheit value.
3. Click **Convert**.
4. The crash banner appears.
5. The console logs a structured JSON bug report.

---

## 📝 Example Error Log (Failure Mode)
```json
{
    "timestamp": "2025-02-10T12:35:21.122Z",
    "function": "fahrenheitToCelsius",
    "input": 98,
    "result": 44,
    "expected": 36.6666667,
    "delta": -7.3333333,
    "error_code": "BUG_WRONG_FORMULA"
}
