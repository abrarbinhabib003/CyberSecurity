
### **Interactive Encoding Techniques Tutorial**

By the end of this activity, you'll gain **practical experience** encoding data to protect your web application from injection attacks. Here, we'll practice encoding techniques like **HTML encoding**, **JavaScript encoding**, and **URL encoding**.

---

### **1. HTML Encoding**
HTML encoding transforms **potentially harmful** characters into **safe equivalents** to ensure they are treated as text, not as code.

#### **Interactive Exercise**
Type any HTML code or script below (such as `<script>alert("Hacked!");</script>`) and see how it’s encoded.

**Input your HTML code:**

```html
<script>alert('Hacked!');</script>
```

Now, **Click on the "Encode" button** below to see how it gets converted to a safe version!

[Encode HTML Code]

---

#### **Expected Result:**
If you typed:
```html
<script>alert('Hacked!');</script>
```

It should convert to:

```html
&lt;script&gt;alert('Hacked!');&lt;/script&gt;
```

This ensures that **malicious code** is displayed as text, **not executed**.

---

### **2. JavaScript Encoding**
JavaScript encoding helps prevent **injection of harmful scripts** that could be executed in your application.

#### **Interactive Exercise**
Type a **dangerous** JavaScript string that contains dangerous characters like `;` or `"` and see how it’s encoded.

**Input your JavaScript code:**

```javascript
"; alert('Hacked!'); //
```

**Click on the "Encode" button** to see how it changes!

[Encode JavaScript Code]

---

#### **Expected Result:**
The input will change to:

```javascript
&quot;; alert('Hacked!'); // 
```

This encoding prevents it from **breaking** your JavaScript code, rendering it **harmless**.

---

### **3. URL Encoding**
URL encoding converts **special characters** in URLs to their safe equivalents so URLs are properly formatted and don't break.

#### **Interactive Exercise**
Type a URL containing **spaces** or **special characters** (e.g., `hello world!`) and see how it’s encoded.

**Input your URL:**

```plaintext
example.com/search?query=hello world!
```

**Click on the "Encode" button** to convert it to a safe URL!

[Encode URL]

---

#### **Expected Result:**
The input should transform to:

```plaintext
example.com/search?query=hello%20world%21
```

This ensures that the URL is **valid** and **safe** to use, even if it contains spaces or special characters.

---

### **Summary of Results**
- **HTML Encoding** turns `<` into `&lt;` and `>` into `&gt;`, ensuring any scripts are displayed as text.
- **JavaScript Encoding** converts dangerous characters like `"` into `&quot;`, stopping potential script injections.
- **URL Encoding** changes spaces into `%20` and special symbols like `!` into `%21`, making the URL safe for use.

---

### **Why Encoding Is Crucial**

1. **Protection Against Malicious Scripts**: Without encoding, attackers could inject harmful code into your web application.
2. **Preventing Broken URLs**: Special characters could break the functionality of your URLs and cause errors.
3. **Safe Display of Content**: User-generated content can be safely displayed on the web without causing security vulnerabilities.

---

### **Interactive Quiz:**
Let's test your knowledge! Answer the following questions.

1. **What happens if a user enters `<script>alert('Hacked!');</script>` without HTML encoding?**
   - [ ] The browser will show an alert pop-up.
   - [ ] The text will be displayed as plain text.
   - [ ] It will be ignored.

2. **What does JavaScript encoding do with the character `"` in a user input?**
   - [ ] It ignores the character.
   - [ ] It converts it into `&quot;`.
   - [ ] It executes the script.

3. **If a URL contains spaces, what does URL encoding change the space character into?**
   - [ ] `%20`.
   - [ ] `%space`.
   - [ ] `_`.

---

### **Results and Feedback**
- **1st Question Answer**: The correct answer is **"The browser will show an alert pop-up."** This is the risk of not encoding HTML input, allowing harmful scripts to run.
- **2nd Question Answer**: The correct answer is **"It converts it into &quot;"** to prevent breaking your JavaScript and stop injection.
- **3rd Question Answer**: The correct answer is **"%20"**. This ensures the URL is properly interpreted by browsers and servers.

---

**Well Done!** You've now mastered encoding techniques that protect your web applications from **injection attacks**. Remember to apply **HTML**, **JavaScript**, and **URL encoding** when handling user input!

---

# 💻 **Interactive Note: Implementing Encoding Techniques in Code** 🛡️

### 🔐 **Why Encoding Matters**
When handling user input in web applications, improper processing can lead to security vulnerabilities. One common attack is **Cross-Site Scripting (XSS)**, where malicious scripts can be injected into your web pages, compromising the integrity of your application. **Encoding** is a critical defense mechanism that transforms dangerous input into harmless text, ensuring that malicious code is not executed.

### 🏗️ **Building the Project: Encoding User Input**
We’ll build a small web project that **encodes user input** before displaying it on a webpage to prevent XSS attacks.

#### 1. **Set Up the Project Environment** 📂
- Create a new project folder and name it.
- Open the folder in Visual Studio Code.
- Create a new file named `index.html`.

#### 2. **HTML Structure** 📝
In the `index.html` file, write the basic HTML structure using a shortcut (`!` + Enter). This template will set up:
- **Document type** declaration
- **Character encoding**
- **Title** for the page

#### 3. **Building the Form** 🖊️
Now, let’s create the **HTML form** where the user can input text:
- Use `<h1>` for the main title and `<p>` for a subtitle.
- Display **special characters** like `<` and `>` as `&lt;` and `&gt;` to encode them safely.
- Add an **input field** (`<input type="text">`) where the user can type their input.
  - Use the `id="userInput"` to access it later in JavaScript.
  - Add a **placeholder** with the text “Enter text.”
- Add a **submit button** with `onClick="handleInput()"` to trigger the JavaScript function.
- Create a **div for output** where the encoded text will be displayed (`id="output"`).

#### 4. **JavaScript Encoding Logic** 🔧
At the bottom of the HTML body, we will:
- Write the **`handleInput` function**.
- **Retrieve the user input** using `document.getElementById('userInput').value`.
- Create a **temporary div** using `document.createElement('div')` to safely encode the input:
  - Set `tempDiv.textContent = input` to ensure characters like `<` and `>` are encoded.
- Update the **output div** with the safely encoded text: 
  ```js
  output.textContent = tempDiv.textContent;
  ```

#### 5. **Testing the Application** 🧪
- Save the file and open it in your browser.
- Test by typing something like `<script>alert('XSS')</script>` and clicking the submit button.
  - **Expected result:** Instead of running the script, it will show as plain text in the output area, because the encoding process converts the script into harmless characters.

### 📜 **Step-by-Step Code Example**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Input Encoding Example</title>
</head>
<body>
    <h1>Safe Encoding Demo</h1>
    <p>Enter text, and we will safely encode it!</p>
    <input type="text" id="userInput" placeholder="Enter text">
    <button onClick="handleInput()">Submit</button>
    <div id="output" style="font-family: monospace; white-space: pre-wrap;"></div>

    <script>
        function handleInput() {
            // Get the input value
            let input = document.getElementById('userInput').value;
            
            // Create a temporary div to encode the input safely
            let tempDiv = document.createElement('div');
            tempDiv.textContent = input;
            
            // Display the encoded text in the output div
            document.getElementById('output').textContent = tempDiv.textContent;
        }
    </script>
</body>
</html>
```

### 🛡️ **Security Benefits of Encoding**
Encoding helps ensure that:
- **User input is displayed as text**, not executed as code.
- Potentially malicious input, such as `<script>`, is **neutralized** and treated as plain text.
- Your web application remains **secure** against **XSS attacks** and other malicious injections.

### 🔍 **Why This Works**
When the input is encoded using `textContent`, **special characters** (like `<` and `>`) are converted into their safe HTML entities:
- `<` becomes `&lt;`
- `>` becomes `&gt;`
- This prevents the browser from interpreting potentially harmful content as HTML or JavaScript.

### 🚀 **Conclusion**
By implementing encoding techniques, you're not only improving the **security** of your web applications but also learning essential web development best practices. With this knowledge, you can prevent dangerous vulnerabilities like **XSS** and ensure a safer user experience.

---

# 🛡️ **Interactive Note: Sanitization Practices** 🧹

### 💡 **What is Sanitization?**
Sanitization is the process of **cleaning** user inputs in web applications to remove potentially dangerous content. This is vital for **preventing attacks**, such as **Cross-Site Scripting (XSS)**, where attackers inject malicious scripts into web pages, compromising the security of both the users and the application.

### 🔍 **Why is Sanitization Important?**
Without proper sanitization, user inputs could contain harmful HTML tags or scripts that, when executed, can lead to:
- **XSS attacks** (malicious scripts that run on the user's browser).
- **Malicious redirections** or **phishing attacks**.
- **Data theft** or loss.

Sanitization ensures that the input remains **safe** by removing harmful content like script tags, links, or unsafe styles.

### 🧼 **How Does Sanitization Work?**
Sanitization works by removing or neutralizing harmful tags and content within the user input. It ensures that:
- Only **safe content** is allowed (e.g., bold or italic text tags).
- **Unsafe content** like `<script>` or `<style>` tags is **stripped** away.

#### Example:
- **Unsafe Input**: `<script>alert('XSS Attack');</script>`
- **Sanitized Output**: `&lt;script&gt;alert('XSS Attack');&lt;/script&gt;`

This prevents the script from executing and ensures the input is rendered as plain text.

### 🛠️ **Tools for Sanitization: DOM Purify**
Manually checking and sanitizing every piece of user input is time-consuming and error-prone. **DOM Purify** is an **open-source JavaScript library** that automates the sanitization process. It scans user inputs, removes dangerous content, and ensures that only safe HTML, CSS, and JavaScript content is allowed.

#### **DOM Purify Use Case**:
- **Input**: User submits a comment on a blog post.
- **Malicious Input**: `<script>alert('Redirecting to malicious website'); window.location='http://evil.com';</script>`
- **Sanitized Output**: The `<script>` tag is removed, and only the text of the comment is displayed, protecting users from malicious actions.

### 📝 **Context-Specific Sanitization**
Sanitization rules vary depending on the context in which user input is used:
- **HTML**: Only safe HTML tags (like `<b>`, `<i>`, and `<p>`) are allowed. Tags like `<script>` are removed to prevent code execution.
- **CSS**: Malicious styles (such as those that load harmful content in the background) are neutralized. Only safe CSS properties are permitted.
- **JavaScript**: Inputs used in dynamic JavaScript features (like search bars or interactive elements) must be sanitized to prevent code execution.

By applying sanitization in these different contexts, developers can **protect** all parts of a web application.

### 🛡️ **Sanitization in Action**
Imagine a **review form** on an e-commerce site where users can leave comments about products. A malicious user might submit a comment with a `<script>` tag that redirects users to a harmful site. Sanitization removes the `<script>` tag, ensuring that the input is displayed safely as plain text.

#### Example:
- **Unsafe User Input**: `<script>window.location='http://malicious-site.com';</script>`
- **Sanitized Output**: `window.location='http://malicious-site.com';` (as plain text)

### 🔒 **How to Apply Sanitization?**

You can use libraries like **DOM Purify** to automate the sanitization process in your web applications.

#### Example using DOM Purify:
```html
<script src="https://cdn.jsdelivr.net/npm/dompurify@2.0.16/dist/purify.min.js"></script>
<script>
    let unsafeInput = "<script>alert('XSS Attack');</script>";
    let safeInput = DOMPurify.sanitize(unsafeInput);
    console.log(safeInput); // This will print a sanitized version without the script tag
</script>
```

### 🚀 **Benefits of Proper Sanitization**
- **Security**: It **prevents XSS attacks** and ensures that malicious content does not get executed.
- **Consistency**: Automates the sanitization process, ensuring that every input is cleaned in a uniform manner.
- **Trust**: By safeguarding user input, you build trust with your users, knowing their data and experience are protected.

### 🧠 **Takeaways**
1. **Sanitization** is crucial for web security and prevents harmful user inputs from compromising your application.
2. Use **tools like DOM Purify** to easily automate the sanitization process.
3. Ensure sanitization is applied to inputs in **HTML**, **CSS**, and **JavaScript** contexts.
4. Always **sanitize user input** before using it in your web application to avoid XSS and other types of attacks.

---

# 🔒 **Interactive Note: Encoding and Sanitization in Web Applications** 🧼

### 💡 **Overview**
In this lab, we learned how to **implement encoding and sanitization techniques** to prevent **Cross-Site Scripting (XSS)** attacks in a web application. These techniques help to **protect** user input and ensure that potentially dangerous content is either neutralized or handled safely.

### 🧑‍💻 **Step 1: HTML Encoding**
- **What is HTML Encoding?**
  HTML encoding ensures that any **HTML tags** entered by a user are treated as **plain text** rather than executable HTML. This helps to prevent malicious scripts from being executed on the page.

- **How to Implement HTML Encoding:**
  In this example, we grab the user input from an input field and place it into a **temporary `div`** element in memory. By setting the `textContent` property of this `div`, we ensure that any HTML in the input is encoded as plain text. Here's how the code works:
  ```javascript
  let input = document.getElementById('userInput').value;
  let tempDiv = document.createElement('div');
  tempDiv.textContent = input; // HTML encoding happens here
  document.getElementById('output').textContent = tempDiv.textContent; // Output the encoded text
  ```
  By using `textContent`, any HTML tags are safely encoded and displayed as plain text, rather than executed as HTML.

### 🛠️ **Step 2: JavaScript Encoding with Regex**
- **What is JavaScript Encoding?**
  JavaScript encoding involves escaping characters that could potentially execute JavaScript code, such as `<`, `>`, and `&`. By replacing these characters, we prevent any scripts from running in the user’s browser.

- **How to Implement JavaScript Encoding:**
  This is achieved by using a **regular expression (Regex)** to replace characters that may pose a security risk:
  ```javascript
  let safeInput = input.replace(/</g, '&lt;').replace(/>/g, '&gt;').replace(/&/g, '&amp;');
  document.getElementById('output').textContent = safeInput;
  ```
  This ensures that any potentially dangerous characters are escaped and displayed as text, not as executable code.

### 🌐 **Step 3: URL Encoding**
- **What is URL Encoding?**
  URL encoding ensures that any URLs submitted by users are **encoded properly** so that special characters (like `?`, `&`, `=`, etc.) are safely handled.

- **How to Implement URL Encoding:**
  The **`encodeURIComponent()`** function is used to encode user input that may contain URL components, ensuring special characters are safely represented:
  ```javascript
  let encodedURL = encodeURIComponent(input);
  console.log(encodedURL); // Output the safely encoded URL
  ```

  This prevents harmful URLs from being injected and executed.

### 🧹 **Step 4: Input Sanitization with DOMPurify**
- **What is DOMPurify?**
  DOMPurify is an open-source library that automates input sanitization. It **cleans** any user input to remove dangerous elements like `<script>` tags, ensuring that only safe content is allowed.

- **How to Implement Sanitization with DOMPurify:**
  By including the DOMPurify library, we can sanitize input with a simple function call:
  ```javascript
  let sanitizedInput = DOMPurify.sanitize(input);
  console.log(sanitizedInput); // Output the sanitized input
  ```

  DOMPurify automatically **removes unsafe elements** from user input, making it easier to ensure that input is safe without manually encoding or escaping every potentially harmful character.

### 🧑‍💻 **Putting It All Together**
In a **real-world application**, you would typically combine all these methods to ensure comprehensive input protection. Here’s a summary of the steps:
1. **HTML Encoding**: Ensures HTML tags are rendered as plain text.
2. **JavaScript Encoding**: Escapes characters to prevent script execution.
3. **URL Encoding**: Safely encodes URL components.
4. **Sanitization**: Cleans up input to remove harmful content using DOMPurify.

### 🚀 **Benefits of Encoding and Sanitization**
1. **Prevents XSS attacks** by ensuring harmful scripts do not execute.
2. **Protects your users** from malicious content injected into forms or URLs.
3. **Reduces security risks** in web applications, providing a safer user experience.

### ⚙️ **Conclusion**
By applying these techniques — HTML encoding, JavaScript encoding, URL encoding, and input sanitization — you can significantly enhance the security of your web application. These methods work together to neutralize potentially dangerous user input and keep your site safe from XSS and other attacks.

---

# 🔒 **Interactive Note: Preventing XSS Attacks with Encoding and Sanitization** 🧼

### 💡 **Overview**
In this lab, you will implement several **security techniques** to protect your web application from **Cross-Site Scripting (XSS)** and **injection attacks**. The steps involve:
- **HTML encoding**: Ensures special characters are rendered as plain text.
- **JavaScript encoding**: Escapes characters to neutralize potentially dangerous input.
- **URL encoding**: Safely encodes special characters in URLs.
- **Input sanitization**: Removes unsafe elements from user input.

### 🧑‍💻 **Part 1: HTML Encoding to Prevent XSS Attacks**
- **Objective**: Ensure that special characters like `<`, `>`, and `"` are displayed as plain text instead of being interpreted as HTML.

#### **Instructions:**
1. **Create the HTML Structure** in `index.html`:
   ```html
   <input type="text" id="userInput" placeholder="Enter some text">
   <button id="submitBtn">Submit</button>
   <div id="output"></div>
   ```
2. **Implement the Encoding Function** in `script.js`:
   ```javascript
   document.getElementById('submitBtn').addEventListener('click', function() {
     let userInput = document.getElementById('userInput').value;
     let tempDiv = document.createElement('div');
     tempDiv.textContent = userInput; // Encode input
     document.getElementById('output').textContent = tempDiv.textContent; // Display safely
   });
   ```

#### **Test the Encoding**:
- Enter `<script>alert('Hacked!')</script>` into the input field.
- You should see the script tags displayed as plain text, not executed as a script.

---

### 🛠️ **Part 2: JavaScript Encoding to Prevent Malicious Input**
- **Objective**: Encode quotes and escape characters to neutralize potential JavaScript-based attacks.

#### **Instructions:**
1. **Modify the JavaScript function** in `script.js` to escape characters that could be used in a malicious script:
   ```javascript
   document.getElementById('submitBtn').addEventListener('click', function() {
     let userInput = document.getElementById('userInput').value;
     let safeInput = userInput.replace(/</g, '&lt;').replace(/>/g, '&gt;').replace(/"/g, '&quot;').replace(/'/g, '&#39;');
     document.getElementById('output').textContent = safeInput; // Display safely
   });
   ```

#### **Test the JavaScript Encoding**:
- Enter `"; alert('XSS'); //` into the input field.
- The output should be displayed as text, not executed as a script.

---

### 🌐 **Part 3: URL Encoding to Prevent Injection Attacks**
- **Objective**: Ensure that special characters in URLs are safely encoded to prevent injection attacks.

#### **Instructions:**
1. **Modify the HTML** to include an input field for URLs:
   ```html
   <input type="text" id="urlInput" placeholder="Enter a URL">
   <button id="submitUrlBtn">Submit URL</button>
   <div id="urlOutput"></div>
   ```

2. **Implement URL Encoding** in `script.js`:
   ```javascript
   document.getElementById('submitUrlBtn').addEventListener('click', function() {
     let urlInput = document.getElementById('urlInput').value;
     let encodedURL = encodeURIComponent(urlInput); // URL encode input
     document.getElementById('urlOutput').textContent = encodedURL; // Display encoded URL
   });
   ```

#### **Test the URL Encoding**:
- Enter `https://example.com/?query=<script>alert('XSS')</script>` into the URL input field.
- The URL should be safely encoded, and the `<script>` tags should not be executed.

---

### 🧹 **Part 4: Input Sanitization with DOMPurify**
- **Objective**: Use **DOMPurify** to sanitize user input and remove dangerous HTML and JavaScript elements.

#### **Instructions:**
1. **Include the DOMPurify library** in the HTML:
   ```html
   <script src="https://cdn.jsdelivr.net/npm/dompurify@2.0.17/dist/purify.min.js"></script>
   ```

2. **Modify the JavaScript function** in `script.js` to sanitize input before displaying it:
   ```javascript
   document.getElementById('submitBtn').addEventListener('click', function() {
     let userInput = document.getElementById('userInput').value;
     let sanitizedInput = DOMPurify.sanitize(userInput); // Sanitize input
     document.getElementById('output').textContent = sanitizedInput; // Display sanitized input
   });
   ```

#### **Test the Sanitization**:
- Enter `<script>alert('XSS')</script>` into the input field.
- The `<script>` tag should be **removed** from the input, and the alert should not execute.

---

### 🔒 **Part 5: Combining Encoding and Sanitization for Robust Security**
- **Objective**: Combine **sanitization** (with DOMPurify) and **encoding** (with textContent) to ensure safe input handling.

#### **Instructions:**
1. **Modify the JavaScript function** to first **sanitize** the input with **DOMPurify**, then **encode** it using `textContent`:
   ```javascript
   document.getElementById('submitBtn').addEventListener('click', function() {
     let userInput = document.getElementById('userInput').value;
     let sanitizedInput = DOMPurify.sanitize(userInput); // Sanitize input
     let tempDiv = document.createElement('div');
     tempDiv.textContent = sanitizedInput; // Encode sanitized input
     document.getElementById('output').textContent = tempDiv.textContent; // Display safely
   });
   ```

#### **Test the Combined Implementation**:
- Enter `<img src=x onerror=alert(1)>` into the input field.
- The `<img>` tag should be **sanitized** (the script removed), and it should be **encoded** (displayed as harmless text).

---

### 🛡️ **Conclusion**
By combining **HTML encoding**, **JavaScript encoding**, **URL encoding**, and **input sanitization**, you ensure that user input is processed securely and that malicious content is neutralized before it can do any harm. This provides robust protection against **XSS attacks**, **script injections**, and other types of web vulnerabilities.

---

# 🔒 **Encoding and Sanitization Cheat Sheet** 🧼

### **Introduction**
Web applications often handle user input that can be exploited for injection attacks, such as **Cross-Site Scripting (XSS)**, if not properly sanitized or encoded. Encoding and sanitization are essential techniques to neutralize harmful content and ensure that malicious input does not execute as code. This guide outlines practical examples of **HTML encoding**, **JavaScript encoding**, **URL encoding**, and **input sanitization** using **DOMPurify** to enhance application security.

---

### 1. **HTML Encoding** 🔠
**Use Case**: Converts special characters into safe HTML entities to prevent them from being interpreted as code.

#### **Example**:
```html
<p>Example: &lt;script&gt;alert('XSS')&lt;/script&gt;</p>
```

#### **Implementation in JavaScript**:
```javascript
function encodeHTML(input) {
    const tempDiv = document.createElement('div');
    tempDiv.textContent = input;
    return tempDiv.innerHTML;
}

const userInput = "<script>alert('XSS')<\/script>";
console.log(encodeHTML(userInput)); 
// Outputs: &lt;script&gt;alert('XSS')&lt;/script&gt;
```

**Explanation**: This encoding ensures that special characters, like `<`, `>`, and `"`, are displayed as plain text, preventing them from being executed as HTML or JavaScript code.

---

### 2. **JavaScript Encoding** 🖥️
**Use Case**: Escapes unsafe characters in JavaScript to prevent code injection and ensure safe string handling.

#### **Example**:
```javascript
function encodeForJS(input) {
    return input.replace(/["'\\]/g, '\\$&');
}

const userInput = 'Hello "world" \\ test';
console.log(encodeForJS(userInput)); 
// Outputs: Hello \"world\" \\ test
```

**Explanation**: This encoding escapes special characters like quotes (`"` and `'`) and backslashes (`\\`) in JavaScript strings, ensuring they don’t break or alter code execution.

---

### 3. **URL Encoding** 🌐
**Use Case**: Ensures that URLs are properly formatted, preventing manipulation or injection attacks through URL parameters.

#### **Example**:
```javascript
const unsafeURL = "https://example.com/search?query=hello world";
const safeURL = encodeURIComponent(unsafeURL);
console.log(safeURL);
// Outputs: https%3A%2F%2Fexample.com%2Fsearch%3Fquery%3Dhello%20world
```

**Explanation**: `encodeURIComponent()` ensures that special characters in a URL, such as spaces or `<` and `>`, are encoded into a safe format, preventing URL manipulation and injection.

---

### 4. **Sanitization with DOMPurify** 🧹
**Use Case**: Cleans user input by removing or neutralizing potentially harmful content while preserving safe HTML.

#### **Example**:
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/dompurify/2.3.6/purify.min.js"></script>
<script>
    function sanitizeInput(input) {
        return DOMPurify.sanitize(input);
    }

    const unsafeInput = "<script>alert('XSS')<\/script><b>Bold Text</b>";
    console.log(sanitizeInput(unsafeInput)); 
    // Outputs: <b>Bold Text</b>
</script>
```

**Explanation**: **DOMPurify** removes harmful tags (like `<script>`) while preserving safe HTML elements (like `<b>`), ensuring that the content is safe for display.

---

### **Conclusion** 🛡️
Implementing encoding and sanitization techniques effectively helps protect web applications from **XSS attacks** and **injection vulnerabilities**. The following practices should be part of every secure web application:

- **HTML Encoding**: Prevents execution of user input by converting special characters into HTML entities.
- **JavaScript Encoding**: Escapes unsafe characters to prevent code injection within JavaScript strings.
- **URL Encoding**: Safely encodes URL parameters to prevent manipulation and attacks through URLs.
- **Sanitization with DOMPurify**: Removes unsafe content while allowing safe HTML, mitigating the risk of malicious code execution.

By consistently applying these techniques, you will greatly improve the security of your web applications and protect user data.

---

**Tips**:
- Always sanitize and encode user input **before** displaying it on the page.
- Use libraries like **DOMPurify** for effective and reliable sanitization.
- Regularly test your application with malicious input to ensure encoding and sanitization are working as expected.

Stay safe and secure your applications! 😊
---