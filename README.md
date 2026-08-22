# CS 305: Software Security

## Artemis Financial – Practices for Secure Software

### Portfolio Artifact

For this portfolio, I selected my **Artemis Financial Practices for Secure Software Report** from Project Two. This project demonstrates my ability to identify software security concerns, refactor an application using secure coding practices, implement encryption and hashing technologies, configure secure communications, and test an application for vulnerabilities.

## Client and Software Requirements

The client for this project was **Artemis Financial**. The company needed improvements to the security of its software application so that sensitive information could be handled more securely. The application needed stronger protections for confidentiality, integrity, and authentication.

To address these requirements, I implemented modern security practices such as SHA-256 hashing for integrity verification, HTTPS using TLS 1.2 and TLS 1.3 for secure communication, and certificate-based authentication. I also generated and configured a development certificate and reviewed the application's dependencies for known security vulnerabilities.

## Identifying Software Security Vulnerabilities

One area I did well was evaluating the application from several different security perspectives instead of relying on only one type of test. I reviewed the source code and configuration, tested the application while it was running, verified the HTTPS connection, and performed software dependency analysis.

Secure coding is important because vulnerabilities can expose confidential information, allow data to be modified, or make an application easier to attack. Security also contributes to the overall health of a company by protecting customer information, reducing risk, supporting customer trust, and preventing problems caused by insecure third-party components.

## Vulnerability Assessment Challenges

One of the more challenging parts of the project was dependency vulnerability scanning. I used **OWASP Dependency-Check** to analyze the application's dependencies. The scan identified vulnerabilities associated with the existing Spring Boot framework, which required me to determine whether the vulnerabilities came from my changes or from the original project dependencies.

The dependency scanner also experienced an issue retrieving one of its online security feeds, so I completed the analysis using the available local NVD vulnerability data. This part of the project was helpful because it showed me that identifying a vulnerability is only the beginning. Developers also need to determine where the vulnerability originates, how serious it is, and what mitigation is appropriate.

## Increasing Layers of Security

I increased security using a **defense-in-depth** approach. Instead of relying on a single security control, I added multiple layers of protection. SHA-256 was used to verify data integrity, HTTPS and TLS protected information while it was being transmitted, the certificate helped authenticate the server, automated tests verified expected behavior, and dependency scanning identified risks in third-party software.

In future projects, I would continue using tools such as OWASP Dependency-Check along with NIST security standards, automated testing, code reviews, vulnerability databases, and dependency analysis. I would evaluate each vulnerability based on its severity, exploitability, affected component, and potential impact before deciding which mitigation technique should be used.

## Testing Functionality and Security

After refactoring the application, I made sure that it remained both functional and secure through several forms of testing. I ran the Maven test suite and confirmed that the automated tests completed successfully without failures or errors. I also started the packaged application and tested the HTTPS endpoint on port 8443.

I verified the secure connection using tools such as **curl and OpenSSL** and confirmed that the application negotiated TLS successfully. I also independently verified the SHA-256 checksum to make sure that the application generated the expected result.

After completing the refactoring, I ran OWASP Dependency-Check again and manually reviewed the Java source code and application configuration. This helped determine whether my changes introduced any new security problems. The remaining vulnerabilities were associated with the supplied Spring Boot dependency baseline rather than the new checksum functionality.

## Resources, Tools, and Secure Coding Practices

Several tools and practices from this project will be useful in future software development work. These include:

* **OWASP Dependency-Check** for identifying vulnerabilities in third-party dependencies
* **Maven** for building and testing Java applications
* **Java MessageDigest** for implementing SHA-256 hashing
* **Java keytool** for generating and managing certificates and keystores
* **OpenSSL** for inspecting and verifying TLS connections
* **PKCS12 keystores** for certificate and private-key storage
* **TLS 1.2 and TLS 1.3** for secure network communication
* **NIST security standards** for selecting appropriate cryptographic algorithms
* Automated testing and manual code review
* Dependency minimization and vulnerability analysis
* Keeping production passwords and secrets outside of source code

One of the most important practices I learned was to use established security standards and trusted cryptographic libraries instead of attempting to design custom security mechanisms.

## What I Would Show Future Employers

I would show future employers my **Artemis Financial Practices for Secure Software Report** as an example of my ability to analyze and improve the security of a software application. The project demonstrates that I can work with secure communication protocols, hashing algorithms, certificates, Java security APIs, automated tests, dependency scanning, and vulnerability mitigation.

I would also discuss the refactored application and the testing evidence from the project to demonstrate that I understand both secure software development and the importance of verifying that security changes do not negatively affect application functionality. Overall, this project demonstrates my ability to approach software security as an ongoing development process rather than something that is added only after an application is complete.
:::

This covers **all seven required questions**, so you can paste it straight into your GitHub `README.md` and submit the **Practices for Secure Software Report** as the artifact.
