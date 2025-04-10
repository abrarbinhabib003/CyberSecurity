## 🧪 Burp Suite Learning Lab Setup  
🎯 *Practice hacking ethically with a safe, local website using DVWA + XAMPP*

---

### 🛠️ Tools Required
1. **XAMPP (Local Web Server)**
2. **DVWA (Damn Vulnerable Web Application)**

---

### 📥 Step 1: Download the Tools
- 🔍 **XAMPP** from: [https://www.apachefriends.org](https://www.apachefriends.org)  
  ➤ Choose version based on your OS (Windows/Linux/Mac)  
  ➤ It includes **Apache**, **MySQL**, **PHP** — everything you need.

- 🔍 **DVWA** from: 
    - Visit [DVWA's official site](http://www.dvwa.co.uk) for the download link. If unavailable, you can download the zip from its [GitHub repository](https://github.com/digininja/DVWA?tab=readme-ov-file).
    - 
  ➤ Download the ZIP file (`DVWA-master.zip`)


---

### 📂 Step 2: Install & Set Up XAMPP
- Install XAMPP (just Next → Next → Install).
- After installing:
  - Open **XAMPP Control Panel**
  - Start both **Apache** and **MySQL** modules

---

### 🗂️ Step 3: Setup DVWA in XAMPP
1. Extract the `DVWA-master.zip`
2. Rename the extracted folder to `dvwa`
3. Move this folder into:
   ```
   C:\xampp\htdocs\
   ```
4. Your path should look like:
   ```
   C:\xampp\htdocs\dvwa\
   ```

---

### ⚙️ Step 4: Configure DVWA
1. Navigate to:
   ```
   C:\xampp\htdocs\dvwa\config\
   ```
2. Rename this file:
   ```
   config.inc.php.dist ➜ config.inc.php
   ```
3. Open `config.inc.php` with **Notepad**

4. Find and edit:
   ```php
   $_DVWA[ 'db_user' ] = 'root';
   $_DVWA[ 'db_password' ] = '';
   ```
   ➤ Leave password as empty string (default in XAMPP)

---

### 🌐 Step 5: Launch DVWA in Browser
- Go to:
  ```
  http://localhost/dvwa
  ```
- You'll see the **Database Setup** page
- Click on **Create / Reset Database**

✅ If successful → you'll be redirected to the login page.

---

### 🔐 Step 6: Log in to DVWA
- **Username:** `admin`
- **Password:** `password`

---

### ⚠️ Step 7: Fix Common Errors

#### 🛑 Error: `Could not connect to database`
**Fix:**
- Ensure these values in `config.inc.php`:
  ```php
  $_DVWA[ 'db_user' ] = 'root';
  $_DVWA[ 'db_password' ] = '';
  ```

#### 🛑 Error: `allow_url_include = Off`
**Fix:**
1. In **XAMPP Control Panel**, click `Config` next to Apache → `php.ini`
2. Find:
   ```
   allow_url_include = Off
   ```
   ➤ Change it to:
   ```
   allow_url_include = On
   ```
3. Save the file.
4. **Stop and Start Apache** again.

✅ Page should now say `allow_url_include = Enabled`

---

### 🧩 [Extra] Missing PHP GD Module (Fixed!)
If you see:
```
PHP module gd: Missing
```
This is needed for **CAPTCHA-based vulnerabilities**.

**Fix:**
1. Open `php.ini` (via XAMPP → Apache → Config → `php.ini`)
2. Search for:
   ```ini
   ;extension=gd
   ```
3. Remove the semicolon (`;`) to uncomment it:
   ```ini
   extension=gd
   ```
4. Save and **restart Apache**

✅ GD module will now be enabled (check in DVWA or `phpinfo()`)

---

### ✅ Final Checks Before Using DVWA
- ✔ Apache & MySQL both running in XAMPP
- ✔ `http://localhost/dvwa` loads successfully
- ✔ Default login works (`admin` / `password`)
- ✔ Config and URL include errors fixed
- ✔ GD module enabled (for captcha modules, optional)

---

### 🧠 Why Use DVWA + XAMPP?
- 🧪 Learn Burp Suite without harming real websites
- 🛡️ Practice ethical hacking in a **safe, isolated** environment
- 🔁 Reset vulnerabilities easily and learn securely

---

### 🔐 Next Steps: Start Learning Burp Suite
Now that DVWA is ready:
- Intercept and manipulate traffic using Burp
- Practice different OWASP Top 10 vulnerabilities like:
  - SQL Injection
  - XSS
  - CSRF
  - File Inclusion
  - Command Injection

---
#### **Troubleshooting Tips** 🛠️
- If DVWA doesn’t load, check that **Apache** and **MySQL** are running in XAMPP.
- If you encounter errors with the database, revisit the **config.inc.php** file to ensure all changes are correctly made.

