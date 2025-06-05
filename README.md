# 📸 Facial Recognition Attendance System

## 📝 Description

This project is a **facial recognition-based attendance system** designed to **automate clock-ins and clock-outs** in schools and workplaces. Built with **Python** in a **Kaggle notebook**, the system uses **face detection models** (Haar cascades and OpenCV DNN) to detect users, records attendance in an **SQLite database**, and enforces **lateness penalties**.

The system ensures fairness, prevents buddy punching, and tracks attendance trends while comparing traditional and deep learning-based detection methods. It supports multiple daily clock-ins, enforces punctuality rules, and provides **performance analytics** on face detection accuracy.

---

## 🚀 Features

* 🎯 **Automated Clock-in/Clock-out** using face detection
* 🕒 **Late Penalty System**: late users must stay extra hours
* 🔁 **Multiple Clock-ins per Day** (e.g., before and after lunch)
* 📊 **Model Comparison**: Haar Cascades vs OpenCV DNN (SSD-ResNet)
* 🧠 **Accuracy Analysis**: detection rate, false positives, processing time
* 💾 **SQLite Integration** for attendance logging and analysis
* 📈 **Visualization** of model performance and lateness data
* 📷 **Face Detection Only**, not full facial recognition (no user identity matching yet)

---

## 🧰 Tech Stack

| Component          | Description                            |
| ------------------ | -------------------------------------- |
| **Language**       | Python                                 |
| **Notebook**       | Kaggle Notebook                        |
| **Face Detection** | Haar Cascades, OpenCV DNN (SSD+ResNet) |
| **Data Storage**   | SQLite Database                        |
| **Dataset**        | LFW (Labeled Faces in the Wild)        |
| **Visualization**  | Matplotlib, Seaborn                    |

---

## 📂 Project Structure

```bash
facial-attendance/
├── face_detection/
│   ├── haar_cascade.py
│   └── dnn_model.py
├── attendance_logic/
│   ├── clock_in_out.py
│   └── lateness_penalty.py
├── database/
│   ├── db_setup.py
│   └── log_attendance.py
├── visualization/
│   ├── performance_plot.py
│   └── trends.py
├── test_cases/
│   ├── simulate_users.py
│   └── random_face_images/
└── main.ipynb  # Kaggle notebook
```

---

## 📌 Key Logic

* **Late morning clock-in** ➜ extra time added to evening shift
* **Late post-lunch return** ➜ more work added to the day
* **Missed clock-ins** ➜ time distributed over following days
* **Each detection logs a confidence score** (to compare model performance)

---

## 📊 Performance Comparison

| Metric                | Haar Cascades | OpenCV DNN |
| --------------------- | ------------- | ---------- |
| Detection Rate        | Moderate      | High       |
| False Positives       | High          | Low        |
| Processing Speed      | Fast          | Slower     |
| Accuracy in Low Light | Low           | High       |

---

## 🔮 Future Improvements

* Integrate **face recognition** to identify individuals
* Add **live webcam support** for real-time usage
* Replace SSD-ResNet with **MobileNet** for faster, lighter DNN inference
* Deploy as a **desktop or web app**

---

## 🧪 How to Use

1. Load `main.ipynb` on Kaggle
2. Run all cells to simulate detection and attendance logging
3. Analyze results via plots and database entries
4. Compare model performance under varying conditions

---

## 📖 License

This project is open-source and available under the **MIT License**.

---

## 💬 Discussion

Would you adopt facial recognition for attendance in your workplace or school?
Let us know your thoughts and feedback in the comments!

---
