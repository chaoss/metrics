# Metric: Risk

Goal: Identify the risk profile of a project. 

## Human Factors

Goal: Identify the risk associated with the people involved in a project. 

Metric | Question
--- | ---
Contributor Importance | What is the fraction of commits by individual contributors from identified organizations?
Committers | What are their contributions and to what components do they commit to?
User Dependency | What is the number of users who are aware that they depend on the project? 
Paid Developers | What is the number of paid developers in a project?

## Copyright and License Factors

Goal: Identify the risk associated with copyright and license issues. 

Metric | Question
--- | ---
Copyright Declaration | What is the degree to which the project properly declares copyright ownership, including the copyright symbol or 'copyright' word, the year of the creation, the name of the author, and a rights statement?
Package License Declaration | What are the license declarations on the software package? 
File License Declarations | What are the license declarations on the software package files?
License Identification Methods | What are the methods or tools used for identifying licenses in files?

## Vulnerability Factors

Goal: Identify the risk associated with vulnerabity issues. 

Metric | Question
--- | ---
Published CPE | What are the number of published [Common Platform Enumerations (CPEs)](https://nvd.nist.gov/products/cpe) for the project (i.e., a project can contain many packages)?
Disclosed Vulnerabilities | What are the number of disclosed package vulnerabilities?
Vulnerabilities in Media | What are the number of published press articles about package related vulnerabilities?

**Disclaimer:**
The name/question pairs listed are not meant to represent a fully comprehensive list. It is expected that this list will evolve as people have insights and thoughts about the name/question pairs that comprise Risk.

**Tooling:**
The name/question pairs are intended to be a starting point for CHAOSS-related software. It is expected that this list will evolve based on the ability (or inability) of software to successfully implement the specific name/question pairs.

**Background:**
The name/question pairs have been identified based CHAOSS-related outreach activities. We thank everyone who participated.

**How to contribute:**
- To advance the document, fork the repo, make your changes, create a pull request see [CONTRIBUTING.md][contrib]
- To ask questions or make comments, post to our [mailing list][ml], join our weekly [Hangout call][ho], or open an [issue on GitHub][issue].

[contrib]: .github/CONTRIBUTING.md
[ml]: https://wiki.linuxfoundation.org/chaoss/metrics#mail-list
[ho]: https://wiki.linuxfoundation.org/chaoss/metrics#weekly-hangout
[issue]: https://github.com/chaoss/metrics/issues
