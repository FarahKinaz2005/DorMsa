# DorMsa: University Housing Platform for MSA Students

**DorMsa** is a web platform that connects MSA University students with verified property brokers near the October City campus. This repository contains the project's **Software Requirements Specification (SRS)**, prepared for the **CS347 Software Engineering** course, Faculty of Computer Science, MSA University.

## The Problem

Every semester, many MSA students need housing near campus, but there is no dedicated platform for it. Students rely on Facebook groups and word of mouth, which leads to scam listings, wasted time and payment disputes. DorMsa aims to be a trusted, verified marketplace built specifically for the MSA community.

## Users

| Role | What they can do |
|---|---|
| **Students / Parents** | Search housing, view listings, shortlist, book and pay a deposit |
| **Brokers** | Submit identity documents, create and manage property listings, view a dashboard |
| **Admins** | Verify brokers, moderate content, suspend users, view analytics |

## Key Features

- Role-based registration with OTP phone verification
- Property search filters: price, gender, room type, distance from campus
- Direct broker contact through WhatsApp and Call buttons
- Secure deposit payment processing
- Broker identity verification and listing management
- Admin dashboard for moderation, analytics and user management
- Automated notifications for bookings, new listings and listing expiry

## What's in the SRS

- Introduction, general description and constraints
- Functional requirements (FR01 to FR50) and non-functional requirements (NFR01 to NFR50)
- Interface requirements: UI screens, REST API, communications
- Performance requirements and design constraints
- Object-oriented domain analysis (`User`, `Student`, `Broker`, `Admin`, `Listing`, `Booking`, `Review`, `Notification`)
- Preliminary schedule and budget
- Appendices: use case diagram, requirements traceability matrix
- Diagrams: use case, sequence, class, rich picture, Gantt chart

## Planned REST API

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Create a new user account |
| POST | `/api/auth/verify-otp` | Validate the OTP and activate the account |
| GET | `/api/listings` | Get listings (filters: price, gender, distance) |
| POST | `/api/listings` | Create a listing (broker only) |
| POST | `/api/payments/deposit` | Start a deposit payment |
| GET | `/api/admin/pending-brokers` | List unverified brokers |
| PATCH | `/api/admin/brokers/:id/approve` | Approve a broker |

## Planned Integrations

- WhatsApp API: broker communication
- Google Maps API: distance from campus
- Twilio: OTP delivery by SMS
- PCI-DSS compliant payment gateway (Stripe or PayMob)

## Project Plan

| Phase | Weeks | Focus |
|---|---|---|
| 1. Requirements Analysis | 1-2 | Requirements gathering and SRS |
| 2. System Design | 3-4 | Diagrams, data modelling, architecture |
| 3. Core Development | 5-9 | Registration, search and filters, broker listings |
| 4. Advanced Features | 10-12 | Admin panels and analytics dashboards |

## Documents

- [`DorMsa_SRS.pdf`](DorMsa_SRS.pdf): the full Software Requirements Specification (111 pages)

## Team

| Name | ID |
|---|---|
| Farah Kinaz | 248311 |
| Retag Ahmed | 248727 |
| Shahd Maher | 248847 |
| Salah Bassem | 245469 |
| Muhammad Kandil | 245629 |
| Ahmed Walid | 242175 |

*Prepared May 2026, CS347 Software Engineering, MSA University.*
