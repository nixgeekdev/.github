# Security Policy

If you believe you have identified a security issue with a NixGeek.Dev project,
_**do not open a public issue**_. To responsibly report a security issue, use
GitHub's [security advisory
system](https://docs.github.com/en/code-security/security-advisories/working-with-repository-security-advisories/creating-a-repository-security-advisory).
From the project's repository, click _"Security"_ at the top, then click
_"Advisories"_ at the left, then click the green _"New draft security advisory"_
button. Alternatively, you may email
[security@nixgeek.dev](mailto:security@nixgeek.dev), and we will convert that to
a GitHub security advisory.

Be sure to include as much detail as necessary in your report. As with reporting
normal issues, a minimal reproducible example will help the maintainers address
the issue faster. Information about why the issue is a security issue is also
helpful. If you are able, you may also provide a fix for the issue.

A maintainer will reply acknowledging the report and how to continue. We will
obtain a CVE id as well, please do not do this on your own. We will work with
you to attempt to understand the issue and decide on its validity. Maintainers
are volunteers working in their free time, and therefore cannot guarantee any
specific timeline. Please be patient during this process.

The current feature release will receive security fixes. A backport to the
previous feature branch may be considered upon request based on usage
information and severity, but is not guaranteed.

The NixGeek.Dev organization is not currently in a financial position were its
able to offer bug or security bounties.

## Before Reporting

The following categories will generally not be considered security issues. You 
may still err on the side of caution and make a private report first, but we may 
close it or ask you to report a regular issue instead.

- Insecure configuration or code in a project using our libraries. This should
  be reported to the relevant project instead.
- Automated reports from vulnerability scanners or "AI" tools. Please make it
  clear that you understand what you are reporting and have put personal time
  into crafting the report.
- Do not report something that has already been fixed and released; check the
  project's change log. Getting a notification from your security scanner that
  you need to update is not itself a new vulnerability to report.
