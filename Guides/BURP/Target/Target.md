# 🥅 **How to Use the Target Tab in Burp Su
💡 *A central hub for identifying, organizing, and analyzing your testing targets in Burp Suite.*

---

## 🎯 **What is the Target Tab?**

The **Target tab** in Burp Suite is your **command center** for monitoring and analyzing web applications you’re testing.

It helps you:
- 📍Identify potential targets
- 🌐 Map the structure of visited websites
- 🧭 Define what’s “in scope” (the parts you want to focus on)
- 🪲 Manage known issue definitions (in Pro version)

---

## 🧩 **Sections of the Target Tab**

The **Target Tab** has **three main parts**:

| Section | Description |
|--------|-------------|
| 🗺️ **Site Map** | Tree view of all domains and files you've visited |
| 🧾 **Scope** | Define which hosts/URLs to test or ignore |
| ❗ **Issue Definitions** (Pro) | Customize vulnerability types Burp can identify |

---

## 🌐 **Example Walkthrough: Exploring a Website in Site Map**

Let’s walk through a basic use-case. Imagine you're testing a demo website:  
🔗 `http://demo.testfire.net`

### 1. 🔄 Open with Burp’s Embedded Browser

- Go to `Proxy` tab → Open browser
- Visit `http://demo.testfire.net`

💥 You’ll now see this domain show up under `Target → Site Map`.

---

### 2. 🏗️ Understand the Tree Structure

- On the left, you’ll see the **site structure**: directories, pages, assets (like `/login.jsp`, `/about.jsp`, `/admin/`, etc.)
- On the right, you’ll see:
  - 🔄 Requests made to these pages
  - 📩 Server responses (HTML, JSON, etc.)

#### 📌 Example:
If you visit `/login.jsp`, the right pane may show:

```
POST /login.jsp HTTP/1.1
Host: demo.testfire.net
Content-Type: application/x-www-form-urlencoded

username=admin&password=admin123
```

---

## 🛠️ **Live Passive Crawl From Proxy**

To populate the Site Map, Burp uses a background task:
- 🟢 `Live passive crawl from proxy` → captures traffic from browser
- 🔴 If turned off, **no new sites** will be recorded!

🧪 **Test Example**:
1. Turn it OFF
2. Visit `https://google.com` → Nothing appears in the Target tab
3. Turn it ON again → Now visit `https://google.com` again → It appears!

---

## 🔍 **Inspector Panel**

Click on a request → Open `Inspector`

- 📊 Shows a summarized view (headers, cookies, query params)
- 🔍 Helps analyze big requests easily
- 🔄 Works similarly to “Network” tab in Developer Tools of Firefox/Chrome

> 🔎 Use this when requests are large or complex — especially for API testing!

---

## 🧰 **Viewing Requests & Responses**

👁️ Burp gives you different view styles:

- 📑 Default split (side-by-side or stacked)
- 🪞 Customize based on comfort
- 🧪 Example:
  - Request → `GET /index.jsp`
  - Response → HTML content of homepage

---

## 🖱️ **Right-Click Options on Targets**

Right-clicking a URL or folder in Site Map offers:

- 🚀 Send to Scanner (Pro version)
- 🔁 Repeat requests
- 📤 Send to Intruder, Repeater, Comparer, etc.
- 🎯 Add to Scope

---

## 🔄 **Filters in Target Tab**

Click **filter icon** above Site Map.

### ✅ Use Case Filters:

| Filter Type | Purpose | Example |
|------------|---------|---------|
| 🎯 In-Scope Only | Show only URLs marked as in-scope | `/secure/*` endpoints only |
| 🧾 Parameterized Requests | Find dynamic/API endpoints | `POST /submit-form` |
| 🧪 MIME Type | Filter files like JS, CSS, JSON | Only show `.js` |
| 📡 Status Codes | Show specific server response types | Show only `404`, `403` |

---

### 📚 **Status Codes Breakdown**  
| Code | Meaning | Use Case |
|------|---------|----------|
| `200` | OK | Success response |
| `301` | Moved Permanently | Redirection |
| `403` | Forbidden | Access blocked |
| `404` | Not Found | Broken link |
| `500` | Server Error | Vulnerability indicator! |

---

## 🧠 Real-Life Analogy

> Imagine Burp Suite as a **digital detective** 🕵️‍♂️.  
> The Target tab is your **investigation board** 📋 — showing every place you’ve visited and what you found there.

---

## 💼 Interview Questions

1. **What is the purpose of the Target tab in Burp Suite?**
   > It shows all the websites visited and helps define the attack scope.

2. **What’s the use of ‘scope’ in Target tab?**
   > It restricts tools like Scanner, Repeater, etc., to selected URLs only.

3. **How does Burp Suite populate the Site Map?**
   > Through manual browsing or passive crawling from the proxy.

4. **How would you filter only interactive endpoints?**
   > Use filter ➜ enable `Show only parameterized requests`.

5. **What is the Inspector and when would you use it?**
   > Inspector summarizes request data for large or complex traffic, useful during API testing.

---

## ✅ Summary Cheatsheet

| Feature | Use |
|--------|-----|
| Site Map | Full view of visited URLs |
| Scope | Define testing boundaries |
| Inspector | Summarized request details |
| Filters | Narrow down targets (status, type, scope) |
| Request/Response Viewer | Review and analyze traffic |
| Right-Click Actions | Send to other Burp tools |

---

## 🧪 Mini Task for Practice

1. Open Burp ➜ Proxy ➜ Browser
2. Visit `http://demo.testfire.net`
3. Go to Target ➜ Site Map
4. Right-click `/login.jsp` ➜ Send to Repeater
5. Play with filters ➜ Show only parameterized requests
6. Explore Inspector tab for `/login.jsp`

---

