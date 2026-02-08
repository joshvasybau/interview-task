Interview Task
 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
</head>

<body>

<h1>Config-Driven Access Control System (RBAC)</h1>

<h2>Objective</h2>
<p>
Build a full-stack application that demonstrates
<strong>Role-Based Access Control (RBAC)</strong> with
<strong>table-level</strong> and <strong>field-level</strong> permissions,
managed dynamically by an <strong>Admin user</strong>.
</p>

<p>
Permissions are stored as configuration in the database and enforced
at the backend without hardcoding access rules.
</p>

<h2>Project Overview</h2>
<p>
This project is a config-driven RBAC banking management system developed
using <strong>Go (Golang)</strong>, <strong>MySQL</strong>, and
<strong>HTML/CSS/JavaScript</strong>.
</p>

<p>
It simulates a real-world banking environment where access to accounts,
transactions, and customer data depends on user roles and permissions.
</p>

<div class="note">
<strong>Important:</strong><br>
After downloading the project from GitHub, please extract the ZIP file
before running the application.
</div>

<h2>Role &amp; Permission Model</h2>

<h3>Roles Implemented</h3>
<ul>
  <li><strong>Admin</strong> – Full access, manages users, roles, and permissions</li>
  <li><strong>Manager</strong> – View access to customers and accounts</li>
  <li><strong>Cashier</strong> – View and edit account balances</li>
  <li><strong>Support</strong> – Read-only customer access</li>
  <li><strong>Auditor</strong> – Read-only transaction access</li>
</ul>

<h3>Permission Configuration</h3>
<p>
Permissions are stored in the database in JSON format and define:
</p>
<ul>
  <li>Table-level access (view / edit)</li>
  <li>Field-level access (view / edit per column)</li>
</ul>

<p>
All authorization checks are enforced at the backend.
Unauthorized access returns HTTP 403.
</p>

<h2>Steps to Run the Project</h2>

<h3>1. Extract the Project</h3>
<p>
Download the ZIP file from GitHub and extract it to a local directory.
</p>

<h3>2. Backend Setup</h3>
<ul>
  <li>Ensure Go and MySQL are installed</li>
  <li>Create a MySQL database</li>
  <li>Import required tables:
    <ul>
      <li>users</li>
      <li>roles</li>
      <li>permissions</li>
      <li>customers</li>
      <li>accounts</li>
      <li>transactions</li>
    </ul>
  </li>
  <li>Update database credentials in <code>db/mysql.go</code></li>
</ul>

<pre>go run main.go</pre>

<p>
The server will start at:
</p>

<pre>http://localhost:8080</pre>

<h3>3. Frontend</h3>
<p>
The frontend is served automatically by the Go backend.
Open the application in a browser using the same URL.
</p>

<h2>Sample Login Credentials</h2>

<h3>Admin</h3>
<pre>
Username: admin_boss
Password: admin123
</pre>

<h3>Manager</h3>
<pre>
Username: manager1
Password: manager123
</pre>

<h3>Cashier</h3>
<pre>
Username: cashier1
Password: cashier123
</pre>

<h3>Support</h3>
<pre>
Username: support1
Password: support123
</pre>

<h3>Auditor</h3>
<pre>
Username: auditor1
Password: auditor123
</pre>

<h2>Technologies Used</h2>
<ul>
  <li>Go (Golang)</li>
  <li>MySQL</li>
  <li>HTML, CSS, JavaScript</li>
  <li>REST APIs</li>
</ul>
<h2>sql query file</h2>
<p>
use the sql text file if needed to create sql data base
</p>
</body>
</html>
