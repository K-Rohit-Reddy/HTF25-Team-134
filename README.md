# Recruitment & Resume Enhancement Platform

A smart platform for **candidates** and **recruiters** that leverages **GPT OSS** and other modern tools to enhance resumes, provide interview preparation, and assist recruiters in identifying the best candidates.

---

## Table of Contents

- [Overview](#overview)  
- [Tech Stack](#tech-stack)  
- [User Roles & Workflows](#user-roles--workflows)  
  - [Candidate](#candidate)  
  - [Recruiter](#recruiter)  
- [System Architecture](#system-architecture)  
- [Features](#features)  
- [Setup & Installation](#setup--installation)  
- [Usage](#usage)  
- [License](#license)  

---

## Overview

This platform provides two main user roles:

1. **Candidates:** Upload resumes, get them enhanced with tips, generate interview questions, and track improvement areas.  
2. **Recruiters:** Upload job descriptions and candidate resumes, view scoring, metrics, and select the best applicants.  

The system integrates AI-driven resume enhancement, scoring, course suggestions, and polished PDF/HTML resume generation.

---

## Tech Stack

- **Frontend:** Next.js  
- **Backend:** Node.js + FastAPI  
- **Database:** MongoDB  
- **AI Engine:** GPT OSS  
- **Search Engine:** For fetching certifications/courses (Candidate improvement)  
- **Resume Generation:** Puppeteer (PDF/HTML output)  

---

## User Roles & Workflows

### Candidate

**Workflow:**

1. Upload **resume** and **job description**.  
2. System extracts text and sends it to GPT OSS via a **predefined template**.  
3. GPT OSS returns:  
   - Enhanced Resume  
   - Resume Optimization Tips  
   - Score vs job description  
   - Weak areas / gaps  
4. Fetch **certifications/courses** to improve skills via Search Engine API.  
5. Optional: Generate **interview questions** via GPT OSS.  
6. Generate polished resume (PDF/HTML) via Puppeteer.  
7. **Dashboard:**  
   - View scores  
   - Weak areas  
   - Suggested courses  
   - Enhanced resume  

---

### Recruiter

**Workflow:**

1. Upload **job description** and multiple **candidate resumes**.  
2. Backend analyzes resumes for **job fit & ranking**.  
3. GPT OSS can enhance resumes and provide scoring/feedback.  
4. Store all data in **MongoDB**.  
5. **Dashboard:**  
   - View all applicants  
   - Scores, metrics, and ranking  
   - Enhanced resumes  
   - Summary analytics  

---

## System Architecture

The platform has **two distinct lanes** for Candidate and Recruiter:

- **Candidate Lane:** Upload → GPT OSS → Scores → Weak Areas → Courses → Enhanced Resume → Dashboard  
- **Recruiter Lane:** Upload → GPT OSS → Scoring → Metrics → Dashboard  
- Shared components include: Backend API, Database (MongoDB), GPT OSS, Search Engine, and Puppeteer for resume generation.  

---

## Features

- **AI-Enhanced Resumes:** GPT OSS improves resumes based on job description.  
- **Optimization Tips:** Personalized feedback and weak area identification.  
- **Interview Questions:** Automatically generated based on job description.  
- **Course Suggestions:** Recommend relevant courses or certifications for improvement.  
- **Candidate Dashboard:** Track scores, gaps, enhanced resumes, and suggested courses.  
- **Recruiter Dashboard:** View applicant scores, metrics, rankings, and enhanced resumes.  
- **Resume Export:** Generate polished PDF or HTML resumes via Puppeteer.  

---