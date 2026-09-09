# SauceDemo — Manual QA Testing

## About the Project

This is a **self initiated Manual QA Testing project** conducted on the SauceDemo web application. The project demonstrates a structured software testing process, from test planning and test case preparation to test execution, defect identification, documentation, and test result analysis.

The testing focused on the main user flows of the application, including:

* Login
* Product Listing
* Product Detail
* Shopping Cart
* Checkout
* Logout

The project was created as part of my QA portfolio to demonstrate practical skills in **manual functional testing, test case design, test execution, defect reporting, and test documentation**.

---

## My Role

**QA Tester — Self-Initiated Project**

Responsibilities:

* Analyzed application flows and identified testable functionalities.
* Prepared test scenarios and detailed test cases.
* Designed positive and negative test scenarios.
* Performed manual functional testing.
* Conducted exploratory testing to identify unexpected behavior.
* Performed UI checks across the tested application flows.
* Executed test cases and recorded test results.
* Identified and documented defects with clear reproduction steps.
* Prepared test evidence to support test results and defect findings.
* Analyzed test execution results and prepared the final test summary report.

---

## Application Flow Tested

```text
Login
  ↓
Product Listing
  ↓
Product Detail
  ↓
Shopping Cart
  ↓
Checkout
  ↓
Logout
```

---

## Testing Approach

The following testing approaches were used:

### Functional Testing

Validated whether application functionalities behaved according to their expected behavior.

### Positive Testing

Verified that valid inputs and normal user flows produced the expected results.

### Negative Testing

Verified application behavior when invalid, incomplete, or unexpected inputs were provided.

### Exploratory Testing

Performed unscripted testing to identify unexpected behavior and potential usability or UI issues beyond the predefined test cases.

### UI Testing

Checked visual and layout consistency of the tested pages, including element positioning and displayed information.

---

## Test Coverage

| Module          | Coverage                                                                                    |
| --------------- | ------------------------------------------------------------------------------------------- |
| Login           | Valid/invalid credentials, empty fields, locked user, password masking, keyboard submission |
| Product Listing | Product display, product information, sorting, adding products                              |
| Product Detail  | Product details, product information, add to cart, return navigation                        |
| Shopping Cart   | Add/remove products, cart badge, product information, navigation                            |
| Checkout        | Customer information validation, order summary, price/subtotal/tax/total, order completion  |
| Logout          | Logout functionality and session termination                                                |

---

## Test Execution Summary

| Metric             | Result |
| ------------------ | -----: |
| Total Test Cases   |     47 |
| Passed             |     43 |
| Failed             |      4 |
| Blocked            |      0 |
| Pass Rate          | 91.49% |
| Fail Rate          |  8.51% |
| Documented Defects |      2 |
| Open Defects       |      2 |

### Module Results

| Module          | Result              |
| --------------- | ------------------- |
| Login           | 7 Passed / 3 Failed |
| Product Listing | Passed              |
| Product Detail  | Passed              |
| Shopping Cart   | Passed              |
| Checkout        | Passed              |
| Logout          | 2 Passed / 1 Failed |

The overall test execution was completed with a **91.49% pass rate**.

The four failed test cases were primarily related to unclear or truncated error messages. These failed test cases do not represent four separate defects, as multiple failed test cases were associated with the same underlying issue.

---

## Defects Identified

### BUG-001 — Login Error Message Is Truncated and Unclear

**Priority:** Low
**Status:** Open

The error message displayed during invalid login attempts was truncated and unclear.

Affected test cases:

* TC-LOGIN-002 — Invalid Username
* TC-LOGIN-003 — Invalid Password
* TC-LOGIN-004 — Invalid Username and Password

**Expected Result:**

A complete and clear error message should be displayed to inform the user why the login attempt was unsuccessful.

**Actual Result:**

The login attempt was rejected, but the displayed error message was truncated and unclear.

---

### BUG-002 — Footer Position Is Not Consistent Across Pages

**Priority:** Low
**Status:** Open

The footer position and alignment were not consistent across different pages or viewport conditions.

**Expected Result:**

The footer should maintain a consistent position and layout across the application.

**Actual Result:**

The footer position/alignment changed depending on the page or viewport.

---

## QA Deliverables

The following documents are included in this repository:

* [Test Plan](Test-Plan/Test%20Plan.pdf)
* [Test Scenarios](Test-Scenarios/Test%20Scenarios.pdf)
* [Test Cases](Test-Cases/Test%20Cases.pdf)
* [Test Execution](Test-Execution/Test%20Execution.pdf)
* [Exploratory Testing](Exploratory-Testing/Exploratory%20Testing.pdf)
* [Bug Reports](Bug-Reports/Bug%20Reports.pdf)
* [Test Evidence](Evidence/)

Each document provides different information and is intended to demonstrate the complete manual testing workflow.

---

## Test Evidence

Test evidence is provided to support test execution results and documented defects.

Evidence includes screenshots related to:

* Successful test execution
* Failed test cases
* Identified defects
* Relevant application behavior

The evidence is organized by testing module to make the results easier to review.

Example structure:

```text
Evidence/
├── Login/
├── Product-Listing/
├── Product-Detail/
├── Shopping-Cart/
├── Checkout/
└── Logout/
```

---

## Repository Structure

```text
SauceDemo-Manual-QA/
│
├── README.md
│
├── Test Plan.pdf
│
├── Test Scenarios.pdf
│
├── Test Cases.pdf
│
├── Test Execution Report.pdf
│
├── Test Summary Report.pdf
│
├── Exploratory Testing Report.pdf
│
├── Bug-Reports/
│   ├── BUG-001.md
│   └── BUG-002.md
│
└── Evidence/
    ├── Login/
    ├── Product-Listing/
    ├── Product-Detail/
    ├── Shopping-Cart/
    ├── Checkout/
    └── Logout/
```

> The file names and folder structure can be adjusted according to the actual files uploaded to the repository.

---

## Test Environment

| Item           | Details                   |
| -------------- | ------------------------- |
| Application    | SauceDemo                 |
| Environment    | Production / Staging      |
| Testing Type   | Manual Functional Testing |
| Test Execution | Manual                    |

Browser and operating system information were not specified in the provided test documentation.

---

## Test Status

**COMPLETED — WITH OPEN DEFECTS**

The testing process was completed with:

* 47 test cases executed
* 43 test cases passed
* 4 test cases failed
* 0 blocked test cases
* 2 documented defects
* Both documented defects remain open
* Overall pass rate of 91.49%

---

## Key Findings

The majority of the tested application functionalities operated as expected.

The main findings were:

1. Invalid login attempts displayed a truncated or unclear error message.
2. The footer layout was not consistently positioned across pages or viewport conditions.
3. The four failed test cases were not equivalent to four separate defects.
4. Further testing should be performed after the identified defects are fixed.

---

## Recommendations

Based on the test results:

* Review and improve the clarity and completeness of login error messages.
* Review logout/session behavior and related user feedback.
* Review footer positioning and layout consistency.
* Perform **retesting** after the identified defects have been fixed.
* Perform **regression testing** after fixes to ensure existing functionality remains unaffected.
* Update defect documentation with the corresponding test case references when changes are implemented.

---

## Tools

* **GitHub** — Test documentation and portfolio repository
* **Microsoft Excel / Microsoft Word** — Test case and test execution documentation
* **Browser** — Manual application testing

---

## Project Outcome

This project demonstrates my ability to perform a structured manual QA process, including:

**Requirement & Flow Analysis → Test Scenario Preparation → Test Case Design → Test Execution → Defect Identification → Bug Documentation → Test Result Analysis**

The project also demonstrates practical experience in organizing QA documentation and maintaining traceability between test cases, execution results, defects, and supporting evidence.

---

## Disclaimer

This is a **self-initiated QA portfolio project** created for learning and demonstration purposes. It is not professional work experience or an official testing project conducted for SauceDemo.

The test results and documented defects represent observations made during the testing performed for this portfolio project.
