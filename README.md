# SkillHub – A Collaborative Learning and Mentorship Platform

## Project Description

Implement SkillHub, a multi-user Web API platform where users register as learners, mentors, or admins. Enable learners to search topics, enroll in mentorship sessions, and track progress. Allow mentors to create sessions, manage learners, and evaluate progress. Provide admins with system oversight and user management capabilities. Create a fully documented RESTful API for consumption by a frontend or mobile app (frontend not required).

## Learning Objectives

- Develop a .NET Web API using real-world architecture
- Implement authentication and role-based access control
- Apply clean code principles and design patterns
- Utilize EF Core with migrations and LINQ
- Validate inputs and handle errors effectively
- Write and execute unit and integration tests

## Core Features and Requirements

### 1. User Management
- Implement registration and login using JWT-based authentication
- Define roles: Learner, Mentor, Admin
- Use password hashing (ASP.NET Core Identity or manual implementation)
- Enable profile management (name, email, bio)

### 2. Mentorship & Learning Sessions
- For Mentors:
  - Implement creation, editing, and deletion of sessions
  - Include metadata: title, description, tags, difficulty, time frame
- For Learners:
  - Enable browsing and searching of sessions
  - Implement session enrollment with capacity limits
  - Provide enrollment and status tracking

### 3. Admin Controls
- Implement user listing, searching, and filtering
- Enable viewing of sessions and enrollment statistics
- Allow activation/deactivation of users
- Provide moderation of flagged content (e.g., reviews)

### 4. Ratings and Reviews
- Enable learners to rate and review completed sessions
- Prevent multiple reviews per session per user
- Allow admins to hide or delete inappropriate content

### 5. File Uploads (Local Only)
- Enable mentors to upload files (e.g., PDFs, images)
- Store files on local disk (e.g., `/uploads`)
- Allow enrolled learners to download resources

### 6. Reporting
- Implement report generation:
  - Mentors can export session details (JSON or CSV)
  - Admins can generate user/session summaries

### 7. Search & Filtering
- Implement advanced filtering using query parameters (e.g., by mentor, tag, level)
- Include pagination and sorting (e.g., by popularity or newest)

## Technical Requirements

### Backend
- Use .NET 8 or the latest stable version (.NET Core accepted)
- Develop an ASP.NET Core Web API
- Follow a modular project structure
- Apply Clean Architecture or a similar layered approach

### Database
- Use SQLite or Local SQL Server Express (free)
- Implement EF Core Migrations for schema management
- Ensure referential integrity and seed sample data

### Authentication & Authorization
- Implement JWT Bearer token authentication
- Apply role-based authorization using `[Authorize]` attributes
- Seed roles and implement policy-based access control

### File Handling
- Save uploaded files to a local folder
- Expose download endpoints with access control

### Validation & Error Handling
- Implement input validation using Data Annotations (Fluent Validation optional)
- Use centralized exception handling middleware
- Return meaningful error responses (e.g., 400s, 403s)

### Documentation
- Generate Swagger/OpenAPI documentation with annotations
- Provide sample requests/responses for each endpoint

### Testing
- Write unit tests for services and controllers
- Create integration tests for key endpoints
- Use xUnit, Moq, and TestServer

## Optional (Extra Credit)
- Implement local caching with MemoryCache
- Add session attendance tracking (e.g., learner completion status)
- Simulate background jobs using `Task.Delay`
- Provide tag suggestion/autocomplete based on usage frequency
- Implement clean logging using a text file logger or Serilog (to disk)

## Deliverables
- Provide full source code in a GitHub repository (or zip archive)
- Include auto-generated Swagger documentation
- Supply example SQL data or migration setup
- Document project structure and architecture in a README
- Prepare a presentation and demo showcasing API usage via Postman or Swagger

## Checklist
- [ ] Implement user registration and login with JWT authentication
- [ ] Define and seed Learner, Mentor, and Admin roles
- [ ] Enable profile management with name, email, and bio
- [ ] Create endpoints for mentors to manage sessions (create/edit/delete)
- [ ] Add session metadata (title, description, tags, difficulty, time frame)
- [ ] Enable learners to browse, search, and enroll in sessions
- [ ] Implement session capacity limits and enrollment tracking
- [ ] Provide admin endpoints for user and session management
- [ ] Allow admins to moderate flagged content
- [ ] Enable learners to rate and review sessions (one per session)
- [ ] Implement file uploads for mentors and downloads for enrolled learners
- [ ] Create report generation for mentors (session details) and admins (summaries)
- [ ] Add advanced search and filtering with pagination and sorting
- [ ] Use .NET 8 or latest stable version with ASP.NET Core Web API
- [ ] Structure project modularly with Clean Architecture
- [ ] Use SQLite or SQL Server Express with EF Core Migrations
- [ ] Ensure referential integrity and seed sample data
- [ ] Implement JWT-based authentication and role-based authorization
- [ ] Store uploaded files locally and secure download endpoints
- [ ] Validate inputs and handle errors with middleware
- [ ] Generate Swagger documentation with sample requests/responses
- [ ] Write unit and integration tests using xUnit, Moq, and TestServer
- [ ] (Optional) Add caching, attendance tracking, background jobs, tag suggestions, or logging
- [ ] Deliver source code, documentation, and demo
