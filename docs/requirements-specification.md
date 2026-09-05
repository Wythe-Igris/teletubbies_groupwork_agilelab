# Requirements Specification

## 1. Purpose

This document defines the functional and non-functional requirements for the IMAGINARY MVP, an AI-powered student life assistant for international university students in Thailand.

## 2. Product Scope

The MVP is a responsive web application with three capabilities:

1. AI Student Assistant.
2. University Notice Simplifier.
3. Thai Phrase Helper.

The MVP gives general guidance and does not replace official university, legal, medical, financial, or emergency services.

## 3. User Groups

| User group | Description |
|---|---|
| International student | Primary user seeking understandable information about university and daily life |
| Content maintainer | Team member who adds, updates, or verifies Thai phrase data |
| Product Owner | Reviews feedback and prioritizes requirements and backlog items |

Anonymous students are the primary actors in the MVP. Authentication and student profiles are not required.

## 4. User Stories

| ID | Priority | User story |
|---|---|---|
| US-01 | Must | As an international student, I want to ask a student-life question so that I can receive a simple English answer. |
| US-02 | Must | As an international student, I want to see a cautious response when an answer is uncertain so that I know when to verify it. |
| US-03 | Must | As an international student, I want to paste a university notice so that I can understand its main message quickly. |
| US-04 | Must | As an international student, I want important dates and required actions separated from the summary so that I do not miss them. |
| US-05 | Must | As an international student, I want to browse Thai phrases by situation so that I can communicate in common situations. |
| US-06 | Must | As an international student, I want to search Thai phrases so that I can find a useful phrase quickly. |
| US-07 | Must | As a mobile user, I want the website to adapt to my screen so that I can use it while travelling. |
| US-08 | Should | As a student, I want to see Thai script, pronunciation, and English meaning together so that I can use a phrase correctly. |
| US-09 | Should | As a student, I want clear errors and retry options so that temporary failures do not confuse me. |
| US-10 | Could | As a student, I want to copy a phrase or generated result so that I can use it in another application. |

Priority uses MoSCoW: Must, Should, Could, and Won't for this release.

## 5. Functional Requirements

### 5.1 Common interface

| ID | Requirement |
|---|---|
| FR-01 | The system shall provide navigation to all three MVP features. |
| FR-02 | The system shall identify each feature with a title and short instruction. |
| FR-03 | The system shall validate required input before submitting a request. |
| FR-04 | The system shall display a loading state while an AI request is being processed. |
| FR-05 | The system shall display a clear error and allow another attempt when a request fails. |
| FR-06 | The system shall display a notice that AI-generated guidance may need verification with official sources. |

### 5.2 AI Student Assistant

| ID | Requirement |
|---|---|
| FR-07 | The system shall accept a text question about university or daily life in Thailand. |
| FR-08 | The system shall reject an empty or whitespace-only question. |
| FR-09 | The system shall return an answer written in simple English. |
| FR-10 | The answer shall clearly state uncertainty or recommend an official contact when reliable guidance cannot be produced. |
| FR-11 | The system shall keep the submitted question visible with its corresponding answer during the current interaction. |
| FR-12 | The system shall refuse unsafe or clearly out-of-scope requests with a helpful explanation. |

### 5.3 University Notice Simplifier

| ID | Requirement |
|---|---|
| FR-13 | The system shall accept pasted university-notice text. |
| FR-14 | The system shall reject empty or whitespace-only notice text. |
| FR-15 | The system shall produce a short plain-English summary. |
| FR-16 | The system shall list dates or deadlines found in the notice. |
| FR-17 | The system shall list actions required from the student. |
| FR-18 | The system shall explicitly show “None identified” when no date or action can be identified. |
| FR-19 | The system shall warn users not to paste passwords, financial details, identification numbers, or other sensitive personal data. |

### 5.4 Thai Phrase Helper

| ID | Requirement |
|---|---|
| FR-20 | The system shall display phrases from stored phrase records. |
| FR-21 | Each phrase shall include an English meaning, Thai script, pronunciation, and category. |
| FR-22 | The system shall allow users to browse phrases by category. |
| FR-23 | The system shall allow users to search by English meaning, Thai script, or pronunciation. |
| FR-24 | The initial categories shall include university, transportation, restaurants, shopping, and emergencies. |
| FR-25 | The system shall show a no-results message when no phrase matches the search. |

## 6. Non-Functional Requirements

| ID | Category | Requirement |
|---|---|---|
| NFR-01 | Usability | Labels, instructions, messages, and generated output shall use clear, simple English. |
| NFR-02 | Responsive design | Core tasks shall be usable at viewport widths from 360 px upward without horizontal scrolling. |
| NFR-03 | Accessibility | Interactive controls shall be keyboard accessible, visibly focused, and programmatically labelled. |
| NFR-04 | Accessibility | Text and essential controls shall meet WCAG 2.1 AA color-contrast targets. |
| NFR-05 | Performance | Locally stored phrase searches shall return results within one second under normal test conditions. |
| NFR-06 | Feedback | The interface shall show a loading indication within one second of submitting an AI request. |
| NFR-07 | Reliability | A failed external AI request shall not crash the application or prevent access to the Phrase Helper. |
| NFR-08 | Security | API credentials and secrets shall be stored outside source code and shall not be committed to the public repository. |
| NFR-09 | Privacy | Raw questions and notices shall not be stored persistently by default. If logging is enabled, sensitive text shall be excluded or anonymized. |
| NFR-10 | Data quality | Published phrase records shall be marked as verified only after review by a competent reviewer. |
| NFR-11 | Compatibility | The application shall support the latest stable versions of Chrome, Safari, Firefox, and Edge available during testing. |
| NFR-12 | Maintainability | Feature logic, AI integration, and data access shall be separated sufficiently to allow independent testing and replacement. |

## 7. Business Rules

- BR-01: IMAGINARY provides guidance, not an official university decision.
- BR-02: Important university information should direct students to an official office or source when available.
- BR-03: A phrase marked as verified must record when it was verified.
- BR-04: User-submitted question and notice content is temporary unless the user is explicitly informed and gives consent to storage in a future version.
- BR-05: Emergency queries must advise the user to contact appropriate emergency or official services instead of relying only on AI output.

## 8. Data Requirements

- The MVP shall persist categories and Thai phrase records.
- AI request metadata may be stored for reliability monitoring, but raw user content is excluded by default.
- Each generated request shall have a type, status, and timestamps.
- Stored data shall use UTF-8 so Thai and English text are preserved correctly.
- Database identifiers shall not expose secrets or personal information.

## 9. External Interfaces

| Interface | Purpose |
|---|---|
| Web browser | Presents the responsive user interface |
| AI service API | Generates student-assistant answers and notice summaries |
| Application API | Validates requests, applies safety rules, and separates the browser from credentials |
| Relational database | Stores phrase categories, phrases, and optional non-sensitive request metadata |

## 10. Dependencies

- Availability and terms of the selected AI service.
- Internet access for AI-powered features.
- Reviewed Thai phrase content.
- A supported web browser.

## 11. MVP Exclusions

The following are Won't-have items for this release: user accounts, maps, live transport data, transactions, voice features, image translation, service finders, and full banking or SIM-card guides. They may be evaluated for later releases through backlog refinement.

## 12. Traceability

| User stories | Related requirements | Acceptance criteria |
|---|---|---|
| US-01, US-02 | FR-07–FR-12, NFR-01, NFR-06 | AC-01–AC-05 |
| US-03, US-04 | FR-13–FR-19, NFR-01, NFR-09 | AC-06–AC-10 |
| US-05, US-06, US-08 | FR-20–FR-25, NFR-05, NFR-10 | AC-11–AC-15 |
| US-07, US-09 | FR-01–FR-06, NFR-02–NFR-04, NFR-07 | AC-16–AC-20 |
