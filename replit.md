# MedExtract Pro - Medical Document Processing Platform

## Overview

MedExtract Pro is a comprehensive medical document processing platform designed to extract, analyze, and manage structured data from various medical documents. The application uses advanced OCR (Optical Character Recognition) and NLP (Natural Language Processing) technologies to convert unstructured medical documents into searchable, structured data.

## System Architecture

The application follows a modern full-stack architecture with the following key components:

- **Frontend**: React-based SPA with TypeScript, using Vite for build tooling and Wouter for routing
- **Backend**: Express.js server with TypeScript, handling API requests and file processing
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **UI Framework**: Tailwind CSS with shadcn/ui components for consistent design
- **File Processing**: Multer for file upload handling with OCR and NLP services
- **State Management**: TanStack Query for server state management

## Key Components

### Frontend Architecture
- **React Components**: Modular component structure with TypeScript
- **UI Components**: shadcn/ui component library for consistent design system
- **Styling**: Tailwind CSS with custom medical theme colors and utilities
- **State Management**: TanStack Query for API state management and caching
- **File Handling**: Custom file processing tracker for upload progress monitoring

### Backend Architecture
- **Express Server**: RESTful API with middleware for logging and error handling
- **File Processing Pipeline**: Multi-stage processing (OCR → NLP → Data Extraction)
- **Database Layer**: Drizzle ORM with PostgreSQL for data persistence
- **Service Layer**: Modular services for OCR, NLP, and file processing operations

### Database Schema
- **Documents**: File metadata, processing status, and patient associations
- **Extractions**: Structured data extracted from documents with confidence scores
- **Processing Jobs**: Background job tracking for document processing
- **Activity Logs**: Audit trail for all system activities

## Data Flow

1. **File Upload**: Users upload medical documents through the web interface
2. **Processing Queue**: Files are queued for processing with status tracking
3. **OCR Processing**: Images and PDFs are processed using Tesseract.js for text extraction
4. **NLP Analysis**: Extracted text is analyzed to identify medical entities (patient info, vitals, medications, etc.)
5. **Data Storage**: Structured data is stored in PostgreSQL with confidence scores
6. **User Interface**: Processed data is displayed in searchable tables with filtering options

## External Dependencies

### Core Libraries
- **@neondatabase/serverless**: PostgreSQL database connectivity
- **drizzle-orm**: Type-safe database ORM
- **tesseract.js**: OCR processing for image-to-text conversion
- **multer**: File upload handling middleware
- **@tanstack/react-query**: Server state management

### UI Components
- **@radix-ui/***: Accessible UI primitives for form controls and interactions
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Component variant management
- **lucide-react**: Icon library

### Development Tools
- **vite**: Fast build tool and development server
- **typescript**: Type safety and developer experience
- **esbuild**: Fast bundling for production builds

## Deployment Strategy

The application is configured for deployment on Replit with the following setup:

- **Development**: `npm run dev` starts both frontend and backend in development mode
- **Build**: `npm run build` creates production builds for both client and server
- **Production**: `npm run start` runs the production server
- **Database**: PostgreSQL 16 module configured for data persistence
- **Port Configuration**: Server runs on port 5000 with external port 80 mapping

### Environment Configuration
- **NODE_ENV**: Controls development/production behavior
- **DATABASE_URL**: PostgreSQL connection string (required)
- **File Storage**: Local uploads directory for document storage

## Changelog

- June 18, 2025. Initial setup

## User Preferences

Preferred communication style: Simple, everyday language.