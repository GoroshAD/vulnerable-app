# 🔐 VulnVault

![License](https://img.shields.io/badge/license-MIT-green.svg) ![Made with Flask](https://img.shields.io/badge/Made%20with-Flask-blue.svg) ![Security Education](https://img.shields.io/badge/Purpose-Security%20Training-orange)

> 🎯 A deliberately vulnerable web app built to teach and test real-world security vulnerabilities.  
> ✅ Great for portfolios, CTFs, red team practice, and application security education.

---

## 🎨 Screenshots

<table>
  <tr>
  <td><img src="https://github.com/user-attachments/assets/095f84d6-f3c4-4adb-b69c-661c1e2c9b97" alt="Home Page" width="300"></td>
  <td><img src="https://github.com/user-attachments/assets/a1dc1921-e67e-413b-8308-26a9d8322432" alt="SQL Injection" width="300"></td>
</tr>

  <tr>
    <td align="center">Home Page</td>
    <td align="center">Login SQLi</td>
  </tr>
</table>

---

## 📦 Tech Stack

- **Backend**: Python + Flask
- **Database**: SQLite
- **Frontend**: HTML5, CSS3 (Custom styling)
- **Deployment**: Docker-ready

---

## 💣 Vulnerabilities Included

| Vulnerability | OWASP | Description |
|---------------|-------|-------------|
| 💬 XSS | A7 | User comments render unescaped HTML `c\|safe` |
| 🛑 SQL Injection | A1 | Login bypass using classic `' OR 1=1 --` |
| 🔁 CSRF | A5 | Profile update without CSRF tokens |
| 🧾 IDOR | A4 | Invoices accessible by changing `/invoice/<id>` |
| 📎 Insecure File Upload | A8 | Uploads allow arbitrary file types |
| 🧑‍💻 Broken Auth | A2 | No rate limit or session expiration |
| ⚙️ Misconfiguration | A6 | Debug mode enabled, stack traces visible |

---

## 🚀 Getting Started

### 🔧 Requirements

- Python 3.8+
- pip
- Optional: Docker

### ▶️ Run Locally

```bash
git clone https://github.com/pleontis/VulnVault-A-Deliberately-Insecure-Web-App.git
cd VulnVault-A-Deliberately-Insecure-Web-App
pip install -r requirements.txt
python run.py
````

Then open [http://localhost:5000](http://localhost:5000)

### 🐳 Docker Setup

```bash
docker build -t vulnvault .
docker run -p 5000:5000 vulnvault
```

---

## 🔍 Vulnerability Writeups

Each vulnerability has its own detailed walkthrough in the `docs/writeups/` directory.

✅ Includes:

* Exploit steps
* Real-world examples (CVEs, bug bounty reports)
* Secure code comparisons

---

## 📂 Project Structure

```
vulnvault/
├── app/
│   ├── static/         # CSS, uploads
│   ├── templates/      # HTML pages
│   ├── routes.py       # Flask routes
│   └── __init__.py
├── run.py              # Entry point
├── Dockerfile
├── requirements.txt
└── README.md
```

---

## 🌐 Live Demo

> ⚠️ For security reasons, this app is NOT recommended for public deployment as-is.

To deploy safely:

* Turn off `debug=True`
* Add authentication
* Filter user input
* Use CSRF tokens

---

## 📘 License

This project is licensed under the MIT License.
For educational use only. Do not use in production environments.

---

## 🙋‍♀️ Author

Made with 💀 by Panagiotis Leontis.

Want to collab on security tools or CTFs? Reach out!

