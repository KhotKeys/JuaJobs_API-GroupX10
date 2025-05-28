# JuaJobs API - GroupX10

**Connecting skilled workers to clients across Africa — starting with Rwanda**  
*A Django REST Framework backend for the JuaJobs platform, featuring job listings, mobile payments, and offline-first design.*

---

## 👥 Team Structure & Responsibilities

| Role                      | Member               | Key Responsibilities                          |
|---------------------------|----------------------|-----------------------------------------------|
| **API Architect**         | Patrick Mukunzi      | Resource modeling, database relationships     |
| **Endpoint Designer**     | Divine Nubuhoro      | RESTful routes, query parameters              |
| **Documentation Specialist** | Gabriel Khot Garang | OpenAPI specs, usage examples                 |
| **Security Designer**     | Chiedu Paul Unekwe   | OTP auth, JWT, payment security               |

---

##  Project Overview

JuaJobs is a mobile-first platform that:
- Enables clients to post jobs and workers to apply  
- Supports mobile money payments (MTN/Airtel)  
- Uses geolocation and multilingual interfaces (`en_RW`, `fr_RW`)  
- Optimized for low-bandwidth areas with offline-sync capabilities  

---

## Tech Stack

| Category          | Technologies                          |
|-------------------|---------------------------------------|
| **Backend**       | Django + Django REST Framework        |
| **Database**      | PostgreSQL                            |
| **Authentication**| Phone OTP + JWT                       |
| **Payments**      | MTN Mobile Money, Airtel, Bank Transfer |
| **Localization**  | Multi-language (en_RW, fr_RW), Multi-currency (RWF, KES, USD) |
| **DevOps**        | Docker-ready                          |

---

## Documentation

### API Specifications
🔗 [JuaJobs API Spec & ERD](https://docs.google.com/document/d/1m40c0K7Lsxi34NLKKlE6wrZxPwEzvIRiRe-1AZeOAt8/edit?usp=sharing)  
🔗 [OpenAPI Documentation](https://editor.swagger.io/) *(Import the YAML spec from `/docs/openapi.yaml`)*  

**Includes:**
- RESTful routes (`/api/v1/`)
- OTP Auth Flow (`/auth/otp/send`, `/auth/otp/verify`)
- Job posting, applications, and payment endpoints
- Admin tools
- Escrow and mobile money integration

### Full Project Documentation
🔗 [Functional & Architecture Docs](https://docs.google.com/document/d/1HmTD2_SmpRl7EwMgQIzeltMcq4oBDWom8y6-qqBRAdc/edit)  
Covers use-case personas, API flows, offline design, and payment workflows.

---

### Presentation
 Stakeholder & Team Presentation Slides  [View Canva/Google Slides Here](https://www.canva.com/design/DAGorIn2Jt0/gWQFmBTN-DN-6r4BPwagPA/edit)

---

##  Getting Started

### Local Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/YourOrg/JuaJobs_API-GroupX10.git
   cd JuaJobs_API-GroupX10
