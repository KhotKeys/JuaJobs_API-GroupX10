# JuaJobs API - GroupX10

**Connecting skilled workers to clients across Africa — starting with Rwanda**  
*A Django REST Framework backend for the JuaJobs platform, featuring job listings, mobile payments, and offline-first design.*

---

## 👥 Team Structure & Responsibilities
| Role                      | Member               | Key Responsibilities                          |
|---------------------------|----------------------|-----------------------------------------------|
| **API Architect**         | Patrick Mukunzi      | Resource modeling, database relationships    |
| **Endpoint Designer**     | Divine Nubuhoro      | RESTful routes, query parameters             |
| **Documentation Specialist** | Gabriel Khot Garang | OpenAPI specs, usage examples                |
| **Security Designer**     | Chiedu Paul Unekwe   | OTP auth, JWT, payment security              |

---

## Project Overview

**JuaJobs** is a mobile-first platform that:
 Enables clients to post jobs and workers to apply  
 Supports mobile money payments (MTN/Airtel)  
 Uses geolocation and multilingual interfaces (`en_RW`, `fr_RW`)  
   Optimized for low-bandwidth areas with offline-sync capabilities  

---

## 🛠 Tech Stack

| Category          | Technologies                          |
|-------------------|---------------------------------------|
| **Backend**       | Django + Django REST Framework        |
| **Database**      | PostgreSQL                            |
| **Authentication**| Phone OTP + JWT                       |
| **Payments**      | MTN Mobile Money, Airtel, Bank Transfer |
| **Localization**  | Multi-language (en_RW, fr_RW), Multi-currency (RWF, KES, USD) |
| **DevOps**        | Docker-ready                          |

---

##  Documentation
🔗 [JuaJobs API Spec & ERD](https://docs.google.com/document/d/1m40c0K7Lsxi34NLKKlE6wrZxPwEzvIRiRe-1AZeOAt8/edit?usp=sharing)

Includes:

* RESTful routes (`/api/v1/`)
* OTP Auth Flow (`/auth/otp/send`, `/auth/otp/verify`)
* Job posting, applications, messaging, and payment endpoints
* Admin tools
* Escrow and mobile money integration

---

###  Full Project & Functional Documentation

🔗 [JuaJobs Full Functional and Architecture Doc](https://docs.google.com/document/d/1HmTD2_SmpRl7EwMgQIzeltMcq4oBDWom8y6-qqBRAdc/edit?tab=t.0#heading=h.9k2n33hnzlao)

Covers:

* Use-case personas (clients, workers, admin)
* API use flows
* Local-first & offline design
* Data models & relationships
* Payment workflows
* Error handling

---

### API Specifications
🔗 [OpenAPI Documentation](https://editor.swagger.io/) *(Import the YAML spec provided in `/docs/openapi.yaml`)*  
🔗 [ERD & API Flow Diagrams](https://docs.google.com/document/d/1m40c0K7Lsxi34NLKKlE6wrZxPwEzvIRiRe-1AZeOAt8/edit)


**Key Endpoints:**
```http
POST /auth/otp/send       # Request OTP
POST /auth/otp/verify     # Verify OTP → Get JWT
GET  /api/v1/jobs         # List jobs (filter by location/skill)
POST /api/v1/payments     # Initiate mobile money payment

##  Getting Started (Local Setup)

# 1. Clone repo
git clone https://github.com/YourOrg/JuaJobs_API-GroupX10.git
cd JuaJobs_API-GroupX10

# 2. Set up environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate    # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Configure environment variables
cp .env.example .env
# Edit .env with your DB and payment keys

# 5. Run migrations
python manage.py migrate

# 6. Start server
python manage.py runserver

Access Endpoints:

API Docs: http://localhost:8000/swagger/

Admin Panel: http://localhost:8000/admin/ (Create superuser with python manage.py createsuperuser)

## Authentication Flow
sequenceDiagram
    User->>+Server: POST /auth/otp/send (phone_number)
    Server->>+Redis: Store OTP (expires in 5min)
    Server->>User: SMS with OTP
    User->>Server: POST /auth/otp/verify (phone_number, otp)
    Server->>User: JWT Token (valid 24h)


Presentation Materials
   Stakeholder Pitch Deck:
[Canva Presentation](https://www.canva.com/design/DAGorIn2Jt0/gWQFmBTN-DN-6r4BPwagPA/edit)

