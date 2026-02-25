📸 Manual Testing Evidence


📌 Overview



This directory contains visual evidence collected during manual validation of the Employees \& Benefits module.



The screenshots demonstrate:

Functional correctness

Financial calculation accuracy

CRUD behavior

Boundary testing

UI consistency

Data persistence validation

All images correspond to real execution scenarios validated before automation implementation.



📁 Folder Structure
screenshots/
│
├── create/
├── edit/
├── delete/
├── boundary-tests/
├── financial-validation/

Each folder represents a specific functional area validated during testing.



🧪 Test Evidence Breakdown


🟢 Create



Validates:

Employee creation success

Correct data persistence

UUID generation

Dashboard visibility

Initial financial calculation

Example validations captured:

Successful POST response

Employee visible in dashboard

Correct net pay calculation after benefits deduction



🟡 Edit



Validates:

Employee information update

Dependent modification

Financial recalculation accuracy

Persistence after update

UI reflects updated values

Example validations captured:

Updated name persists

Dependents update correctly

Net pay recalculates based on new benefit cost



🔴 Delete



Validates:

Successful employee removal

Proper system confirmation

Record count decrement

Absence from dashboard

Negative lookup validation

Example validations captured:

DELETE success message

Employee no longer listed

404 validation when queried after deletion



🔵 Boundary Tests



Validates system behavior under edge conditions:

0 dependents

1 dependent

Multiple dependents

Maximum allowed dependents (32)

Over-boundary attempt handling (if applicable)

Ensures:

No calculation overflow

No negative financial values

Proper validation messaging



💰 Financial Validation



Validates business rule integrity:

Assumptions:

$2000 gross per paycheck

26 paychecks per year

$1000 yearly cost per employee

$500 yearly cost per dependent

Validated formula:

Yearly Benefits = 1000 + (dependents × 500)
Benefits per Paycheck = Yearly Benefits / 26
Net Pay = 2000 - Benefits per Paycheck





Screenshots demonstrate:

Correct benefit deductions

Net pay lower than gross

Proper decimal handling

Consistency across CRUD operations





🎯 Purpose of This Evidence



This directory supports:

Traceability between manual and automated tests

Visual proof of system behavior

Stakeholder reporting

Audit readiness

Regression reference baseline





🚀 Professional Testing Approach Reflected

This evidence demonstrates:

Structured manual validation before automation

Business rule awareness

Deterministic data handling

Validation beyond UI (logic-focused testing)

Production-level testing discipline





Author:
Jesus Ricardo Hernandez Campos
QA Engineer | API \& UI Automation | CI/CD Ready Frameworks



