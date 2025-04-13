# 🧭 **Browsing Directories with the Linux Terminal**

## 🎯 Learning Objectives
By the end of this note, you will be able to:
- 🧠 **Describe** what a Linux terminal is used for
- 💡 **Use** `pwd` and `ls` commands to browse directories

---

## 💻 What is the **Linux Terminal**?

The **Linux terminal** (also called the **command line** or **command prompt**) is like a magic doorway to your computer! ✨  
You type **commands**, hit **Enter**, and *boom!*—the computer listens and acts. No mouse needed!

> 🟦 **Example Prompt**:  
```
/home/project $
```
- `/home/project` → This is your **current directory** (aka where you are right now in your system).
- `$` → This is the **command prompt** waiting for your command.

---

## 📍 **pwd** – "Print Working Directory"

Want to know *where you are* in the file system?

👉 Use the `pwd` command:
```
$ pwd
/home/project
```

✅ Output: This shows you the **full path** of the directory you're currently in.  

🧠 **Think of it like checking your GPS location on your phone.**

---

## 📂 **ls** – "List"

Want to **see what's inside** the folder you're in?

👉 Use the `ls` command:
```
$ ls
```

If there’s **nothing inside**, you’ll see... well, *nothing*. 😅  
The `ls` command is polite—it doesn't even print a blank line if the directory is empty.

> 🧪 **Try this**:
```
$ ls /home
```

✅ Output:
```
project  theia
```

🎯 This shows the two **subdirectories** inside `/home`:
- `project`
- `theia`

---

## 🗂️ What is a **Directory**?

A **directory** is just like a **folder** on your computer:
- It can contain **files** 📝
- It can also contain **other directories** (aka **subdirectories**) 📁

Example:
```
/home/project
```
This means:
- You are inside a folder named `project`
- That folder lives inside another folder named `home`

📌 Tip: Think of the file system like a 🌳 **tree**:
- The root is `/` (just a single slash)  
- From there, everything **branches out**  
  Example: `/home/theia`, `/home/project`, `/etc`, `/usr`, etc.

---

## 🧠 Recap Time!

✅ The **Linux terminal** lets you interact with your system by typing commands.  
✅ Use `pwd` to see **where you are** in the directory tree.  
✅ Use `ls` to **look around** and see what’s inside a directory.  
✅ Directories are like folders; they can contain **files** and other **directories**.  
✅ The root of the file system is `/`.

---

## 🧪 Challenge Time!

Try running these on your Linux terminal:
1. `pwd` – What directory are you currently in?
2. `ls` – Is there anything in your current directory?
3. `ls /` – What’s at the root level of your file system?
4. `ls /home` – What users or directories are inside `/home`?

---

## 🎉 You Did It!

You're officially on your way to becoming a **Linux pro**! 🐧💪  
Exploring the terminal is like going on a treasure hunt—every command reveals something new! 🗺️

---

Sure! Here's an **interactive, in-depth explanation note** on:

---

# 🖥️ Linux Terminal Tips: Tab Completion & Command History

---

## 🎯 Learning Objectives
By the end of this session, you’ll be able to:

✅ Use **Tab Completion** to speed up your typing  
✅ Use **Command History** to navigate and rerun previous commands

---

## 🧩 What is Tab Completion?

**Tab Completion** is a *keyboard shortcut* that auto-fills a command, filename, or directory name when you press the `Tab` key.

### 🧪 Real-Life Example:

Let’s say your **home directory (~)** has the following folders:

```
Pictures/
Videos/
Documents/
Downloads/
```

Now you want to **go to the `Pictures` folder** using the terminal.

If you type:
```
cd P
```
and then press `Tab` → The terminal **autocompletes** it for you:
```
cd Pictures/
```

Why? Because `Pictures` is the **only folder starting with “P”**.

---

### 🧠 What if There Are Similar Names?

Let’s try:

```
cd Do
```
🛑 Nothing happens when you press `Tab`. Why?  
There are **two folders** starting with “Do” → `Documents/` and `Downloads/`.

Now try:
```
cd Doc
```
✅ Pressing `Tab` now autocompletes:
```
cd Documents/
```

Press `Tab` **again** → and it autocompletes deeper:
```
cd Documents/python-examples/
```

✨ With just a few keystrokes, you navigated a deep path!

---

## 🕹️ Command History

The **command history** lets you **reuse previously typed commands** using the **Up (`↑`)** and **Down (`↓`)** arrow keys.

---

### 🧪 Scenario Example:

You've just typed:
```bash
cd ~/Documents/python-examples
python3 myprogram.py
# Output: Hello, World!
cd /
```

Now you’re at the root directory `/`.

### ⏪ Want to return to your Python file folder?

Just press the `Up Arrow (↑)` key **3 times**:

1️⃣ `cd /`  
2️⃣ `python3 myprogram.py`  
3️⃣ `cd ~/Documents/python-examples`

💡 Output lines (like `Hello, World!`) are *not* counted as commands.

---

### 🔁 Navigation Tips:
- **Keep pressing `↑`** to go further back in history.
- **Pressed too far?** Hit the `Down Arrow (↓)` to go forward.

---

## ✅ Summary

You’ve just unlocked **two power tools** for faster terminal usage:

| Feature | Purpose | Shortcut |
|--------|--------|---------|
| 🧩 **Tab Completion** | Autocomplete directory/file names | `Tab` |
| 🔁 **Command History** | Reuse previous commands | `↑` & `↓` |

---

## 🚀 Try It Yourself!

1. Type: `cd D` → Hit `Tab`  
2. Type: `cd ~/Documents/python-examples`  
3. Run: `python3 myprogram.py`  
4. Use `↑` to rerun both without retyping!

---
Got it! Here's the **complete version of Exercise 1** (which may have gotten disrupted earlier due to network issues), fully explained for clarity and ease of learning:

---

# 💻 **Exercise 1 - Basic Terminal Commands**

In this exercise, you'll practice using simple terminal commands to interact with the file system.

---

### 🔹 **1.1. Listing files and directories**

✅ **Command:**
```bash
ls
```

📝 This lists all **files and directories** in your **current working directory**.

📌 **Example Output:**
```
Desktop  Documents  Downloads  Pictures  project
```

---

### 🔹 **1.2. Viewing your current working directory**

✅ **Command:**
```bash
pwd
```

📌 This stands for "**Print Working Directory**" and shows your **current location** in the file system.

📌 **Example Output:**
```
/home/theia
```

---

### 🔹 **1.3. Viewing the contents of a specific directory**

✅ **Command:**
```bash
ls /bin
```

📌 Lists the files in the **`/bin`** directory, which typically contains **binary executables** (commands like `ls`, `cp`, etc.).

📌 **Example Output:**
```
bash  cat  cp  ls  mkdir  mv  rm  sh  touch
```

---

### 🔹 **1.4. Viewing the contents of your home directory**

✅ **Command:**
```bash
ls ~
```

📌 The `~` symbol refers to your **home directory**. This command lists everything in `/home/theia`.

📌 **Example Output:**
```
Documents  Downloads  project
```

---

### 🔹 **1.5. Viewing the contents of the root directory**

✅ **Command:**
```bash
ls /
```

📌 The `/` symbol refers to the **root directory**, the topmost level of the Linux file system.

📌 **Example Output:**
```
bin  boot  dev  etc  home  lib  media  opt  proc  root  sbin  tmp  usr  var
```

---

✅ That completes **Exercise 1 – Basic Terminal Commands**.  

Here's the next engaging and exam-friendly interactive note for **"📂 Exam Time — Exercise 2: Navigating Directories with `cd`"**:

---

# 📂 **Exam Time — Exercise 2: Navigating Directories with `cd`**

🎯 **Goal:** Master how to move around the Linux file system using the `cd` (change directory) command.

---

## 🗂️ **Shortcut Symbols Cheat Sheet**

| Symbol | Meaning                    | Stands for                      |
|--------|----------------------------|----------------------------------|
| `~`    | Home                       | `/home/theia`                    |
| `/`    | Root                       | Top of the file system           |
| `.`    | Current directory          | Stay where you are               |
| `..`   | Parent directory           | One level up                     |

---

## 🏠 2.1 Change to Your **Home Directory**

```bash
cd ~
```

✅ Takes you to your home: `/home/theia`  
💬 Use `pwd` to confirm your current directory.

```bash
pwd
```

---

## 🔙 2.2 Change to **Parent Directory**

```bash
cd ..
```

📂 If you’re in `/home/theia`, this moves you up to `/home`.

---

## 🗃️ 2.3 Go to the **Root Directory**

```bash
cd /
```

🌳 Now you’re at the **top** of the file system tree.

---

## 👶 2.4 Change to a **Child Directory**

Assuming you're in `/`, move into `/bin` like this:

```bash
cd bin
```

📝 This works because `/bin` is a child of `/`.

### 🧠 Alternative Way:

```bash
cd ./bin
```

📌 `.` refers to the current directory  
⚠️ If you're already in `/bin`, doing `cd ./bin` will try to go to `/bin/bin`

---

## 🏃‍♂️ 2.5 Go Back to Your **Home Directory**

Two ways to do it:

🔁 Using full path:
```bash
cd ../home/theia
```

⚡ Shortcut way:
```bash
cd ~
```

Both land you back at `/home/theia`.

---

## 🧪 2.6 Go to Your **Project Directory**

🧱 `/home/project` is a **sibling** of `/home/theia`

📁 From `/home/theia`, run:

```bash
cd ../project
```

✅ Now you're in your **project directory** ready to work!

---

## ✅ Recap — What You Learned

🔹 `cd` = Change directory  
🔹 `..` = Move up  
🔹 `.` = Stay here  
🔹 `~` = Go home  
🔹 `/` = Go root  
🔹 `cd [folder-name]` = Move into child folder  
🔹 `cd ../[sibling-folder]` = Move to sibling folder

---

Here’s your interactive, exam-focused note for **Exercise 3 - Using Tab Completion and Command History**:

---

# ⌨️ **Exam Time — Exercise 3: Tab Completion & Command History**

🎯 **Goal:** Speed up your workflow and save effort by mastering keyboard shortcuts and smart typing tricks.

---

## 🔁 3.1 **Scroll Through Command History**

🔼 **Up Arrow** = Go **back** through previous commands  
🔽 **Down Arrow** = Go **forward** through history  

📌 **Example:**  
If you previously typed:

```bash
cd bin
```

👉 Hit `↑` to bring it back without retyping!  
💡 Use this when doing repetitive tasks like navigating directories.

⚠️ Make sure you're in the right working directory first (e.g., `/`) before running a historical command like `cd bin`.

---

## 🧠 **Pro Tip:** History isn't session-based — **it's persistent** across your session. So, your terminal remembers everything you've typed since opening it!

---

## 🚀 3.2 **Using Tab Completion Like a Pro**

### 📄 **Auto-complete Files & Directories**

Type part of a command or path, then press `Tab`:

```bash
cd /bi   + [Tab]
```

✅ Result:

```bash
cd /bin
```

### ❗ What if there’s more than one match?

Try this:

```bash
cd /b   + [Tab]
```

😐 Nothing happens.  
But...

👉 Hit `Tab` **again**, and it lists **all possible matches**:

```
bin/   boot/
```

Now type:

```bash
cd /bi   + [Tab]
```

✅ Now it autocompletes to `/bin` — since only one match exists.

---

## 🧱 Dig Deeper into Directories with Tab

Tab completion works **step by step**, like walking down a tree:

```bash
ls /home   + [Tab][Tab]
```

📋 You'll see:

```
project/   theia/
```

Now keep going:

```bash
ls /home/theia/dsdriver/bin   + [Tab]
```

🏁 Use Tab repeatedly to complete the full path step-by-step.

---

## 🧪 Practice Task!

Build this command using **Tab completion only**:

```bash
ls /home/theia/dsdriver/bin
```

Use Tab each time you go deeper:
- `/home` → `theia` → `dsdriver` → `bin`

---

## 📝 Recap — Key Shortcuts

| Shortcut         | What it does                      |
|------------------|-----------------------------------|
| ↑ / ↓ Arrow      | Browse command history            |
| `Tab`            | Auto-complete if one match exists |
| `Tab` x2         | Show options if multiple matches  |

---

### ✅ You’re now navigating like a Linux ninja!

Here’s your **interactive study note** for the **Practice Exercises** with emoji markers and clear steps to reinforce memory before exams:

---

# 🧪 **Practice Lab – Terminal Skills Recap**

🖥️ Master the core Linux terminal skills with these quick practice tasks! Great for revision.

---

## 1️⃣ **List the contents of the root directory**

📂 Root directory = `/`

✅ **Command:**
```bash
ls /
```

🧠 **Tip:** Use `ls /` anytime you want to see the top-level directories of the entire system.

---

## 2️⃣ **Change to your home directory**

🏠 Home directory shortcut = `~`

✅ **Command:**
```bash
cd ~
```

📝 In this lab, your home path is `/home/theia`  
👉 In real Linux systems: `/home/your-username`

---

## 3️⃣ **Verify your current working directory**

👣 Check where you are in the filesystem.

✅ **Command:**
```bash
pwd
```

🧾 Output should be:
```
/home/theia
```

---

## 4️⃣ **Use Tab Completion to go to `/bin`**

🚀 Practice navigating with Tab:

1. Start typing:
```bash
cd /b
```
2. Hit `Tab` → ❌ Nothing happens  
3. Hit `Tab` again → ✅ Shows options like:
```
bin/  boot/
```
4. Type:
```bash
cd /bi
```
5. Press `Tab` → Autocompletes to:
```bash
cd /bin
```

---

## 5️⃣ **Use Command History to return home**

🔁 Reuse previous commands with **Up Arrow** (`↑`)

1. Tap `↑` until you see:
```bash
cd ~
```
2. Hit `Enter` ✅

🧠 Saves time and typing effort!

---

## ✨ Summary Table:

| 🔧 Task                            | ✅ Command             |
|----------------------------------|------------------------|
| List root contents               | `ls /`                 |
| Go to home                       | `cd ~`                 |
| Show current directory           | `pwd`                  |
| Tab-complete to `/bin`           | `cd /bi + Tab`         |
| Use history to return to home    | `↑` until `cd ~`       |

---

