# ⏰ Task Reminder Automation (Power Automate Desktop)
---


## 📌 Project Overview
This project is a simple **Task Reminder Automation Flow** built using **Power Automate Desktop (PAD)**.  
It reads scheduled tasks from an Excel file and shows a popup reminder when the current system time matches the scheduled time.

---

## ⚙️ How It Works

1. The flow runs in an infinite loop (`While True`).
2. It opens an Excel file:
```

C:\Users\Sameer Traders\Desktop\Reminders.xlsx

```
3. It reads task data from Excel range **A2:B4**.
4. It gets the current system time in **HH:mm** format.
5. It loops through each row:
- Column A → Scheduled Time
- Column B → Task Description
6. If the scheduled time matches the current time:
- A **popup reminder message** is shown.

---

## 📊 Excel Structure

Your Excel file should look like this:

| A (Time) | B (Task)        |
|----------|-----------------|
| 09:00    | Morning Break   |
| 13:00    | Lunch Time      |
| 17:00    | End Work Review |

---

## 🧠 Logic Flow

```

Start Loop (Infinite)
↓
Open Excel File
↓
Read Task Data (A2:B4)
↓
Get Current Time (HH:mm)
↓
For Each Row:
↓
If Scheduled Time == Current Time
↓
Show Reminder Popup
End Loop

````

---

## 🛠️ Features

- ⏱ Real-time time checking
- 📂 Excel-based task management
- 🔔 Instant popup reminders
- 🔁 Continuous background execution
- 🖥 Simple and lightweight automation

---

## 📁 Project Files

- `Flow.pad` → Power Automate Desktop workflow
- `README.md` → Project documentation
- `/images` → Screenshots of workflow steps

---


---

## 🚀 Future Improvements

* Add sound alert with popup
* Run in system tray mode
* Send email reminders
* Add task completion tracking
* Store logs of reminders shown

---


