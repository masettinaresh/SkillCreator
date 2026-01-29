---
name: resume-builder
description: Generates a professional, ATS-friendly resume based on user input (experience, education, skills, job description).
---

# Resume Builder Skill

This skill helps an agent generate a structured and professional resume in Markdown or PDF format.

## When to use this skill
*   Use when the user asks to create, build, or format a resume.
*   Use when tailoring a resume to a specific job description.

## How to use it
The agent should follow these steps to collect information and build the resume:

1.  **Acknowledge the Request**: Confirm the intent to build or refine a resume.
2.  **Gather Information**: Ask the user to provide the following details:
    *   Contact Info (Name, Phone, Email, LinkedIn)
    *   Professional Summary/Objective
    *   Work Experience (Company, Title, Dates, Bullet Points for responsibilities/achievements)
    *   Education (Institution, Degree, Dates)
    *   Skills (Technical and Soft skills, ensure relevance to the job description if provided)
    *   (Optional) A target Job Description (JD)
3.  **Analyze and Format**:
    *   If a JD is provided, analyze it to extract key skills and keywords.
    *   Format the information into a clean, standard resume layout (e.g., using Markdown tables or a simple text structure).
    *   Ensure the use of standard headings (e.g., "Work Experience", "Education") for ATS compatibility.
    *   Use action verbs and quantifiable achievements in the experience section.
4.  **Present and Refine**: Present the generated resume content to the user for review. Offer to make revisions or convert it to a PDF.
