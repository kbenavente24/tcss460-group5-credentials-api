# TCSS 460 – Group 5 Dataset Web API (TV Shows)

This repository contains the Group 5 Web API project for the TCSS 460 Back-End Development course.
It consists of two integrated components:

1. **Dataset Web API (TV Shows)** – Manages TV show, actor, and related data.
2. **Credentials Web API (Auth²)** – Provides user authentication and authorization.

Both APIs are deployed, fully functional, documented, and tested with Postman.
**🌐 Hosted Data Web API URL (Render):** [https://helloworld-api-su2v.onrender.com](https://helloworld-api-su2v.onrender.com)

**📚 API Documentation:** [https://helloworld-api-su2v.onrender.com/api-docs](https://helloworld-api-su2v.onrender.com/api-docs)

### Credentials (Auth²) API
- **Base URL:** 
- **Swagger Docs:**

## 🧩 Functionality

### 🎥 Dataset Web API (TV Shows)
- CRUD operations for TV shows and actors  
- Search/filter TV shows by genre, release year, or network  
- Pagination and error-handling middleware  
- Relational data linking actors to TV shows  
- Hosted database (PostgreSQL on Render/Heroku)  
- Integrated Swagger UI documentation  

### 🔐 Credentials Web API (Auth²)
Built on the **Auth² student template** (Node.js, Express, TypeScript, PostgreSQL)

#### Implemented Features
- User registration, login, password reset  
- Email verification and token-based authentication  
- Secure JWT-based session handling  
- Input validation (express-validator)  
- Protected routes with middleware  
- Admin API routes for role management

 ## 🚀 Production Sprint Contribution
 **Group Members**

- **Balkirat Singh** – During this sprint, I helped across multiple parts of the API by assisting with debugging and testing the POST, PUT, DELETE, and pagination features while helping make the error handling and API key protection more consistent. I also updated portions of the documentation when new routes were added and helped teammates set up and test their routes on both local and Render environments. On top of that, I started preparing for the next sprint requirements by researching how to add login and register functionality with JWTs, planning the user credentials table for PostgreSQL, and looking into how to host the database externally the way the instructor requires.
- **Kobe Benavente** –  Implemented the POST endpoint for creating new TV shows with comprehensive validation including required field checks, data type validation for numeric fields, and
  rating bounds enforcement (0-10). Developed the DELETE endpoint to remove TV shows by ID with pre-deletion existence verification and detailed error messages. Also coordinated with team
  members to help integrate the new endpoints and update their local projects to reflect the latest API changes.
- **MD Khan (Shanto)** - Helped implement and test the POST, PUT, and DELETE endpoints for managing TV show data, contributing to full CRUD functionality within the API. Worked on building the routes to handle show creation, updates, and deletion with consistent validation, error handling, and database integration.
- **Pham Nguyen** - Implemented all validation functions in src/core/middleware/validation.ts using express-validator, including validateLogin, validateRegister, validatePasswordResetRequest, validatePasswordReset, and validatePasswordChange. Ensured that invalid input data triggers proper error messages, enhancing security and user feedback. Conducted extensive Postman testing to verify that all validation logic works as intended and that the API responds consistently to invalid requests.
---

## 💬 Production Sprint Meetings

**Primary Communication Methods**

- **Discord:** Used for group coordination, sprint planning, and real-time collaboration during Production Sprint.
- **GitHub:** Used for version control, pull requests, code reviews, and tracking sprint progress.

**Meeting Details**

- **When/Where:** Weekly Discord voice meetings and continuous asynchronous collaboration via Discord text channels and GitHub throughout the Beta II Sprint period.

### Topics Discussed
- Data API route implementation and testing  
- PostgreSQL connection and deployment  
- Swagger documentation configuration  
- Auth² validation and admin route setup  
- Integration testing using Postman

## 💬 Production Sprint Comments

- **Deployment:** Encountered minor build timeout issues on Render; resolved by optimizing build steps.  
- **Integration:** Integrated authentication tokens between two APIs successfully.  
- **Testing:** Enhanced Postman coverage for all route combinations.  
- **Learning:** Gained hands-on experience with route validation, JWT, and cloud deployment.  
- **Next Steps:** Extend Dataset API with search and sorting enhancements.  

---
## 🗂️ Current Repository Structure
```
tcss460-group5-tv-api/
├── src/
│   ├── app.ts                     # Express app configuration
│   ├── index.ts                   # Server entry point
│   ├── routes/
│   │   ├── open/                  # Public routes
│   │   ├── closed/                # Protected routes
│   │   └── admin/                 # Admin routes (TODO)
│   ├── controllers/
│   │   ├── authController.ts      # Authentication logic
│   │   ├── verificationController.ts
│   │   └── adminController.ts     # Admin controller (TODO)
│   ├── core/
│   │   ├── middleware/
│   │   │   ├── jwt.ts             # JWT validation
│   │   │   ├── validation.ts      # Validation chains (TODO)
│   │   │   └── adminAuth.ts       # Admin middleware (TODO)
│   │   ├── utilities/             # Helper utilities
│   │   └── models/                # TypeScript interfaces
│   └── test/                      # Test setup
├── data/
│   ├── init.sql                   # Database schema
│   └── heroku.sql                 # Heroku deployment schema
├── docs/
│   └── swagger.yaml               # API documentation
├── docs-2.0/                      # Educational documentation
├── ai.prof/                       # AI assistant instructions
└── .claude/                       # Claude Code commands
```


## 🧩 Production Sprint Summary
During the Production Sprint, Group 5 successfully integrated the Dataset Web API (TV Shows) and Credentials Web API (Auth²) into a cohesive, cloud-hosted back-end system.
This milestone marked the completion of full CRUD functionality, secure authentication, hosted documentation, and comprehensive testing across both APIs.
## ✅ Key Achievements
1. Full CRUD Functionality (Dataset API)
Implemented POST, GET, PUT, and DELETE endpoints for TV shows and actors.
Added filtering by year, genre, and network, plus pagination for efficient data retrieval.
Ensured consistent error handling and validation across all routes.
2. Authentication & Authorization (Credentials API)
Implemented user registration, login, and JWT-based authentication for secure route access.
Added email verification and password reset capabilities.
Created a foundation for admin-level access control, with admin middleware placeholders prepared for future extension.
3. Cloud Deployment & Database Integration
Successfully deployed both APIs on cloud platforms (Render for Dataset API; Heroku/Render for Auth²).
Configured and hosted the PostgreSQL databases externally, ensuring full functionality independent of local environments.
4. API Documentation & Testing
Updated and hosted Swagger UI documentation at the /api-docs route for both APIs.
Created a comprehensive Postman collection located in /testing/Postman/postman.json, testing all routes, authentication flows, and error responses.
5. Team Collaboration & Workflow
Coordinated using Discord for sprint planning and GitHub for version control and code reviews.
Conducted weekly sync meetings and asynchronous development throughout the sprint.
## 🧠 Lessons Learned
Improved understanding of Express.js architecture, JWT security, and PostgreSQL integration.
Learned best practices for cloud deployment, documentation hosting, and API testing.
Strengthened teamwork and sprint-based project management skills.
## 🔜 Next Steps
Complete the admin routes for role-based access control.
Optimize query performance and response caching for large datasets.
Add search and sorting enhancements to improve API usability.
