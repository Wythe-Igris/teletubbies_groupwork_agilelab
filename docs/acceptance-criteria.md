# Acceptance Criteria

## Purpose

These criteria define observable conditions for accepting the IMAGINARY MVP. Each scenario uses Given/When/Then language and can be converted into a manual or automated test.

## AI Student Assistant

### AC-01 — Submit a valid question

**Given** the Student Assistant page is available  
**When** a user enters a relevant student-life question and submits it  
**Then** the system displays a loading state and subsequently displays a simple-English answer associated with that question.

### AC-02 — Prevent an empty question

**Given** the question field is empty or contains only spaces  
**When** the user tries to submit it  
**Then** no AI request is sent and the system explains that a question is required.

### AC-03 — Handle uncertainty

**Given** the system cannot produce a sufficiently reliable answer  
**When** the response is displayed  
**Then** it states the uncertainty and advises the user to verify important information through an appropriate official source.

### AC-04 — Handle an AI service failure

**Given** the external AI service fails or times out  
**When** a user submits a question  
**Then** the page remains usable, displays a clear error, and provides a way to try again.

### AC-05 — Display responsible-use guidance

**Given** a user views or receives AI-generated guidance  
**When** the result is shown  
**Then** the interface states that the answer may need verification and is not an official university decision.

## University Notice Simplifier

### AC-06 — Simplify a notice

**Given** a user has pasted non-empty university-notice text  
**When** the user selects the simplify action  
**Then** the result contains distinct sections for a short summary, important dates, and required actions.

### AC-07 — Extract dates and actions

**Given** a notice contains an explicit deadline and an action for students  
**When** it is simplified  
**Then** the deadline appears in the dates section and the student action appears in the actions section without inventing information absent from the notice.

### AC-08 — Handle missing dates or actions

**Given** a valid notice contains no identifiable date or required action  
**When** it is simplified  
**Then** the corresponding section displays “None identified.”

### AC-09 — Prevent an empty notice

**Given** the notice field is empty or contains only spaces  
**When** the user tries to simplify it  
**Then** no AI request is sent and the system explains that notice text is required.

### AC-10 — Warn about sensitive information

**Given** the Notice Simplifier input is visible  
**When** the user prepares to paste text  
**Then** a visible message warns against entering passwords, financial details, identification numbers, or other sensitive personal data.

## Thai Phrase Helper

### AC-11 — Display complete phrase information

**Given** a stored phrase is displayed  
**Then** its English meaning, Thai script, pronunciation, and category are visible.

### AC-12 — Browse by category

**Given** phrase records exist in multiple categories  
**When** the user selects one category  
**Then** only phrases assigned to that category are displayed.

### AC-13 — Search phrases

**Given** phrase records exist  
**When** a user enters a partial or complete English meaning, Thai phrase, or pronunciation  
**Then** matching phrases are displayed without requiring an exact case-sensitive English match.

### AC-14 — Show no matching phrases

**Given** the search term does not match any stored phrase  
**When** search results are evaluated  
**Then** the system displays a friendly no-results message and a way to clear or change the search.

### AC-15 — Provide required categories

**Given** the initial phrase dataset has been loaded  
**When** the category list is viewed  
**Then** university, transportation, restaurants, shopping, and emergencies are available.

## Common Quality Criteria

### AC-16 — Navigate to MVP features

**Given** a user opens the application  
**When** the user uses the primary navigation  
**Then** the Student Assistant, Notice Simplifier, and Thai Phrase Helper are each reachable.

### AC-17 — Mobile layout

**Given** the viewport width is 360 px  
**When** the user completes the main task for each MVP feature  
**Then** required content and controls remain visible and usable without horizontal page scrolling.

### AC-18 — Keyboard operation

**Given** a user operates the application with a keyboard  
**When** the user moves through and activates interactive controls  
**Then** all core actions are reachable, the focus order is logical, and focus is visibly indicated.

### AC-19 — Protect credentials

**Given** the public repository is scanned before release  
**When** tracked source and configuration files are inspected  
**Then** no working API key, password, token, or other secret is present.

### AC-20 — Keep features isolated during failure

**Given** the AI service is unavailable  
**When** the user opens the Thai Phrase Helper  
**Then** stored categories, browsing, and search remain usable.

## MVP Release Acceptance

The MVP is accepted when:

- AC-01 through AC-20 pass in the agreed test environment.
- Every Must-priority requirement is implemented.
- No unresolved critical or high-severity defect remains.
- The Product Owner reviews the increment and accepts it during the sprint review.
- The public repository contains setup instructions and no secrets or personal test data.

## Evidence Record

The team can use this table during review:

| Criterion | Result | Evidence or issue link | Tester | Date |
|---|---|---|---|---|
| AC-01 | Not tested |  |  |  |
| AC-02 | Not tested |  |  |  |
| AC-03 | Not tested |  |  |  |
| AC-04 | Not tested |  |  |  |
| AC-05 | Not tested |  |  |  |
| AC-06 | Not tested |  |  |  |
| AC-07 | Not tested |  |  |  |
| AC-08 | Not tested |  |  |  |
| AC-09 | Not tested |  |  |  |
| AC-10 | Not tested |  |  |  |
| AC-11 | Not tested |  |  |  |
| AC-12 | Not tested |  |  |  |
| AC-13 | Not tested |  |  |  |
| AC-14 | Not tested |  |  |  |
| AC-15 | Not tested |  |  |  |
| AC-16 | Not tested |  |  |  |
| AC-17 | Not tested |  |  |  |
| AC-18 | Not tested |  |  |  |
| AC-19 | Not tested |  |  |  |
| AC-20 | Not tested |  |  |  |
