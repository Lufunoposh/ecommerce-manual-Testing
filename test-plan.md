
Test Plan: E-Commerce Website (Manual Testing)


1. Document Control & Overview

• Test Plan ID. TP-ECOM-001
• Project Name. [Insert Website Name] E-Commerce Platform
• Version. 1.0
• Author. [Your Name / QA Team]
• Objective. To validate that all customer-facing and back-end e-commerce workflows function accurately, securely, and smoothly across supported browsers and devices prior to launch.

2. Scope of Testing


In-Scope (Features to be Tested)

• User Authentication. Registration, login, logout, password recovery, and profile/address management.
• Navigation & Discovery. Homepage banners, category menus, search bar (valid/invalid keywords, autocomplete), sorting, and filtering.
• Product Detail Pages (PDP). Image galleries, price display, stock availability, variant selection (size, color), and customer reviews.
• Shopping Cart. Adding/removing items, updating quantities, saving for later, and real-time subtotal/tax recalculations.
• Checkout & Payments. Guest vs. registered checkout, shipping method selection, promo/coupon code application, and payment gateway integration (sandbox mode).
• Post-Purchase Workflows. Order confirmation screen, email notifications, order history tracking, and return/cancellation requests.
• Admin Panel (Basic). Adding/editing products, updating inventory counts, and viewing incoming orders.

Out-of-Scope (Excluded from Manual Scope)

• Automated Load & Stress Testing. High-concurrency performance testing (handled separately via tools like JMeter).
• Third-Party Payment Gateway Internals. Internal banking infrastructure beyond verifying proper API handoffs and response codes.
• Native Mobile Apps. Dedicated iOS/Android apps (only mobile web browsers are included in this plan).

3. Test Strategy & Testing Types

Testing will follow the standard Software Testing Life Cycle (STLC) using black-box techniques such as Equivalence Partitioning and Boundary Value Analysis.
• Smoke Testing. Verify critical paths (site loads, login, add to cart, checkout) immediately after each new build deployment.
• Functional Testing. Validate every feature against the Business Requirement Document (BRD) using positive and negative test data.
• UI / Usability Testing. Check alignment, font consistency, broken images/links, error message clarity, and overall user flow.
• Cross-Browser & Responsive Testing. Verify layout and functionality across desktop and mobile screen resolutions.
• Regression Testing. Re-execute core test cases after bug fixes to ensure existing features remain unbroken.

4. Test Environment & Tools

• Test URL. Staging / QA Environment (https://staging.[yourdomain].com)
• Operating Systems. Windows 11, macOS, Android, iOS
• Browsers. Google Chrome, Mozilla Firefox, Apple Safari, Microsoft Edge (latest stable versions)
• Test Management & Documentation. Excel / Google Sheets (or TestLodge) for Test Cases and Traceability Matrix.
• Defect Tracking. Jira (or Trello / Bugzilla) for logging bugs with screenshots and screen recordings.

5. Entry and Exit Criteria


Phase	Criteria
Entry Criteria	• Requirements (BRD/User Stories) are finalized and approved.
• Staging environment is deployed, stable, and accessible.
• Test data (test user accounts, dummy credit cards, product catalog) is ready.
• Test scenarios and test cases are written and reviewed.
Suspension Criteria	• Critical blocker defects prevent access to core modules (e.g., server crash, broken login, or dead checkout flow).
• Staging environment goes offline or undergoes unscheduled maintenance.
Exit Criteria	• 100% of planned test cases have been executed.
• Pass rate reaches at least 95% with zero Critical or High-severity open defects.
• All medium/low defects are documented and accepted by stakeholders.
• Final Test Summary Report is signed off.


6. Test Schedule & Deliverables


STLC Phase	Estimated Timeline	Key Deliverable
1. Requirement Analysis	Days 1 – 2	Requirement Clarification Log
2. Test Planning	Day 3	Approved Test Plan Document
3. Test Case Design	Days 4 – 7	Test Scenarios, Test Cases, & Requirement Traceability Matrix (RTM)
4. Environment Setup	Day 8	Test Data Sheet & Browser Matrix Verification
5. Test Execution & Bug Reporting	Days 9 – 15	Executed Test Logs & Defect Reports
6. Regression & Closure	Days 16 – 18	Final Test Summary Report & Sign-Off


7. Risks & Mitigation

• Payment Gateway Sandbox Downtime. Third-party test servers may intermittently fail. Mitigation: Maintain mock payment bypass flags in staging and test gateway flows early.
• Late Requirement Changes. Last-minute UI or pricing rule tweaks can delay testing. Mitigation: Freeze scope before Cycle 2 execution and prioritize high-risk modules.
• Incomplete Test Data. Missing edge-case products (e.g., out-of-stock or discounted items). Mitigation: Create dedicated admin test accounts to generate custom product states on demand.
