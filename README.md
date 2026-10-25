# CS 305: Software Security

Andrew Mendoza

## Portfolio artifact

Selected artifact: Artemis Financial Vulnerability Assessment Report (Project One). The report file still needs to be uploaded to this repository. Its exact dependency-scan findings must be verified against the generated local Dependency-Check report before final submission.

## 1. Client and software requirements

Artemis Financial is a financial consulting company that develops individualized plans for savings, retirement, investments, and insurance. The company wanted to modernize its RESTful application while protecting sensitive financial and personal information. My assessment focused on weaknesses in the supplied Java and Spring Boot application, including communication security, access controls, input validation, credentials, error handling, and third-party dependencies.

## 2. Identifying vulnerabilities and the value of secure coding

I did well connecting findings to specific source files and explaining both the risk and a practical mitigation. For example, my manual review identified hard-coded database credentials, missing visible authentication and authorization controls, unvalidated request parameters, and incomplete HTTPS configuration. I also distinguished potential risks from confirmed exploitability instead of assuming every concern was an established exploit. Secure coding matters because it helps protect customer information, prevent unauthorized changes, and maintain reliable services. For a company like Artemis Financial, these practices support customer trust and reduce avoidable operational and financial risk.

## 3. Challenging and helpful parts of the assessment

A challenging part was separating issues visible in the code from dependency findings that require an actual scan and an applicability review. A component version alone is not enough to establish that every associated vulnerability affects the application. The assessment process was helpful because it organized my review into security areas and helped me prioritize findings instead of treating every issue as equally urgent.

## 4. Layers of security and future assessment methods

My Project One mitigation plan proposed defense in depth through HTTPS, authentication, object-level authorization, input validation, parameterized queries, protected credentials, controlled errors, and dependency maintenance. In the Project Two implementation, I prepared SHA-256 checksum verification, HTTPS configuration, environment-based keystore passwords, restricted local binding, and safer error responses. These are prepared controls, not verified deployment results. In future work, I would combine manual review, OWASP Dependency-Check, secret scanning, automated tests, and threat modeling. I would prioritize mitigations using severity, exposure, exploitability, business impact, and the application's actual use of an affected component.

## 5. Functionality, security, and checking refactored code

I prepared positive and negative tests for checksum behavior, including known hash values, repeatability, changed data, and invalid verification inputs. I also documented separate checks for application startup, HTTPS certificate trust, error responses, and dependency findings. However, the available project evidence does not establish that Java compilation, Maven tests, browser TLS verification, or Dependency-Check completed successfully. Before claiming the refactored application is functional and secure, I need to run those checks, review actual results, fix applicable findings, and repeat the tests and scan. Comparing baseline and final dependency reports would help identify newly introduced dependency issues, while manual review and negative tests would address risks a dependency scanner cannot detect.

## 6. Reusable tools, resources, and practices

Useful resources and tools included Java, Spring Boot, Maven, OWASP Dependency-Check, Java Keytool, JDK cryptographic APIs, and the Vulnerability Assessment Process Flow. Practices I can reuse include separating request handling from service logic, explicitly using UTF-8, checking a digest against an independently calculated reference, keeping passwords outside source code, and documenting limitations honestly. Combining code review, automated tests, and dependency analysis gives a more complete assessment than relying on any single tool.

## 7. Demonstrating skills to employers

I would show employers my vulnerability assessment report and its prioritized mitigation plan to demonstrate that I can review an unfamiliar codebase, explain security risks, and connect findings to actionable recommendations. I could also discuss the prepared checksum service, HTTPS configuration, and test design as examples of secure implementation choices. I would distinguish completed analysis and prepared code from runtime validation that still needs evidence. This demonstrates technical communication and an evidence-based approach to software security without overstating the project's readiness.
