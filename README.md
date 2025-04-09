# 📝 Task Tracker CLI

A simple yet elegant task tracking command-line tool built with [Cobra](https://github.com/spf13/cobra) in Go. Easily add, view, complete, and delete tasks — all from your terminal.

---

## 🚀 Features

- ✅ Add new tasks
- 📋 View tasks by status (all, complete, incomplete)
- 🗑️ Delete tasks
- ☑️ Mark tasks as complete
- 📦 Save tasks to a local `tasks.json` file

---

## 📦 Installation

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/task-tracker-cli.git
cd task-tracker-cli
```

### 2. Build the Binary

```bash
go build -o task-tracker-cli
```

### 3. (Optional) Move to Global Path

```bash
sudo mv task-tracker-cli /usr/local/bin/
```

---

## 🛠 Usage

### 1. Add a Task

```bash
task-tracker-cli addTask "Finish writing blog"
```

### 2. View Tasks

```bash
task-tracker-cli viewTasks
task-tracker-cli viewTasks --status all
task-tracker-cli viewTasks --status complete
task-tracker-cli viewTasks --status in-progress
task-tracker-cli viewTasks --status not-started
```

### 3. Mark As Done

```bash
task-tracker-cli markAsDone 2
```

### 4. Change Status

```bash
task-tracker-cli changeStatus 2 complete
```

### 5. Delete Task

```bash
task-tracker-cli deleteTask 3
```

---

## 🖼 Output Preview

<img width="318" alt="Screenshot 2025-04-09 at 3 21 11 PM" src="https://github.com/user-attachments/assets/abd094d5-e2c3-47f9-994f-7d1dd4f61dc3" />

---

## 📂 Data Format

Tasks are stored in a local JSON file named tasks.json.

```json
[
  {
    "ID": 1,
    "Title": "Finish writing blog",
    "Completed": false
  }
]
```

---

## 📚 Tech Stack

- [Go](https://go.dev/)
- [Cobra CLI](https://github.com/spf13/cobra)
- [tablewriter](https://github.com/olekukonko/tablewriter)
- [faith/color](https://github.com/fatih/color)
