# 🧩 Burp Suite Target Tab – CTF Cheatsheet 🧠  
**💥 Bug Bounty | CTF | Web Exploitation Ready**

---

## 🔹 What is the Target Tab?

> It's where you track, analyze, and manage all URLs, endpoints, and requests of your target application.

---

## 🔍 Basic Workflow with Target Tab

1. **Proxy → Intercept ON → Visit target site**
2. **Target → Site Map gets auto-populated**
3. **Add scope → Tools focus only on that target**
4. **Use filters → Hide noise (images, scripts)**

---

## 🎯 Scope Configuration

- Go to `Target → Scope`
- Click "Add" ➜ Insert domain: `https://example.ctf`
- Enable **“Use suite-wide scope”**

**🔥 Tip:** Keeps Scanner, Repeater, Intruder focused only on your target — not third-party resources like Google or CDNs.

---

## 📁 Site Map Filters (Game Changer for CTF)

| Filter Option | Why Use It |
|---------------|------------|
| Only in-scope items | Hide 3rd party domains |
| Show parameterized requests | Expose vulnerable inputs |
| MIME type = HTML / JSON | Filter out noise |
| Status code = 403 / 401 / 500 | Privileged or broken access |
| Sort by length | Spot large pages (e.g., admin panels, backups) |

---

## 🧪 CTF Attack Techniques Using Target Tab

### 1. **Find Hidden Endpoints**
- Use: `Status Code Filter → 403/401/500`
- Check for: `/admin`, `/debug`, `/panel`, `/old`, `/.env`, `/backup.zip`

### 2. **Discover Input Points**
- Right-click → "Send to Repeater"
- Use **Inspector** to:
  - View & modify parameters
  - See headers/cookies easily
  - Detect base64/encoded tokens

### 3. **Try Auth Bypass**
Headers to test in Repeater:
```http
X-Forwarded-For: 127.0.0.1
Referer: internal
User-Agent: curl/7.64.1
X-Auth: internal
Authorization: Bearer null
```

### 4. **Reveal Sensitive Files**
Sort by extension:
- `.zip`, `.bak`, `.old`, `.tar.gz`, `.env`, `.sql`
- Download & unzip ➜ Look for hardcoded credentials or flags

---

## 🔐 Auth & Role Escalation CTF Tricks

| Trick | What it Does |
|-------|---------------|
| Spoof IP headers | Bypass IP restrictions |
| Replay tokens | Reuse session/cookie from low user |
| Try HTTP verb tampering | Switch GET ↔ POST ↔ HEAD |
| Use broken Referer check | Add Referer: /admin |

---

## 🏁 CTF Checkpoints

✅ Passive crawling complete  
✅ Scope is defined  
✅ Filters applied  
✅ Parameterized URLs found  
✅ Suspicious paths identified (403/401)  
✅ Manual testing in Repeater  
✅ Inspector used for decoding, token analysis  
✅ Hidden file access attempted  
✅ Headers tampered for bypass  

---

## 📚 Quick Commands Summary

```bash
# Add scope manually
Target → Scope → Add → https://target.ctf

# Filter only parameterized endpoints
Target → Site Map → Filter → Only Parameterized

# Sort by status code
Sort → 401, 403, 500

# Send request to Repeater
Right-click → Send to Repeater

# View and edit parameters easily
Use Inspector Tab (below request/response)
```

---

## 🧠 Must-Try Practice Scenarios

| Challenge | Tools |
|----------|-------|
| Find `/admin` protected by IP filter | Repeater + spoof headers |
| Detect hidden `.env` or `.git/config` | Site Map + length filter |
| Decode base64 `Set-Cookie` | Inspector or Decoder |
| Replay tokens from normal user to admin path | Site Map + Repeater |

---

## 🛑 Bonus: When NOT to Use Scanner

In CTFs, scanners can:
- Waste time
- Get you rate-limited
- Miss logic flaws

✅ Use **Target + Manual Repeater + Inspector** = Best for CTFs

---

## 🏆 Flag Example (from CTF Guide Above)

```
Endpoint: /admin-panel
Method: GET
Header added: X-Forwarded-For: 127.0.0.1
Flag: FLAG{b0nus_admin_bypass_ctf}
```

---

