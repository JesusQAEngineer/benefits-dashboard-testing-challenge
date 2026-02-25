📘 Automation Plan

📌 Overview



This document defines the automation strategy implemented for the Employees \& Benefits module.



The objective of this plan is to ensure:



Deterministic execution



Business rule validation



Full CRUD coverage



Financial calculation accuracy



CI/CD readiness



Scalable framework structure



This plan supports both API Automation (Postman/Newman) and UI validation alignment.



🎯 Automation Objectives



The automation framework validates that an employer can:



Create employees



Calculate benefit costs correctly



Update employee information



Delete employees



See accurate financial data reflected in the system



Beyond endpoint validation, the automation verifies business logic correctness.



🏗 Strategy Design Principles



The automation was designed to be:



Deterministic (repeatable results)



Independent (tests do not depend on previous executions)



Self-contained



Free of hardcoded IDs



CLI executable



Pipeline-ready



Business-logic aware



🔁 CRUD Automation Flow

Execution Sequence



POST – Create Employee



GET by ID – Validate persistence



GET All – Validate dashboard visibility



PUT – Update employee



GET by ID – Validate update persistence



DELETE – Remove employee



GET by ID (Negative) – Confirm deletion



GET All – Validate record count decrement



This ensures:



Full lifecycle validation



Data integrity verification



Clean test execution



💰 Business Logic Validation Strategy

Financial Rules Validated



$2000 gross per paycheck



26 paychecks per year



$1000 annual employee benefit cost



$500 annual cost per dependent



Validated Formula

Yearly Benefits = 1000 + (dependents × 500)

Benefits per Paycheck = Yearly Benefits / 26

Net Pay = 2000 - Benefits per Paycheck

Automation Validates



Correct gross value



Accurate benefit calculation



Net pay lower than gross



No negative values



Decimal tolerance handling



🧪 Test Coverage Areas

✅ Functional Coverage



Employee creation



Data persistence



Record retrieval



Record updates



Record deletion



✅ Negative Coverage



Validation after deletion (404 expected)



Boundary dependent validation



Data integrity enforcement



✅ Boundary Testing



0 dependents



1 dependent



Multiple dependents



Maximum allowed dependents (32)



🔍 Technical Implementation Details



Dynamic UUID capture



Collection variable management



No hardcoded test data



Status code validation (200, 201, 404)



Response schema validation



Ownership validation



Error-resilient JSON parsing



Deterministic data flow



🛠 Tooling



Postman



Newman



newman-reporter-htmlextra



Node.js



⚙️ Execution Strategy

CLI Execution

newman run Benefits\_Automation.postman\_collection.json

With HTML Report

newman run Benefits\_Automation.postman\_collection.json \\

-r htmlextra \\

--reporter-htmlextra-export report.html

This Supports:



Local execution



Pipeline execution



Version-controlled validation



Automated reporting



🚀 CI/CD Readiness



The framework is structured for:



GitHub Actions integration



Automated pipeline runs



Report artifact generation



Deterministic execution in shared environments



No manual intervention required.



📈 Professional Approach Reflected



This automation plan demonstrates:



Business-rule-driven validation



Production-level API automation design



Clean data management



Test reliability discipline



Pipeline-oriented thinking



Prevention of false positives



👤 Author



Jesus Ricardo Hernandez Campos

QA Engineer | API \& UI Automation | CI/CD Ready Frameworks

