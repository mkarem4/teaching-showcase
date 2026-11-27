# Teaching — Multi-Tenant Academy Platform

**One platform, many academies.** Teaching is a multi-tenant SaaS for tutoring centres and academies: every tenant gets its own isolated workspace with courses, lessons, exams, study groups and payments, while a central panel manages tenants, plans and audit.

> This repository is a project showcase. It contains documentation only — the production source code is private.

---

## Overview

A teaching business needs more than a course page. It needs enrolments, groups, sessions, exams, payments and follow-up, with each academy's data kept apart from every other academy's.

Teaching does that with a tenant-per-database architecture: the central application owns tenants, SaaS plans and the audit log, and each tenant runs its own isolated database for its courses, students, groups, exams and payments.

## My role

**Senior Laravel Backend Engineer & Team Lead**

- Built the multi-tenant architecture: tenant provisioning, tenant-aware models, central versus tenant boundaries.
- Built the domain: courses, sections, lessons, exams and the exam runner.
- Built the study-group model: enrolments, sessions, makeup sessions, transfers and follow-up tasks.
- Built payments, coupons and access codes, and the central SaaS plans.
- Built the admin panels and the API, with permissions per role and panel.

## Tech stack

| Area | Stack |
| --- | --- |
| Language & framework | PHP 8.3, Laravel 13, MVC, Eloquent ORM |
| Multi-tenancy | stancl/tenancy (database per tenant) |
| Admin panels | Filament 5, Livewire 4 |
| Data | MySQL |
| API & auth | Laravel Sanctum |
| Permissions | Filament Shield, Spatie permissions |
| Background work | Laravel queues and jobs |
| Auditing | Central audit log |
| Delivery | Git, CI/CD, Linux, Nginx |

## Key features

**Tenancy**
- Database-per-tenant isolation with stancl/tenancy.
- A central application for tenants, SaaS plans and the audit log.
- Automatic teacher provisioning: a job creates a new teacher's workspace and wiring.

**Courses**
- Subjects, courses, sections and lessons.
- Enrolments that tie a student to the course they are studying.

**Exams**
- A question bank per tenant, with exam definitions built from it.
- Attempts recorded per student, with a Livewire exam runner and an exam service behind it.
- Policies so a student only reaches their own attempts.

**Study groups**
- Groups with scheduled sessions, makeup sessions and group transfers.
- Student notes and follow-up tasks so nothing gets lost between sessions.

**Payments**
- Payments and group payments, with a payment review step.
- Coupons and access codes for enrolment.

**Platform**
- SaaS plans managed centrally.
- Announcements, per-tenant settings and device registration.
- Roles and permissions generated per panel.

## About this repository

This is a documentation-only showcase of a production product. It contains no client code, student data or infrastructure details.

**Mohamed Karem Tawfik** — Senior PHP / Laravel Developer, Backend Team Lead
[GitHub](https://github.com/mkarem4) · [LinkedIn](https://linkedin.com/in/mohamed-karem93)
