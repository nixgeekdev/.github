<!--
Please use Conventional Commits 1.0.0 Format for the PR

    <type>[optional scope]: <description>

    [optional body]

    [optional footer(s)]

See https://www.conventionalcommits.org/en/v1.0.0/ for examples
-->


----

### Creator Checklist
<!-- Check items by adding an "x" within the brackets or clicking after the PR is created. -->  

- [ ] **Testing**
  - Changes have been tested locally or in an appropriate environment.
  - Test coverage is sufficient.
  - Unnecessary comments and debug statements have been removed.
- [ ] **Security**
  - No hardcoded secrets (e.g., API keys, credentials).
  - IAM roles and permissions follow the principle of least privilege.
  - Public exposure of resources (e.g., storage, APIs, security groups) is restricted unless explicitly required.
  - No security misconfigurations in infrastructure (e.g., open security groups, unrestricted access).
  - Input validation and error handling follow secure coding practices (e.g., OWASP Top 10).
- [ ] **Logging & Monitoring**
  - Logging provides sufficient context for debugging and auditing without exposing sensitive information.
  - Logs are securely stored and adhere to compliance requirements.
  - Monitoring and alerting have been updated to reflect changes.
- [ ] **Dependencies**
  - Dependencies come from trusted sources.
  - Versions are pinned to prevent unexpected updates.
  - Dependencies have been vetted for security vulnerabilities and licensing issues.
- [ ] **Documentation**
  - Relevant documentation (e.g., API docs, usage instructions, examples) has been updated.
- [ ] **Merging**
  - Merged latest changes from `main`.
  - Your branch points to `main`.

### Reviewer Checklist
<!-- Ensure all security and quality checks are met before approving. -->  

- [ ] **Code Review**
  - Code is clean, follows best practices, and avoids unnecessary complexity.
  - Error handling and input validation are properly implemented.
- [ ] **Security**
  - No hardcoded secrets or sensitive data exposure.
  - IAM and access controls are properly scoped and follow least privilege.
  - No unnecessary publicly accessible resources.
  - Code follows secure development practices (e.g., input validation, error handling).
- [ ] **Logging & Monitoring**
  - Sufficient logging is in place for debugging and auditing.
  - No sensitive data is logged.
  - Monitoring and alerting have been updated to reflect changes.
- [ ] **Dependencies**
  - No untrusted or vulnerable dependencies are introduced.
  - Versioning strategy is appropriate.
- [ ] **Documentation**
  - Any necessary updates to documentation are made.
     
----

### Creator's Affidavit of Origin

By making a contribution to this project, I certify that:

 (a) The contribution was created in whole or in part by me and I
     have the right to submit it under the open source license
     indicated in the file; or

 (b) The contribution is based upon previous work that, to the best
     of my knowledge, is covered under an appropriate open source
     license and I have the right under that license to submit that
     work with modifications, whether created in whole or in part
     by me, under the same open source license (unless I am
     permitted to submit under a different license), as indicated
     in the file; or

 (c) The contribution was provided directly to me by some other
     person who certified (a), (b) or (c) and I have not modified
     it.

 (d) I understand and agree that this project and the contribution
     are public and that a record of the contribution (including all
     personal information I submit with it, including my sign-off) is
     maintained indefinitely and may be redistributed consistent with
     this project or the open source license(s) involved.
