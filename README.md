# FUTURE_CS_03

## API Security Risk Analysis

## Project Overview

This project presents an API Security Risk Analysis conducted as part of the Future Interns Cyber Security Internship Programme. The assessment focused on identifying common API security risks using safe, read only testing techniques against the JSONPlaceholder public REST API.

The objective was to evaluate the API from a security consultant's perspective by reviewing authentication, authorization, data exposure, response headers, and other security related controls. No exploitation or unauthorised testing was performed.

## Objectives

The objectives of this project were to:

- Analyse a public REST API.
- Identify common API security risks.
- Assess authentication and authorization mechanisms.
- Evaluate potential business impacts.
- Recommend security improvements based on industry best practices.

## API Tested

**API Name:** JSONPlaceholder

**Base URL:**
https://jsonplaceholder.typicode.com

### Endpoints Tested

- GET `/posts`
- GET `/users`
- GET `/comments`
- GET `/albums`

## Tools Used

- Postman
- Google Chrome Developer Tools
- JSONPlaceholder Public API
- Microsoft Word
- GitHub

## Methodology

The following methodology was used during the assessment:

1. Reviewed the API documentation.
2. Sent read only GET requests using Postman.
3. Inspected request and response headers.
4. Analysed API responses for potential security risks.
5. Classified findings according to risk severity.
6. Proposed remediation recommendations.

## Security Findings

The assessment identified the following potential security risks:

- **Publicly accessible endpoints (High):** The tested API endpoints were accessible without authentication, allowing unrestricted access to data.

- **Missing authentication (High):** No API keys, bearer tokens, or other authentication mechanisms were required to access the endpoints.

- **Excessive data exposure (Medium):** The `/users` endpoint returned more information than may be necessary, including email addresses, phone numbers, company details, and addresses.

- **Missing authorization controls (Medium):** No visible access control mechanisms were observed to restrict users from accessing information that could belong to other users in a production environment.

- **No visible rate limiting (Low):** The API responses did not include any indication of rate limiting, which could allow excessive requests if implemented in a production system.

- **Input validation could not be confirmed (Low):** Since JSONPlaceholder is a demonstration API, it was not possible to verify whether server side input validation was implemented.

## Recommendations

The following recommendations were identified during the assessment:

- Require authentication for protected endpoints.
- Implement Role Based Access Control (RBAC).
- Return only the minimum data required by clients.
- Implement API rate limiting.
- Validate all user supplied input.
- Follow the OWASP API Security Top 10 guidelines.
- Perform regular API security assessments.

## Repository Structure

```text
FUTURE_CS_03
│
├── Report
│   └── Task 3 Report.pdf
│
├── Evidence
│   ├── headers.png
│   ├── JSON_api_documentation.png
│   ├── JSON_postman_get_albums.png
│   ├── JSON_postman_get_comments.png
│   ├── JSON_postman_get_posts.png
│   ├── JSON_postman_get_users.png
│   └── response_headers.png
│
└── README.md
```

## Learning Outcomes

This project strengthened practical knowledge of:

- API security fundamentals
- REST API testing
- Authentication and authorization analysis
- Security risk assessment
- Business impact evaluation
- Professional cybersecurity reporting

**Author**

**Entisaar Elfadl**

Bachelor of Business Science (Computer Science)

University of Cape Town