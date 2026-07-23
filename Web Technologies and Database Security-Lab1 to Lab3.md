
## COURSE TITLE: Web Technologies and Database Security

## 8 February 2024

---

### INT309: Web Technologies and Database Security - Lab 1: Introduction to
Web Technologies and Understanding HTTP and HTTPS
Introduction
Web Technologies and Database Security encompass the measures and practices used to
protect websites, web applications, and databases from cyber threats, ensuring data
confidentiality, integrity, and availability .
What are Web Technologies: Web security refers to the measures taken to safeguard
websites, web applications, and the underlying infrastructure from various cyber threats,
including data breaches, malware, phishing attacks, and denial - of - service attacks.
Database Security : is a process of ensuring the right policies, measures and practice of used
of database to protect database from unauthorized user or access, misuse, and data breaches
in the data storage
Exercise 1: Creating a Simple Web Page
A web page created using html with file name index.php, the web page contains html
structure such as the title, header that introduces the topic, the paragraph which explains the
content of the website and link for further access external libraries.

---

Reflection :
- Discuss what you learned about the structure of HTML documents. How do elements
such as headers, paragraphs, and links contribute to a web page’s content and usability?
Answer:
The HTML document structures contain both open tags and close tags such as DOCTYPE html,
html lang = “en”, head, body and header.
The header tags have both open and close tags (<header></header>) this is used for housing
the heading in the web page in order to introduce a topic, the design which usually contains h1
to h 6 tags depending on the desired heading front size.
Paragraph in the HTML document is another tag that is represented by tag <p></p>, this
differentiates one paragraph to the other and gives well arrange structure while navigation
through the work.
Links contributed to easy navigating to an external resource for further learning or to accessing a
page. This can be identified as <a></a>

---

Exercise 2: Analyzing HTTP Requests and Responses
Reflection :
- Analyze the significance of each element. Why is it important to understand these
components when developing or securing web applications? Discuss the potential
vulnerabilities associated with improperly handled requests and responses.
Answer :
To analyses each http requests element observed on the developer tool, go network tab, the
request URL is the address of the web page visited which show where the website is secure or
not.
Request Method shows that GET which means the sever was able to request and get index file
from the int309 folder.
Response status code is 200 OK, this means a successful response status code indicates that a
request has succeeded, as this show in the above pictures .
Response Headers contain different such content - type: text/html; charset=UTF - 8 , cache - control
and date : Sat, 05 Apr 2025 11:12:27 GMT .

---

Why is it important to understand these components when developing or securing web
applications? Discuss the potential vulnerabilities associated with improperly handled
requests and responses.
1. Request URL :
- Purpose:
The URL (Uniform Resource Locator) specifies the location of the resource being requested
from the server.
- Importance:
Developers need to understand URLs for routing requests to the correct endpoints, ensuring that
the server can find and serve the requested content.
- Security:
Malformed or malicious URLs can lead to vulnerabilities like path traversal or injection attacks,
making it essential to validate and sanitize URLs.
2. Request Method:
- Purpose:
The request method (e.g., GET, POST, PUT, DELETE) indicates the type of action the client
wants to perform on the resource.
- Importance:
Developers need to use the correct method to ensure the server performs the intended operation,
such as retrieving data (GET), creating a new resource (POST), updating an existing resource
(PUT), or deleting a resource (DELETE).
- Security:
Misusing methods can lead to unintended consequences, such as deleting data when it shouldn't
be deleted or allowing unauthorized access to resources.
3. Response Status Code:
- Purpose:
The status code (e.g., 200 OK, 404 Not Found, 500 Internal Server Error) informs the client
about the outcome of the request.
- Importance:

---

Developers need to understand status codes to handle errors and provide meaningful feedback to
users, such as displaying error messages or redirecting them to a different page.
- Security:
Certain status codes (like 403 Forbidden or 500 Internal Server Error) can indicate security
issues or server problems, requiring developers to investigate and address them.
4. Response Headers:
- Purpose:
Response headers provide additional information about the response, such as the content type,
server information, and catching instructions.
- Importance:
Developers need to understand headers to properly render the response, manage caching , and
enforce security policies.
- Security:
Headers like Content - Security - Policy (CSP) are crucial for preventing XSS (Cross - Site
Scripting) and other security vulnerabilities, while Cache - Control headers help manage caching
and improve performance

---

Exercise 3: Understanding HTTPS and Its Importance
Reflection :
- Discuss the advantages of using HTTPS over HTTP, particularly in terms of data security
and privacy. What protections does HTTPS provide against attacks such as
eavesdropping and man - in - the - middle (MitM)?
HTTPS offers superior data security and privacy compared to HTTP by encrypting data
transmission, preventing eavesdropping and ensuring data integrity, while HTTP transmits data
in plain text, making it vulnerable to interception and manipulatio n.

---

Encryption: HTTPS uses encryption (typically TLS/SSL) to scramble data during transmission,
making it unreadable to anyone who intercepts the data, even if they have the tools to sniff
network traffic.
Protection against eavesdropping: With HTTP, data is sent in plain text, which means anyone
with the right tools can easily read the information being transmitted. HTTPS prevents this by
encrypting the data.
Protection against man - in - the - middle attacks: A man - in - the - middle attack occurs when an
attacker intercepts communication between a client and a server. HTTPS helps prevent this by
verifying the identity of the server and encrypting the communicati on.
A padlock icon shows on the https address which indicates secure web address and safe to visit,
when click on this, it allows to view security certificates of such website, the encryption method,
date of registration, expiring date and issuer. As shown bel ow.

---

---

### INT309: Web Technologies and Database Security – Lab 2: Web Development
### Components and Security Threats.
Exercise 1: Exploring Front - End Development Components
1. Identify Front - End Technologies:
- Research and create a list of common front - end technologies used in web
development, including:
▪ HTML
▪ CSS
▪ JavaScript
▪ Front - end frameworks (e.g., React, Angular, Vue.js)
2. Create a Simple Front - End Application:
- Build a basic web application using HTML, CSS, and JavaScript that includes:
▪ A header with a navigation menu.
▪ A form for user input (e.g., contact form).
▪ Interactive elements (e.g., a button that changes the text when clicked).

---

Reflection :
- Discuss how front - end technologies interact to create a cohesive user experience. What
potential security issues arise from poorly implemented front - end code (e.g., XSS,
CSRF)?
Front end technologies are an interface a user can interact with while making use of web pages
and this will enhance the user experience if the design is good and user friendly.
- HTML : this is skeleton structure of web design; it is used for content write up
and define element of web page.
- CSS : it is used as a style website for attractive user interface
- JavaScript : this is used for interactive and to build a responsive website.
- Front - end frameworks (e.g., React, Angular, Vue.js ) : these are frame that already
contains inbuilt html, css and Javascript and its easy for building a website .
Security Issues from Poorly Implemented Front - End Code
Potential security issues may arise due to poor implementation of front - end code such as
improper sanitization of user input in JavaScript code , this can cause problems such as cross
site script (XSS) and Cross - Site Request Forgery (CSRF) .
- C ross site script (XSS) : where a malicious actor inject malicious script into website or
stores it in the vulnerable code which are then executed by other users browsers,
potentially compromising their data or action . If a website is not properly implemented it
can also lead to CSRF where an attacker crafts a malicious website or clicks the link,

---

their browser automatically includes their authentication cookies (or other session data)
with the request to the target website.
- Cross - Site Request Forgery (CSRF) : Exploits user sessions to execute unauthorized
actions on trusted websites.
- Clickjacking: Embeds a malicious site within an invisible frame, tricking users into
unintended actions.
- Insecure JavaScript Libraries: Using outdated or vulnerable libraries can expose
websites to attacks.
Mitigation Strategies: Implement Content Security Policy (CSP), input validation, secure
authentication, and regular updates to prevent these threats.
Exercise 2: Understanding Back - End Development Components
1. Identify Back - End Technologies:
- Programming Languages: PHP, Python, Java, Node.js, Ruby
- Databases: MySQL, PostgreSQL, MongoDB, SQLite
- Web Frameworks: Django (Python), Express.js (Node.js), Laravel (PHP), Spring Boot
(Java)
Create a Simple Back - End Application :
- Using a chosen back - end technology, set up a basic server that responds to HTTP
requests. For example, using Node.js:

---

Reflection :
- Analyze the role of back - end components in web applications. How do vulnerabilities in
the back - end (e.g., SQL injection, insecure APIs) affect overall application security?
Ans
Back - end components are the foundation of web applications, handling data storage, processing,
and core functionalities, so vulnerabilities in these areas can lead to severe security breaches,
including data theft, unauthorized access, and system manipulat ion.
Role of Back - End Components:
- Data Storage and Management:
Back - end systems, including databases, store and manage sensitive user data, financial
information, and other critical data.
- Application Logic and Functionality:
The back - end executes the core logic of the application, handling user requests, processing data,
and interacting with external services.
- Authentication and Authorization:
Back - end systems are responsible for verifying user identities and controlling access to
resources, ensuring only authorized users can access sensitive information.
- API Management:

---

Back - end components often expose APIs, which are the interfaces that allow different
applications to communicate and exchange data.
Vulnerabilities and Their Impact:
- SQL Injection:
A common vulnerability that allows attackers to manipulate database queries, potentially gaining
unauthorized access to data, modifying data, or even gaining control of the database server.
- Insecure APIs:
APIs that lack proper authentication, authorization, or input validation can be exploited by
attackers to gain unauthorized access to data or functionalities.
- Cross - Site Scripting (XSS):
An attacker can inject malicious scripts into a web application, allowing them to steal user data,
redirect users to malicious sites, or compromise the user's session.
- Cross - Site Request Forgery (CSRF):
An attacker can trick a user into performing actions on a web application without their
knowledge, such as making unauthorized changes to their account or data.
- Broken Authentication and Authorization:
Weak authentication mechanisms or insufficient authorization controls can allow attackers to
bypass security measures and gain unauthorized access to sensitive data or functionalities.
- Data Breaches:
Compromised back - end systems can lead to data breaches, where sensitive information is stolen
and exposed to unauthorized parties.
- Unauthorized Access:
Vulnerabilities can allow attackers to gain unauthorized access to the application, database, or
underlying server.
- System Manipulation:
Attackers can exploit vulnerabilities to manipulate the application's functionality, potentially
causing disruptions or even taking control of the system.
- Financial Loss:

---

Data breaches and system compromises can lead to significant financial losses for businesses,
including costs associated with remediation, legal fees, and reputational damage.
- Reputational Damage:
Security breaches can severely damage a company's reputation, leading to loss of customer trust
and potential business losses.
Exercise 3: Identifying Security Threats
- Research Common Security Threats :
- Investigate the OWASP Top Ten list and identify at least five common security threats in
web development. Focus on:
o SQL Injection
o Cross - Site Scripting (XSS)
o Cross - Site Request Forgery (CSRF)
o Security Misconfiguration
o Insecure Deserialization

---

Reflection:
o Discuss the impact of these security threats on user data and application integrity.
What measures can developers implement to mitigate these risks?
Impact of Security Threats & Mitigation Strategies SQL Injection (SQLi)
Impact:
- Attackers can bypass authentication and gain unauthorized access.
- User data leakage, leading to identity theft.
- Attackers can delete, modify, or steal entire databases.
- Some SQLi attacks enable remote code execution, allowing full system control.
Mitigation Strategies:
✔ Use Prepared Statements (Parameterized Queries) to prevent injection.
✔ Use Web Application Firewalls (WAFs) to filter malicious requests.
✔ Limit database permissions for application users (least privilege).
✔ Sanitize and validate user input before processing it.
Cross - Site Scripting (XSS)
Impact:
- Attackers inject malicious JavaScript into web pages.
- Can steal cookies, session tokens, and login credentials.
- Redirect users to phishing sites or deface the website.
- Can spread malware through user interactions.
Mitigation Strategies:
✔ Escape user input to prevent JavaScript execution.
✔ Use Content Security Policy (CSP) to restrict script execution.

---

✔ Sanitize input fields to allow only safe characters.
✔ Implement HTTP - only and Secure cookies to prevent cookie theft.
Cross - Site Request Forgery (CSRF)
Impact:
- Attackers trick users into executing unwanted actions on their accounts.
- Can lead to unauthorized fund transfers, password changes, or account deletion.
- Exploits users who are already logged in to the target application.
Mitigation Strategies:
✔ Use CSRF tokens to verify request authenticity.
✔ Enforce SameSite cookie attributes to restrict cross - site requests.
✔ Implement Multi - Factor Authentication (MFA) for critical actions.
✔ Use Referrer and Origin headers to validate requests.
Security Misconfiguration
Impact:
- Default credentials (e.g., admin/admin) expose sensitive data.
- Excessive permissions can lead to privilege escalation.
- Unnecessary features or debug modes increase attack surface.
- Insecure error messages reveal system details to attackers.
Mitigation Strategies:
✔ Disable default accounts and change default passwords.
✔ Use the principle of least privilege for permissions.
✔ Regularly update and patch software to fix vulnerabilities.
✔ Disable unnecessary services and features in production.

---

Insecure Deserialization
Impact:
- Attackers can manipulate serialized objects to execute malicious code.
- Can lead to remote code execution (RCE) and system compromise.
- Can be used to elevate privileges or tamper with application data.
Mitigation Strategies:
✔ Avoid using serialized objects from untrusted sources.
✔ Use digital signatures to verify object integrity.
✔ Implement strong input validation before deserializing data.
✔ Use safer data formats like JSON instead of serialized objects.
Conclusion
Security threats like SQLi, XSS, CSRF, Security Misconfigurations, and Insecure
Deserialization can compromise user data, application integrity, and system security.
Developers should implement secure coding practices, input validation, least privileged
principles, and security headers to mitigate these risks.
INT309: Web Technologies and Database Security – Lab 3: Introduction to Databases
and SQL
Definition: SQL stands for Structured Query Language, SQL is a standard language for storing,
manipulating and retrieving data in databases
Exercise 1: Setting Up MySQL with XAMPP
Install and Run XAMPP :
- If you haven’t already, download and install XAMPP from
https://www.apachefriends.org/ .
- Launch XAMPP and start the Apache and MySQL services from the XAMPP Control
Panel.
Access phpMyAdmin :

---

- Open your web browser and navigate to http://localhost/phpmyadmin/.
- phpMyAdmin is a web - based tool provided by XAMPP for managing MySQL databases
Create a New Database :
- In phpMyAdmin, click on the Databases tab.
- Enter the name student_management_system for your new database and click Create .
- This database will store information about students, courses, and enrollments.

---

Reflection :
- Explain why a web application like a Student Management System would need a
relational database. What are the benefits of using MySQL in such applications?
ANSWER
Databases are essential for the role it play when come to data storage in web application such as
student Management system, In the school environment the administration need to save student
data e.g. student results, Bio data, Matric No, Blood - group etc. for easy access when all ocate a
student. And it is easy to navigate and query table for editing and deleting data.
Benefits of MySQL in such Applications are:
- Manipulation of data: it can be used to add, delete and edit data from database.
- Store data: it can be used to store and qu e ry table from database
- retrieving data in databases : it can be used to recall data and search for any data on the
database
Exercise 2: Creating Tables and Defining Columns
Create a students Table :
- After creating the database, click on the student_management_system database.
- Create a new table named students with the following columns:
o student_id (INT, Primary Key, Auto Increment)
o first_name (VARCHAR(50))
o last_name (VARCHAR(50))
o email (VARCHAR(100), Unique)
o date_of_birth (DATE)
- Click Save to create the table.

---

Create a courses Table :
- Create a second table named courses with the following columns:
o course_id (INT, Primary Key, Auto Increment)
o course_name ( VARCHAR ( 100))
o credits (INT)
- Click Save .
Create an enrollments Table (Relationship Between Students and Courses):
- Create a third table named enrollments to track which students are enrolled in which
courses. This table should have the following columns:
o enrollment_id (INT, Primary Key, Auto Increment)
o student_id (INT, Foreign Key referencing students.student_id)
o course_id (INT, Foreign Key referencing courses.course_id)
o enrollment_date (DATE)
- Click Save to complete the table creation.

---

Reflection :
- Discuss how relationships are established between tables in a relational database. Why
are foreign keys important in maintaining data integrity?
ANS
The relationship was established between tables using primary key , the primary key is unique
identification that is common between two tables or more.
Foreign keys is important in maintaining data integrity , ensuring that the data link to the right
owner of the data, for instance in the above table created student_id and course_id are foreign
key that link the three table together and ensuring it link to the rightful owner of date in order to
maintain data i ntegrity without mix up the data.
Exercise 3: Inserting Data into the Tables
Insert Sample Data into the students Table :
- Open the SQL tab in phpMyAdmin and execute the following SQL statement to insert
some students:
- INSERT INTO students (first_name, last_name, email, date_of_birth)
- VALUES
- ('John', 'Doe', 'john.doe@example.com', '1995 - 04 - 12'),
- ('Jane', 'Smith', 'jane.smith@example.com', '1998 - 09 - 05'),
- ('Tom', 'Brown', 'tom.brown@example.com', '1997 - 11 - 22' ).

---

Insert Sample Data into the courses Table :
- Insert some sample courses using the following SQL statement:
- INSERT INTO courses (course_name, credits)
- VALUES
- ('Introduction to Databases', 3),
- ('Web Development', 4),
- ('Cybersecurity Fundamentals', 3 ).
Insert Sample Data into the enrollments Table :
- Enroll the students into different courses using this SQL statement:
- INSERT INTO enrollments (student_id, course_id, enrollment_date)
- VALUES
- (1, 1, '2024 - 01 - 15'),
- (2, 2, '2024 - 01 - 17'),
- (3, 3, '2024 - 01 - 19'),
- (1, 2, '2024 - 01 - 20' ).

---

Reflection :
o Explain how inserting data into tables allows the database to become useful for
managing information. Why is data consistency crucial when inserting related
data across tables?
ANS
Inserting data into table allows databases to become useful for managing information because the
data will be arranged in such a way that it will be easy to query while searching for information
and provide unique identification for each data on the database.
Why is data consistency crucial when inserting related data across tables?
Data consistency is important to match one table to other related table if there is not consistency
while inserting data there will mixed up while query the data or missed data.
Exercise 4: Querying the Database
Retrieve All Students :
- Use a SQL query to retrieve all records from the student’s table:
SELECT * FROM students.
Retrieve Students Enrolled in a Specific Course :
- Write a SQL query to retrieve students enrolled in "Web Development":
- SELECT s.first_name, s.last_name, c.course_name
- FROM students s

---

- JOIN enrollments e ON s.student_id = e.student_id
- JOIN courses c ON e.course_id = c.course_id
WHERE c.course_name = 'Web Development'

---

Update a Student’s Email Address :
- Update the email address for John Doe using the following SQL statement:
- UPDATE students
- SET email = 'john.newemail@example.com'
WHERE first_name = 'John' AND last_name = 'Doe';
Delete an Enrollment Record :
- Delete the enrollment record for Jane Smith from the enrollments table:
- DELETE FROM enrollments
WHERE student_id = 2 AND course_id = 2;
Reflection :
o Discuss how SQL allows you to query and manipulate data in a relational
database. How do JOINs facilitate retrieving related information from multiple
tables?
ANS
SQL allows us to manipulate and query data in the database by using primary key or foreign key,
which is common identity that relates two or more table together, the relational database can also
be query by using SQL structure statement such as WHERE, FROM, SELECT, JOIN, AND, OR
etc.

---

JOIN s facilitate retrieve of related data by checking the relationship between two tables . This
can be done in different ways such as:
INNER JOIN : this will join only what common or overlap to the two table
OUTER JOIN: this will join what is not common to the two tables
FULL JOIN: this will join two tables irrespective of what common to bot.
LEFT AND RIGHT JOIN: this will only consider the left table and right will consider only the
right table to join the table.
