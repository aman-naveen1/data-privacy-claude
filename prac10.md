# PRACTICAL – 10

# CASE STUDIES IN DATA PRIVACY AND CLAUDE AI

## AIM

To study practical case studies related to data privacy and Claude AI and to analyze the privacy risks, ethical concerns, security issues, applicable privacy principles, and suitable mitigation measures in each situation.

## OBJECTIVES

- To understand how data privacy issues can arise in real-world situations.
- To apply concepts studied in previous practicals to practical scenarios.
- To identify privacy and security risks involving AI systems.
- To analyze data minimization, purpose limitation, consent, retention, security, and user control.
- To understand the role of anonymization, encryption, privacy-enhancing technologies, and incident response.
- To recommend appropriate privacy and security measures.
- To develop practical problem-solving skills related to AI data privacy.

## INTRODUCTION

Case studies help in understanding how data privacy principles are applied in real situations.

Claude AI can be used for activities such as writing, summarization, programming, document analysis, research, and educational assistance. During these activities, users or organizations may provide conversations, documents, source code, personal information, or confidential business information.

The previous practicals examined data privacy audits, Privacy Impact Assessments, data protection requirements, cryptography, anonymization, privacy policy analysis, Privacy-Enhancing Technologies, breach response, and data ethics. This practical combines those concepts through practical case studies.

The case studies below are educational examples. They use fictional organizations and situations to demonstrate privacy principles and are not intended to represent a specific incident involving Anthropic or Claude.

## SYSTEM SELECTED

System Name: Claude AI

Developer: Anthropic

Type: Generative Artificial Intelligence Assistant

Possible information involved:

- Conversation data
- Uploaded documents and files
- Source code
- Account-related information
- Feedback
- Technical and usage information

---

# CASE STUDY 1 – STUDENT DOCUMENT ANALYSIS

## SCENARIO

A college student wants Claude to summarize a project report. The student uploads the complete document without removing personal information. The document contains the student's name, college roll number, email address, phone number, project information, and a scanned identity document.

The identity document is not required to summarize the project report.

## PRIVACY ISSUES IDENTIFIED

- Unnecessary personal information has been submitted.
- A government or identity document has been uploaded even though it is unrelated to the task.
- The student's contact information is unnecessarily exposed.
- The student may not have considered the applicable data-handling and retention practices of the AI service.
- The principle of data minimization is not being followed.

## RISK ASSESSMENT

| Risk | Likelihood | Impact | Risk Level |
|---|---|---|---|
| Unnecessary personal information exposure | Medium | High | High |
| Identity document exposure | Low/Medium | High | Medium/High |
| Account compromise | Medium | High | High |
| Unnecessary data retention | Medium | Medium/High | Medium/High |

## ANALYSIS

The purpose of the task is only to summarize the project report. The student's name, phone number, email address, roll number, and identity document are not necessary for this purpose.

This is a clear example of data minimization. Only the information required for the intended task should be provided.

## RECOMMENDED ACTION

The student should:

1. Remove unnecessary personal identifiers.
2. Remove the identity document completely.
3. Upload only the portion of the report required for summarization.
4. Review applicable privacy controls and retention information.
5. Delete unnecessary stored information where appropriate.
6. Avoid entering passwords, authentication secrets, or highly sensitive information.

## PRIVACY PRINCIPLES APPLIED

- Data minimization
- Purpose limitation
- Security
- User control
- Retention limitation

---

# CASE STUDY 2 – COMPANY CONFIDENTIAL DOCUMENT

## SCENARIO

A software company allows employees to use Claude for summarizing internal documents. An employee uploads an internal product strategy document containing unreleased product features, customer information, internal financial information, employee names, and API credentials.

The employee only wanted Claude to summarize the product strategy.

## PRIVACY AND SECURITY ISSUES

- Confidential business information is unnecessarily exposed.
- API credentials should not be included in an AI prompt.
- Customer information may not be necessary for the task.
- The organization has not clearly defined which information employees are allowed to submit.
- The incident may affect both privacy and information security.

## RISK ASSESSMENT

| Information | Example | Risk |
|---|---|---|
| Customer information | Names and contact details | Privacy exposure |
| Financial information | Internal financial data | Confidentiality loss |
| Product strategy | Unreleased features | Business impact |
| API credentials | Secret keys | Unauthorized system access |
| Employee information | Internal employee details | Privacy exposure |

## ANALYSIS

The main issue is not simply that Claude was used. The problem is that more information than necessary was submitted.

API credentials are particularly sensitive and should never be included in ordinary AI prompts. The company should also classify information before employees submit it to an AI service.

## RECOMMENDED ACTION

The company should:

- Establish an AI acceptable-use policy.
- Define permitted and prohibited information categories.
- Train employees on responsible AI use.
- Remove credentials and secrets before submission.
- Apply data minimization and redaction.
- Use access controls for sensitive information.
- Periodically review AI usage and privacy practices.
- Establish a procedure for reporting accidental disclosure.

## PRIVACY PRINCIPLES APPLIED

- Data minimization
- Purpose limitation
- Confidentiality
- Least privilege
- Accountability
- Employee awareness

---

# CASE STUDY 3 – STUDENT DATA ANALYTICS

## SCENARIO

A university wants to analyze student performance using an AI-assisted data analysis system. The dataset contains names, student IDs, ages, departments, grades, attendance information, and demographic information.

The university plans to share the dataset with an external analyst after removing student names.

## PRIVACY ISSUES IDENTIFIED

Removing names alone does not necessarily make a dataset anonymous.

Other information such as age, department, grades, attendance, and demographic characteristics may act as quasi-identifiers.

## ANALYSIS

The university should examine whether students can still be identified by combining the remaining data with other information.

Possible privacy-enhancing techniques include:

- Data masking
- Pseudonymization
- Generalization
- k-anonymity
- Differential privacy

A mapping table used for pseudonymization should be separately protected.

For statistical analysis, differential privacy can be considered when appropriate because it adds controlled uncertainty to published results.

## EXAMPLE

Before minimization:

```text
Name: Student A
Student ID: 10457
Age: 19
Department: Computer Science
Attendance: 91%
Grade: 88
```

After generalization and minimization:

```text
Age Group: 18–21
Department: Computing
Attendance Range: 85–95%
Grade Range: 80–90
```

The exact transformation should be selected according to the privacy risk and intended analytical purpose.

## RECOMMENDED ACTION

The university should:

1. Identify direct identifiers and quasi-identifiers.
2. Remove unnecessary fields.
3. Evaluate re-identification risks.
4. Select an appropriate anonymization or privacy-enhancing technique.
5. Protect any pseudonymization mapping separately.
6. Assess the privacy-utility trade-off before releasing the dataset.

## PRIVACY PRINCIPLES APPLIED

- Data minimization
- Anonymization
- Pseudonymization
- Generalization
- k-anonymity
- Differential privacy
- Privacy-utility trade-off

---

# CASE STUDY 4 – AI-ASSISTED HR RECRUITMENT

## SCENARIO

A company uses an AI system to help summarize job applications. Recruiters upload resumes containing names, phone numbers, addresses, educational information, employment history, and other personal details.

The company begins relying heavily on AI-generated summaries while making hiring decisions.

## PRIVACY AND ETHICAL ISSUES

- Resumes contain personal information.
- The organization should determine which information is actually necessary for the task.
- AI-generated information may be inaccurate.
- Excessive reliance on AI output may reduce appropriate human oversight.
- The organization should consider whether the AI-assisted process could create unfair effects for different applicants.
- Access to applicant information should be restricted to authorized personnel.

## ANALYSIS

Privacy and ethical considerations must be addressed together.

The organization should distinguish between:

**Privacy:** How applicant information is collected, used, stored, and shared.

**Security:** How applicant information is protected from unauthorized access.

**Fairness:** Whether AI-assisted processing could create unequal effects.

**Human Oversight:** Whether recruiters appropriately review important decisions rather than relying blindly on AI output.

## RECOMMENDED ACTION

The company should:

- Define the purpose of processing applicant data.
- Remove unnecessary personal information where practical.
- Restrict access to applicant records.
- Establish appropriate retention periods.
- Evaluate AI outputs for accuracy.
- Conduct appropriate fairness assessments.
- Maintain meaningful human review for important decisions.
- Document responsibilities and controls.

## PRIVACY PRINCIPLES APPLIED

- Purpose limitation
- Data minimization
- Security
- Fairness
- Accountability
- Human oversight

---

# CASE STUDY 5 – ACCIDENTAL PRIVACY BREACH

## SCENARIO

An employee accidentally copies a confidential customer complaint into a public AI chat instead of the organization's approved internal AI environment. The text contains the customer's name, phone number, email address, order details, and complaint history.

The employee realizes the mistake several minutes later.

## IMMEDIATE RESPONSE

The organization should follow its incident-response procedure.

### STAGE 1 – DETECTION

Record the incident as soon as it is identified.

### STAGE 2 – INITIAL ASSESSMENT

Determine:

- What information was submitted?
- When was it submitted?
- Which account or system was used?
- Who may be affected?
- Is the information still accessible?
- What immediate action is possible?

### STAGE 3 – CONTAINMENT

Possible actions include:

- Restrict or secure the affected account.
- Remove the information where applicable and where the service permits.
- Reset credentials if credentials were exposed.
- Preserve relevant evidence and logs.
- Prevent further disclosure.

### STAGE 4 – INVESTIGATION

Determine the exact information involved and whether other systems, users, or third parties were affected.

### STAGE 5 – RISK ASSESSMENT

Assess potential consequences to the affected customer and organization.

### STAGE 6 – COMMUNICATION

If notification is legally or organizationally required, affected parties should receive clear and accurate information.

### STAGE 7 – RECOVERY

Review access controls, employee procedures, training, and technical safeguards.

### STAGE 8 – POST-INCIDENT REVIEW

Identify the cause and implement measures to reduce the likelihood of recurrence.

## RECOMMENDED ACTION

The organization should also review its AI acceptable-use policy and make the difference between approved and unapproved AI environments clear to employees.

## PRIVACY PRINCIPLES APPLIED

- Incident response
- Data minimization
- Security
- Accountability
- User protection

---

# CASE STUDY 6 – PRIVACY-PRESERVING AI ANALYTICS

## SCENARIO

An organization wants to understand how employees use an AI assistant. Management does not need to inspect individual conversations. It only wants higher-level information such as the most common types of tasks, overall usage patterns, and trends over time.

## PRIVACY CHALLENGE

Directly reviewing individual conversations could unnecessarily expose personal or confidential information.

## ANALYSIS

The organization should consider privacy-enhancing approaches such as:

- Aggregation
- Anonymization
- Access controls
- Data minimization
- Differential privacy where suitable

Anthropic has described Clio as a privacy-preserving system for analyzing patterns in Claude usage using techniques such as anonymization and aggregation. This illustrates a broader privacy principle: analytics can sometimes be designed around higher-level information rather than direct inspection of individual conversations.

However, privacy-preserving analytics should still be evaluated for:

- What information is collected.
- How information is transformed.
- Who can access it.
- Whether re-identification is possible.
- How long information is retained.

## RECOMMENDED ACTION

The organization should:

1. Collect only information necessary for the analytics purpose.
2. Prefer aggregated results where possible.
3. Restrict access to raw data.
4. Evaluate re-identification risks.
5. Establish appropriate retention periods.
6. Document the purpose and controls.

## PRIVACY PRINCIPLES APPLIED

- Data minimization
- Aggregation
- Anonymization
- Differential privacy
- Access control
- Purpose limitation

---

# CASE STUDY COMPARISON

| Case Study | Main Privacy Issue | Main Principle | Recommended Control |
|---|---|---|---|
| Student Document Analysis | Unnecessary personal information | Data minimization | Remove unnecessary identifiers |
| Company Confidential Document | Confidential data and credentials | Purpose limitation | Redaction and AI usage policy |
| Student Data Analytics | Re-identification risk | Anonymization | Generalization and privacy-enhancing techniques |
| AI-Assisted HR | Privacy, fairness, and over-reliance | Human oversight | Access control and human review |
| Accidental Privacy Breach | Unauthorized disclosure | Incident response | Detection, containment, investigation |
| Privacy-Preserving Analytics | Excessive access to raw data | Data minimization | Aggregation and anonymization |

---

# GENERAL CASE STUDY ANALYSIS METHOD

The following method can be used to analyze a data privacy case:

```text
Identify the Data
       |
       v
Identify the Purpose
       |
       v
Is the Data Necessary?
       |
     +---+
     |   |
    No  Yes
     |   |
  Remove |
  Data   v
       Identify Risks
           |
           v
     Assess Impact
           |
           v
   Select Privacy Controls
           |
           v
     Apply Security
           |
           v
   Consider Fairness
           |
           v
  Maintain Human Oversight
           |
           v
     Document Actions
           |
           v
       Review
```

## GENERAL RECOMMENDATIONS

### FOR USERS

- Provide only information necessary for the task.
- Do not enter passwords, API keys, or authentication secrets.
- Remove unnecessary personal information from documents.
- Review applicable privacy settings.
- Verify important AI-generated information.
- Follow organizational AI policies.

### FOR ORGANIZATIONS

- Establish a clear AI acceptable-use policy.
- Classify information before allowing it to be submitted to AI systems.
- Apply data minimization and purpose limitation.
- Use appropriate access controls and authentication.
- Protect sensitive information using suitable security controls.
- Evaluate anonymization and privacy-enhancing techniques where appropriate.
- Maintain incident-response procedures.
- Train employees regularly.
- Conduct privacy and ethical assessments for high-impact uses.
- Maintain appropriate human oversight.
- Review AI privacy practices periodically.

## FINDINGS

The case studies produced the following findings:

- Many AI privacy risks are caused by providing more information than necessary.
- Personal and confidential information should be minimized before being submitted.
- Removing a person's name does not automatically make a dataset anonymous.
- Security and privacy should be considered together but are not identical.
- AI-assisted decisions may require human oversight.
- Privacy incidents should be handled through a structured response process.
- Anonymization, aggregation, and other privacy-enhancing techniques can reduce unnecessary exposure.
- Organizations need clear policies explaining acceptable AI use.
- Employee awareness and training are important parts of privacy protection.
- Responsible AI use requires continuous review of privacy, security, ethical, and governance controls.

## CONCLUSION

The case studies demonstrate how data privacy principles can be applied to realistic situations involving Claude AI and other AI-assisted systems.

The practical examined student document processing, confidential business information, student analytics, AI-assisted recruitment, accidental privacy breaches, and privacy-preserving analytics.

The analysis shows that privacy protection is not limited to a single technical control. Effective protection requires data minimization, purpose limitation, appropriate security, anonymization where suitable, access control, incident response, transparency, human oversight, and user awareness.

Users should provide only information necessary for their intended task, while organizations should establish clear policies, technical safeguards, training, accountability, and review procedures.

## RESULT

The case studies on data privacy and Claude AI were successfully analyzed. Privacy risks, ethical issues, security concerns, relevant privacy principles, and suitable mitigation strategies were identified for each case.

## VIVA QUESTIONS AND ANSWERS

### Q1. What is a case study in data privacy?

Answer: A case study is a practical scenario used to examine how privacy principles, risks, and controls apply to a real or fictional situation.

### Q2. What is the main lesson from the student document case?

Answer: Only information necessary for the intended task should be provided. Unnecessary personal information should be removed.

### Q3. Why should API keys not be entered into an AI prompt?

Answer: API keys are authentication secrets. If exposed, they may allow unauthorized access to a system or service.

### Q4. Does removing a person's name make a dataset anonymous?

Answer: No. Other information may still identify a person when combined with other datasets.

### Q5. What is data minimization?

Answer: Data minimization means using or providing only the information necessary for a specific purpose.

### Q6. Why is human oversight important in AI-assisted recruitment?

Answer: Human oversight helps ensure that important decisions are reviewed appropriately and that AI output is not treated as automatically correct.

### Q7. What should an organization do after an accidental privacy breach?

Answer: It should detect and record the incident, assess the situation, contain further exposure, investigate, assess risk, communicate where required, recover, and conduct a post-incident review.

### Q8. What is the privacy-utility trade-off?

Answer: It is the balance between reducing the ability to identify individuals and keeping enough information for useful analysis.

### Q9. Why are aggregation and anonymization useful in privacy analytics?

Answer: They can reduce unnecessary exposure of individual-level information while still allowing organizations to study overall patterns.

### Q10. What is the main lesson from all the case studies?

Answer: Responsible AI use requires data minimization, clear purpose, appropriate security, user awareness, suitable privacy controls, human oversight where necessary, and a structured response to privacy incidents.

## REFERENCES

- Anthropic – Official Website
- Anthropic – Consumer Privacy Policy and Terms
- Anthropic – Security and Privacy Information
- Anthropic – Clio Research
- NIST Privacy Framework
- General Data Protection Regulation (GDPR)
- Digital Personal Data Protection Act, 2023
- General references on data anonymization and differential privacy

Access Date: 24 September 2026
