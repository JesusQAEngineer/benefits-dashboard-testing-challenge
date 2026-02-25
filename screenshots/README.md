<h1>📸 Manual Testing Evidence</h1>

<h2>📌 Overview</h2>

<p>
This directory contains visual evidence collected during manual validation of the Employees & Benefits module.
</p>

<p>The screenshots demonstrate:</p>

<ul>
  <li>Functional correctness</li>
  <li>Financial calculation accuracy</li>
  <li>CRUD behavior</li>
  <li>Boundary testing</li>
  <li>UI consistency</li>
  <li>Data persistence validation</li>
</ul>

<p>
All images correspond to real execution scenarios validated before automation implementation.
</p>

<hr>

<h2>📁 Folder Structure</h2>

<pre>
screenshots/
│
├── create/
├── edit/
├── delete/
├── boundary-tests/
├── financial-validation/
</pre>

<p>
Each folder represents a specific functional area validated during testing.
</p>

<hr>

<h2>🧪 Test Evidence Breakdown</h2>

<h3>🟢 Create</h3>

<p><strong>Validates:</strong></p>

<ul>
  <li>Employee creation success</li>
  <li>Correct data persistence</li>
  <li>UUID generation</li>
  <li>Dashboard visibility</li>
  <li>Initial financial calculation</li>
</ul>

<p><strong>Example validations captured:</strong></p>

<ul>
  <li>Successful POST response</li>
  <li>Employee visible in dashboard</li>
  <li>Correct net pay calculation after benefits deduction</li>
</ul>

<hr>

<h3>🟡 Edit</h3>

<p><strong>Validates:</strong></p>

<ul>
  <li>Employee information update</li>
  <li>Dependent modification</li>
  <li>Financial recalculation accuracy</li>
  <li>Persistence after update</li>
  <li>UI reflects updated values</li>
</ul>

<p><strong>Example validations captured:</strong></p>

<ul>
  <li>Updated name persists</li>
  <li>Dependents update correctly</li>
  <li>Net pay recalculates based on new benefit cost</li>
</ul>

<hr>

<h3>🔴 Delete</h3>

<p><strong>Validates:</strong></p>

<ul>
  <li>Successful employee removal</li>
  <li>Proper system confirmation</li>
  <li>Record count decrement</li>
  <li>Absence from dashboard</li>
  <li>Negative lookup validation</li>
</ul>

<p><strong>Example validations captured:</strong></p>

<ul>
  <li>DELETE success message</li>
  <li>Employee no longer listed</li>
  <li>404 validation when queried after deletion</li>
</ul>

<hr>

<h3>🔵 Boundary Tests</h3>

<p>
Validates system behavior under edge conditions:
</p>

<ul>
  <li>0 dependents</li>
  <li>1 dependent</li>
  <li>Multiple dependents</li>
  <li>Maximum allowed dependents (32)</li>
  <li>Over-boundary attempt handling (if applicable)</li>
</ul>

<p><strong>Ensures:</strong></p>

<ul>
  <li>No calculation overflow</li>
  <li>No negative financial values</li>
  <li>Proper validation messaging</li>
</ul>

<hr>

<h3>💰 Financial Validation</h3>

<p><strong>Validates business rule integrity:</strong></p>

<p><strong>Assumptions:</strong></p>

<ul>
  <li>$2000 gross per paycheck</li>
  <li>26 paychecks per year</li>
  <li>$1000 yearly cost per employee</li>
  <li>$500 yearly cost per dependent</li>
</ul>

<p><strong>Validated formula:</strong></p>

<pre>
Yearly Benefits = 1000 + (dependents × 500)
Benefits per Paycheck = Yearly Benefits / 26
Net Pay = 2000 - Benefits per Paycheck
</pre>

<p><strong>Screenshots demonstrate:</strong></p>

<ul>
  <li>Correct benefit deductions</li>
  <li>Net pay lower than gross</li>
  <li>Proper decimal handling</li>
  <li>Consistency across CRUD operations</li>
</ul>

<hr>

<h2>🎯 Purpose of This Evidence</h2>

<ul>
  <li>Traceability between manual and automated tests</li>
  <li>Visual proof of system behavior</li>
  <li>Stakeholder reporting</li>
  <li>Audit readiness</li>
  <li>Regression reference baseline</li>
</ul>

<hr>

<h2>🚀 Professional Testing Approach Reflected</h2>

<ul>
  <li>Structured manual validation before automation</li>
  <li>Business rule awareness</li>
  <li>Deterministic data handling</li>
  <li>Validation beyond UI (logic-focused testing)</li>
  <li>Production-level testing discipline</li>
</ul>

<hr>

<h3>Author</h3>

<p>
Jesus Ricardo Hernandez Campos<br>
QA Engineer | API & UI Automation | CI/CD Ready Frameworks
</p>
