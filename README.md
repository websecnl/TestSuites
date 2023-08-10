# Test Suites and Test Cases
AttackForge helps you to track your security testing performed on any assessment or project.
This is achieved using Test Cases which are assigned to a project, and can be further assigned to individual testers and/or scope assets.

Every Test Case on the project can help to guide you on what needs to be tested, how it should be tested, and help you to store and capture testing evidence and artefacts.

A Test Suite is made up of a collection of Test Cases which are relevent to the Test Suite.

For example, a Test Suite might be "Web Application Pentest" and a Test Case on this Test Suite might be "Verify that request throttling is in place to prevent automated attacks against common authentication attacks such as brute force attacks or denial of service attacks."

AttackForge already comes pre-loaded with many Test Suites from industry methodologies such as OWASP, OSSTMM, NIST and more.

This repository provides additional industry methodologies you can import into your AttackForge tenant.
The following methodologies are supported:

- OWASP Application Security Verification Standard (ASVS) Version 4 - Level 1
- OWASP Application Security Verification Standard (ASVS) Version 4 - Level 2
- OWASP Application Security Verification Standard (ASVS) Version 4 - Level 3
- OWASP Mobile Application Security Testing Guide (MASTG) Version 2 - Level 1
- OWASP Mobile Application Security Testing Guide (MASTG) Version 2 - Level 2
- OSSTMM Version 3 - Human Security Testing
- OSSTMM Version 3 - Physical Security Testing
- OSSTMM Version 3 - Wireless Security Testing
- OSSTMM Version 3 - Telecommuncations Security Testing
- OSSTMM Version 3 - Data Networks Security Testing

You can load additional testing methodologies in the form of Test Cases which can be imported on your Test Suites using the [AttackForge Self-Service API](https://support.attackforge.com/attackforge-enterprise/modules/self-service-restful-api/addtestcasestotestsuite).

The following cURL example will import the OWASP ASVS v4 Level 1 Test Cases included in this repository to an existing Test Suite:

```
curl --request POST --url https://<YOUR-ATTACKFORGE-TENANT>/api/ss/testsuite/<TESTSUITE-ID>/testcases --header 'content-type: application/json' --header 'x-ssapi-key: <YOUR-API-KEY>' --data @owasp_asvs_level_1.json
```
