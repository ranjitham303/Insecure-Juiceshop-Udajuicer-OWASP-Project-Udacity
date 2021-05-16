# Insecure Juice Shop & Vulnerability Report
Insecure Juice shop
#Section 1: Threat Assessment
It’s time to get to work! You’ve arrived at one Udajuicer’s headquarters located in Miami and are shocked at the lack of technology. You ponder how in the world is this the largest juice shop without ever using computers or relying on technology. After the initial shock, you’re ready to get back on track and get to work. Manu, the eccentric owner, takes it upon himself to work with you directly to make sure you have everything you need. You first request an architecture diagram of the application and logs from right before the application went down. At a quick glance you notice the woefully designed architecture and buckle up for a long day, all the whilst Manu is in your ear talking about Super Smoothies evil plot to take down his franchise.

Part 1: Asset Inventory
The first part of our threat model is being able to identify all the assets involved in the target of the assessment. What does Udajuicer have of value? Looking at the architecture diagram, identify all the components that make up Udajuicer and document them in the assessment scope of your report. After identifying all the parts, explain the function of each part and how a request goes from the client to the server.

Part 2: Architecture Audit
Now that we’ve identified all the components that makeup Udajuicer, let’s conduct an architecture review with the given diagram. Referencing what we went over secure architecture best practices, list out at least 3 flaws.

Part 3: Threat Model
Build a Threat Model Diagram showing the flow of data using OWASP Threat Dragon. Identify at least 3 possible threats that would pose a threat to your web application. Think of the OWASP Top 10.

Part 4: Threat Analysis
We’ve now identified a few insecurities in Udajuicer’s architecture and want to use this knowledge to help us identify what was causing Udajuicer's website to crash. When in doubt, investigating logs should point us in the right direction. Analyze the log file on the desktop to identify what type of attack took down the Juice Shop.

Part 5: Threat Actor Analysis
The final part of our assessment consists of us trying to identify who would possibly want to take down the Juice Shop? Below are possible threat actors that we’ve covered in our course. Select who you think would most likely be responsible for the attack and explain why.

Organized Crime
APT Groups
State-Sponsored Attack
Insider Threat
Hacktivist
Script Kiddie

Section 2: Vulnerability Analysis
You’ve made it past the initial assessment and still have your sanity as working with Manu can be exhausting. You’ve identified the initial attack and shortcomings of the application setup. Manu is currently fuming with anger at the ineptness of both his business team and Chad whom they hired. Treading lightly, you notify him you have to continue with a deeper analysis of the application to see if you can find more vulnerabilities. Petrified Manu retreats into the corner awaiting the news of your probe.

Task 1: SQL Injection
The first vulnerability we want to exploit is on the login page of the website. Navigate to the login page and you should see a username and password field. Unfortunately for Juice Shop, this login portal is subjectable to a SQL Injection attack! Just as we covered during the course, exploit the vulnerability, and gain access to the site as admin.

Take a screenshot of:

The commands you used
Account settings showing you as admin
Task 2: XSS
The second vulnerability we want to exploit is after we’ve logged into the site. We want to exploit an XSS vulnerability in the search bar. Attempt an arbitrary command that will render an alert with the value “Hacked”.

Take a screenshot of:

Both of the commands you used
The message box displaying “Hacked”
Optional Stand Out Task:
See if you can identify other vulnerabilities in the Juice Shop!

Section 3: Risk Analysis
After notifying Manu of two more vulnerabilities, his technophobia is in full display. You reassure him that these problems can be resolved but the next step is to rank the risks in order of what should be dealt with first.

Task 1: Scoring Risks
Use the matrix in the Threat Model Report to score the risks that we’ve identified so far to the Juice Shop. Make sure to edit the matrix to include the name of the attack we identified in 1.3. Threats:

Name of Attack Identified in 1.3
Insecure Architecture
SQl Injection Vulnerability
XSS Vulnerability
Task 2: Risk Rationale
Now that we’ve scored all our risks, explain why you chose to rank the risks in the way you did. This rationale and ranking shows where Udajuicer’s resources should be allocated first as opposed to trying to tackle everything at once.

Section 4: Mitigation Plan
At this point we’ve broken down all the risks and in what order Udajuicer should mitigate them. Unsure and still broken Manu asks you how to resolve them. You assure him that you’ll build out the mitigation and get Udajuicer back up and running! Manu’s faith in you getting the job done is all that’s holding his technophobia in check.

Task 1: Secure Architecture
Use draw.io to design a far more secure architecture for Manu to implement in getting the Juice Shop back up and running. Make sure to fix any faults we identified prior in our initial assessment.

Task 2: Mystery Attack Mitigation
Now we want to tackle his most pressing issue and want to implement a solution to mitigate the attack you identified in 1.3. We’ve covered a few different strategies on how to prevent these types of attacks in this course, choose one or more of the methods we’ve covered in the course and describe how implementing it would prevent further attacks of this type.

Task 3: SQL Injection Mitigation
The next issue we want to fix is the SQL injection vulnerability on his login page. We’ve covered a few different strategies on how to prevent SQL Injections attacks, choose one or more of the methods we’ve covered in the course and describe how implementing it would prevent further Injection attacks.

Task 4: XSS Mitigation
The last issue we want to fix is the XSS vulnerability. We’ve covered a few different strategies on how to prevent XSS attacks, choose one or more of the methods we’ve covered in the course and describe how implementing it would prevent further XSS attacks.





Vulnerability Report
Project Instructions
Your task is to complete a vulnerability assessment according to your organization’s Vulnerable Assessment standards using a provided report template. Your report will be consumed by leadership of the Development Team, as well as practitioners. It is important to note that the report must account for audiences of multiple technical levels, including management, supervisors, and practitioners. Generally speaking, the first section of the report is a summary appropriate for management. As the report continues, it becomes more technical, with the final sections intended for the Development Team, who will be responsible for remediation efforts.

Your organization has a report template that standardizes all vulnerability assessment and analysis, which is available here.

Your vulnerability report must contain the following sections:

Report Title/Cover Page
Table of Contents
Engagement Overview
Discussion of who requested the assessment and what the initial request was.
Discussion of appropriate assessment scope.
Scope
Given the information provided by the Development Team, determine the appropriate scope of the vulnerability assessment.
Explain how the scope was determined.
If necessary, explain any considerations of the project that are considered out-of-scope and why.
Risk Analysis
Provide a high-level risk assessment of the overall assessed risk. Provide an explanation of why this risk-level was reported. (High | Medium | Low)
In Layman’s terms, explain what vulnerabilities caused the overall rated risk.
Recommendation
Provide general guidance for the Development Team to correct, mitigate, or resolve the assessed highest risk vulnerabilities.
Vulnerability Summary
Provide a list of the significant assessed vulnerabilities listed in order of descending risk.
Vulnerability Detail
For each significant assessed vulnerability, provide additional information.
Include the vulnerability name (and CVE if applicable).
Include an explanation of how the vulnerability was identified and validated.
Include an explanation of the vulnerabilities' probability of exploit.
Include a short proof-of-validation of the vulnerability (typically a screenshot or log excerpt, etc.).
Analysis Methodology
The methodology section should be a scientific methodology that would allow another analyst to replay your actions to arrive at the same conclusions about the overall risk.
Include how the application was initially accessed and include a validation the defined scope is appropriate for the assessment.
Include a list of tools that will be used during the vulnerability assessment.
Explain in logical (usually chronological) order the actions that were taken to perform the vulnerability assessment.
Include screenshots of the vulnerability assessment process, tools, and actions made during the vulnerability validation.
Project Rubric
While the starter template should lead you to a proper submission, make sure to double check your work against the project rubric requirements.
Additional Information regarding OWASP Juice Shop
The web-application is an Open Source MIT licensed intentionally vulnerable web application designed to challenge and instruct those interested in web-application testing. The application includes a Capture-the-flag component and a scoring system, however it is not necessary to complete the capture-the-flag component or achieve a certain score for this project.

Your task in this project is to complete a vulnerability assessment of the application. You may choose to complete the capture-the-flag component of the application as an additional learning opportunity after the vulnerability assessment project is completed.
