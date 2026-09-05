# Project Charter

## Project Information

| Field | Details |
|---|---|
| Project name | IMAGINARY — AI Student Life Assistant |
| Project type | Agile Software Development course lab assignment |
| Institution | Siam University |
| Product | Responsive web application |
| Primary users | International university students in Thailand |
| Development approach | Agile, using short iterations and continuous feedback |

## Background

International students in Thailand often face language barriers and have difficulty finding reliable university and daily-life information. Important information may be distributed across university websites, social media, and other online sources. Searching these sources can be slow and confusing, especially for students who are new to Thailand.

## Problem Statement

International university students in Thailand need a simple way to access and understand university and daily-life information because language barriers and scattered information can make studying and living in Thailand confusing.

## Vision

To provide one simple AI assistant for studying and living in Thailand.

## Project Goal

Design and develop a usable MVP that enables international students to:

1. Ask questions about university and daily life and receive clear English answers.
2. Paste a university notice and receive a concise summary of its key information, dates, and required actions.
3. Find useful Thai phrases for common student situations.

## Objectives

- Deliver the three MVP features in a responsive website.
- Use simple English throughout the interface and generated content.
- Make common tasks understandable without training.
- Organize the work as a prioritized product backlog and deliver it incrementally.
- Validate each increment against agreed acceptance criteria.
- Protect user-submitted text and avoid storing it longer than necessary.

## Scope

### In scope for the MVP

- AI Student Assistant for university and everyday-life questions.
- University Notice Simplifier for pasted text.
- Thai Phrase Helper with searchable phrases and categories.
- Basic navigation and responsive interface.
- Helpful error messages and basic input validation.
- Anonymous use; a user account is not required for the MVP.

### Out of scope for the MVP

- Maps and live transportation tracking.
- Banking, SIM-card, and complete student-life guides.
- Service-provider booking or transactions.
- Voice input, voice output, and automatic image translation.
- Support for universities or countries outside the initial Thailand context.
- A native mobile application.

## Key Deliverables

- Product backlog containing prioritized user stories.
- Working web application containing the three MVP features.
- Project charter, requirements specification, acceptance criteria, and database design.
- Test evidence showing that acceptance criteria have been checked.
- Demonstration and retrospective notes.

## Stakeholders

| Stakeholder | Interest or responsibility |
|---|---|
| International students | Primary users who need clear, quick guidance |
| Student project team | Designs, develops, tests, and demonstrates the MVP |
| Product Owner | Prioritizes the backlog and accepts completed stories |
| Scrum Master | Facilitates the Agile process and removes impediments |
| Course instructor | Reviews learning outcomes and assesses the assignment |
| University staff | Potential source and reviewer of university information |

For a small student team, one person may hold more than one team role, but the responsibilities should remain clear.

## Assumptions

- Users can access the website with an internet connection and a modern browser.
- Users can enter questions and notices as text.
- An AI service is available for question answering and notice simplification.
- The initial interface and AI responses are primarily in English.
- Phrase content can be prepared and reviewed before release.

## Constraints

- The project must fit the time and resources of a university lab assignment.
- AI output can be incomplete or inaccurate and must be presented as guidance, not official advice.
- External AI services may impose cost, rate, and availability limits.
- Personal or sensitive information must not be requested unnecessarily.

## Risks and Responses

| Risk | Impact | Planned response |
|---|---|---|
| AI provides incorrect information | Students may act on unreliable guidance | Display a disclaimer, cite or identify sources when available, and advise verification with official university channels for important matters |
| Student enters personal data in a notice | Privacy may be compromised | Show a warning and avoid persistent storage of submitted notice text by default |
| MVP scope grows too large | Delivery may be delayed | Keep only the three selected features in the MVP and place new ideas in the backlog |
| AI service is unavailable | Core features may fail | Return a clear retry message and keep the phrase helper available from stored data |
| Thai phrases are inaccurate | Miscommunication may occur | Review phrase content and store its verification status |

## Agile Delivery Approach

Work will be organized into short sprints. At the start of each sprint, the team selects the highest-priority ready stories. A story is complete only when its acceptance criteria pass and it meets the Definition of Done. Each sprint ends with a review and retrospective so feedback can influence the next increment.

## High-Level Milestones

| Milestone | Outcome |
|---|---|
| Discovery and planning | Charter, initial backlog, architecture, and acceptance criteria agreed |
| Increment 1 | Navigation and Thai Phrase Helper available |
| Increment 2 | AI Student Assistant available |
| Increment 3 | Notice Simplifier integrated and MVP tested |
| Final review | Demonstration, feedback, documentation, and retrospective completed |

## Success Measures

- All Must-have acceptance criteria pass.
- A first-time user can access each MVP feature from the main navigation.
- Test users can complete one task in each feature without assistance.
- At least 80% of test users rate the output as easy to understand.
- No critical or high-severity defects remain open at submission.

## Definition of Done

A backlog item is Done when:

- Its acceptance criteria pass.
- The implementation has been reviewed by another team member where possible.
- Relevant automated and manual tests pass.
- The interface works on current desktop and mobile-sized browsers.
- Error states and accessibility basics have been checked.
- No secrets or personal test data are committed to the public repository.
- Related documentation is updated.

## Authorization

This charter authorizes the student team to develop and evaluate the IMAGINARY MVP within the scope above. Material scope changes should be reviewed and reprioritized by the Product Owner before implementation.
