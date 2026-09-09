# n8n Drive Study Assistant

An automated study assistant built with n8n that monitors Google Drive, processes PDF files, generates AI-powered study material, and uploads the final study guide back to Google Drive.

## Features

- Monitor a Google Drive input folder
- Detect newly uploaded PDF files
- Prevent duplicate file processing
- Download PDF files automatically
- Extract text from PDFs
- Clean and validate extracted text
- Generate AI-powered:
  - Summary
  - Key points
  - Questions and answers
  - Flashcards
- Create a Markdown study guide
- Upload the generated study guide to Google Drive
- Store processed file records in PostgreSQL / Supabase
- Skip unsupported files
- Skip previously processed files

## Tech Stack

- n8n
- Google Drive
- OpenAI
- PostgreSQL
- Supabase
- JavaScript
- Markdown

## Workflow

```text
Google Drive Trigger
        ↓
Normalize File Metadata
        ↓
Check Supported PDF
        ↓
Check Duplicate in PostgreSQL
        ↓
Download PDF
        ↓
Extract PDF Text
        ↓
Clean Extracted Text
        ↓
OpenAI Study Analysis
        ↓
Parse AI JSON
        ↓
Build Study Guide
        ↓
Convert Study Guide to File
        ↓
Upload to Google Drive
        ↓
Save Processing Record
