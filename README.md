# 🛠️ JuaJobs\_API-GroupX10

**Connecting skilled workers to clients across Africa — starting with Rwanda.**
A RESTful API backend for the JuaJobs platform designed to support job listings, secure payments, skill-based matchmaking, and localized offline-first experiences.

---

## 🌍 Project Description

**JuaJobs** is a mobile-first, inclusive platform that enables clients to post jobs and workers to apply for them. It leverages mobile money integrations, geolocation filters, multilingual support, and an offline-sync design — ideal for users in low-bandwidth environments.

---

## 🚀 Tech Stack

* **Backend Framework**: Django + Django REST Framework
* **Database**: PostgreSQL
* **Auth**: OTP via phone number
* **Payments**: Mobile Money (MTN & Airtel), Bank Transfer
* **Localization**: `en_RW`, `fr_RW`, multi-currency (RWF, KES, USD)
* **Versioning**: `v1`
* **Hosting**: Local development + Docker-ready

---

## 📚 Documentation

### 📄 API Documentation (OpenAPI Structure)

🔗 [JuaJobs API Spec & ERD](https://docs.google.com/document/d/1m40c0K7Lsxi34NLKKlE6wrZxPwEzvIRiRe-1AZeOAt8/edit?usp=sharing)

Includes:

* RESTful routes (`/api/v1/`)
* OTP Auth Flow (`/auth/otp/send`, `/auth/otp/verify`)
* Job posting, applications, messaging, and payment endpoints
* Admin tools
* Escrow and mobile money integration

---

### 🗂️ Full Project & Functional Documentation

🔗 [JuaJobs Full Functional and Architecture Doc](https://docs.google.com/document/d/1HmTD2_SmpRl7EwMgQIzeltMcq4oBDWom8y6-qqBRAdc/edit?tab=t.0#heading=h.9k2n33hnzlao)

Covers:

* Use-case personas (clients, workers, admin)
* API use flows
* Local-first & offline design
* Data models & relationships
* Payment workflows
* Error handling

---

## 🧪 Getting Started (Local Setup)

1. **Clone the repository**

   ```bash
   git clone https://github.com/YourOrg/JuaJobs_API-GroupX10.git
   cd JuaJobs_API-GroupX10
   ```

2. **Set up virtual environment**

   ```bash
   python3 -m venv env
   source env/bin/activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run migrations & start server**

   ```bash
   python manage.py migrate
   python manage.py runserver
   ```

5. **Access development server**

   * API: `http://127.0.0.1:8000/api/jobs/`
   * Jobs: `http://127.0.0.1:8000/jobs/`
   * Sign up/ Sign In: `http://127.0.0.1:8000/login/`
   * Admin Panel: `http://127.0.0.1:8000/admin/`

---

## 🔐 Authentication Flow

* **Step 1**: User sends phone number to `/auth/otp/send`
* **Step 2**: User receives OTP and submits it to `/auth/otp/verify`
* **Step 3**: Server returns JWT Token for authenticated access

---

## 📊 Presentation

🎤 **Stakeholder & Team Presentation Slides**
📎 [*Coming Soon – View Canva/Google Slides Here*](https://www.canva.com/design/DAGorIn2Jt0/gWQFmBTN-DN-6r4BPwagPA/edit)

*(You’ll update this with the final link when the presentation deck is ready.)*

---

## 🧾 License

MIT License
© 2025 JuaJobs\_API-GroupX10

---

## 🤝 Contributing

We welcome pull requests and ideas for expansion!
Please read `CONTRIBUTING.md` before getting started.
