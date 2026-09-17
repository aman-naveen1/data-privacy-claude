PRACTICAL – 5

ANONYMIZATION TECHNIQUES FOR PROTECTING PERSONAL DATA
AIM

To study and apply different data anonymization techniques such as data masking, pseudonymization, k-anonymity, and differential privacy to a sample dataset in order to reduce privacy risks while maintaining useful information for analysis.

OBJECTIVES

To understand the concept of data anonymization.

To understand the difference between anonymization and pseudonymization.

To implement data masking on personal information.

To understand and apply k-anonymity.

To understand the basic concept of differential privacy.

To compare privacy protection with data utility.

To understand the importance of anonymization in data privacy.

INTRODUCTION

Organizations often collect personal information for activities such as education, healthcare, banking, research, and customer management.

Sometimes data needs to be analyzed or shared without unnecessarily exposing the identity of individuals. Data anonymization techniques can help reduce privacy risks.

Anonymization involves transforming data so that individuals cannot reasonably be identified from the resulting dataset, taking into account the relevant circumstances and available information.

Common privacy techniques include:

Data masking

Pseudonymization

Generalization

k-anonymity

Differential privacy

DATASET USED

For this practical, the following fictional student dataset is used.

ORIGINAL DATASET

Student ID	Name	Age	Gender	City	Course	Marks
S001	Rahul Sharma	20	Male	Delhi	BCA	82
S002	Priya Singh	21	Female	Delhi	BCA	78
S003	Amit Kumar	20	Male	Noida	BCA	85
S004	Neha Verma	21	Female	Noida	BCA	81
S005	Arjun Mehta	22	Male	Gurgaon	BCA	75
S006	Simran Kaur	22	Female	Gurgaon	BCA	79

Note: All names and data in this practical are fictional.

TYPES OF DATA

The dataset contains different types of information.

A. DIRECT IDENTIFIERS

Direct identifiers can directly identify an individual.

Examples:

Name

Student ID

Phone number

Email address

B. QUASI-IDENTIFIERS

Quasi-identifiers may not uniquely identify a person by themselves but can contribute to identification when combined with other information.

Examples:

Age

Gender

City

Course

C. SENSITIVE INFORMATION

Sensitive information can cause privacy harm if improperly disclosed.

Examples may include:

Medical information

Financial information

Passwords

Certain identification information

In this dataset, marks are treated as academic information.

TECHNIQUE 1 – DATA MASKING

Data masking replaces part of a value with another character or hides it.

For example:

Original Email:
rahul@example.com

Masked Email:
r****@example.com

Original Phone:
9876543210

Masked Phone:
98******10

PROCEDURE:

Identify fields containing personal information.

Select the portion that should be hidden.

Replace the selected characters with symbols such as *.

Keep only the information necessary for the intended purpose.

Verify that the masked data cannot unnecessarily expose the original value.

EXAMPLE:

Original Name	Masked Name
Rahul Sharma	R***** S****
Priya Singh	P**** S****
Amit Kumar	A*** K****
Neha Verma	N*** V****

RESULT:

Data masking successfully reduced the visibility of direct identifiers.

TECHNIQUE 2 – PSEUDONYMIZATION

Pseudonymization replaces identifying information with artificial identifiers.

Example:

Original:

Student ID: S001
Name: Rahul Sharma

Pseudonymized:

Student ID: STUDENT_001
Name: PERSON_A

PSEUDONYMIZED DATASET

Pseudonymous ID	Age	Gender	City	Course	Marks
STUDENT_001	20	Male	Delhi	BCA	82
STUDENT_002	21	Female	Delhi	BCA	78
STUDENT_003	20	Male	Noida	BCA	85
STUDENT_004	21	Female	Noida	BCA	81
STUDENT_005	22	Male	Gurgaon	BCA	75
STUDENT_006	22	Female	Gurgaon	BCA	79

PROCEDURE:

Identify direct identifiers.

Replace the identifiers with artificial values.

Keep the mapping information separate and protected if it is needed operationally.

Analyze the pseudonymized dataset without exposing the original names.

OBSERVATION:

Pseudonymization reduces direct exposure of identity but does not automatically make data anonymous. If the pseudonyms can be linked back to individuals, the information remains potentially identifiable.

RESULT:

The dataset was successfully pseudonymized by replacing direct identifiers with artificial identifiers.

TECHNIQUE 3 – GENERALIZATION

Generalization reduces the precision of information.

For example:

Exact Age:

20, 21, 22

Generalized Age:

20–22

Exact City:

Delhi
Noida
Gurgaon

Generalized Location:

NCR

GENERALIZED DATASET

Student ID	Age Group	Gender	Region	Course	Marks
STUDENT_001	20–22	Male	NCR	BCA	82
STUDENT_002	20–22	Female	NCR	BCA	78
STUDENT_003	20–22	Male	NCR	BCA	85
STUDENT_004	20–22	Female	NCR	BCA	81
STUDENT_005	20–22	Male	NCR	BCA	75
STUDENT_006	20–22	Female	NCR	BCA	79

OBSERVATION:

Generalization reduces the precision of information and therefore reduces the possibility of identifying an individual from specific attributes.

TECHNIQUE 4 – K-ANONYMITY

k-anonymity is a privacy model in which each combination of selected quasi-identifiers occurs for at least k records in the released dataset.

For example, if k = 2, every combination of the selected quasi-identifiers should occur in at least two records.

Consider the following quasi-identifiers:

Age Group

Gender

Region

After generalization, the dataset can contain repeated combinations such as:

Age Group: 20–22
Gender: Male
Region: NCR

This combination appears in multiple records.

Similarly:

Age Group: 20–22
Gender: Female
Region: NCR

also appears in multiple records.

PROCEDURE:

Select quasi-identifiers.

Identify combinations that could distinguish individuals.

Generalize or suppress values.

Group records with similar quasi-identifiers.

Check whether each equivalence class contains at least k records.

Repeat the process if necessary.

EXAMPLE:

For k = 2:

Age Group	Gender	Region	Number of Records
20–22	Male	NCR	3
20–22	Female	NCR	3

Since each group contains at least two records, the example satisfies k = 2 for the selected quasi-identifiers.

RESULT:

The dataset was generalized to demonstrate k-anonymity with k = 2.

TECHNIQUE 5 – DIFFERENTIAL PRIVACY

Differential privacy is a mathematical framework for reducing the privacy risk associated with learning information about individuals from statistical queries.

Instead of releasing an exact statistic, controlled random noise can be added to the result.

For example:

Actual number of students:
100

Published result:
102

The small difference is introduced to reduce the ability to determine whether a particular individual's data contributed to the result.

A simplified example can be represented as:

Published Count = Actual Count + Random Noise

PROCEDURE:

Calculate a statistical value from the dataset.

Determine the privacy mechanism to be used.

Add controlled noise to the result.

Release the noisy result instead of the exact value.

Compare privacy protection with the accuracy of the result.

EXAMPLE:

Actual number of students who passed:

80

Random noise:

+2

Published result:

82

The published result is slightly different from the actual result.

OBSERVATION:

Differential privacy introduces uncertainty into statistical outputs, making it more difficult to determine whether information about a particular individual was included.

The amount of privacy and the accuracy of the result depend on the parameters of the privacy mechanism.

COMPARISON OF TECHNIQUES

Technique	Main Purpose	Privacy Level	Data Utility
Data Masking	Hide parts of data	Medium	High
Pseudonymization	Replace identifiers	Medium	High
Generalization	Reduce data precision	Medium/High	Medium
k-Anonymity	Make records less distinguishable	High	Medium
Differential Privacy	Protect statistical outputs	High	Medium

The actual level of protection depends on how each technique is implemented and what additional information an attacker may have.

PRIVACY-UTILITY TRADE-OFF

An important concept in data anonymization is the privacy-utility trade-off.

Increasing privacy protection may reduce the usefulness or accuracy of a dataset.

For example:

Original:
Age = 20

Generalized:
Age = 20–22

The generalized information provides less precise information but can provide greater privacy.

Similarly, adding more noise under differential privacy can provide stronger privacy protection but may reduce the accuracy of statistical results.

OBSERVATIONS

The following observations were made:

Direct identifiers can be hidden using data masking.

Pseudonymization replaces direct identifiers with artificial identifiers.

Pseudonymized data may still be linkable to an individual.

Generalization reduces the precision of information.

k-anonymity attempts to ensure that individuals are not distinguishable based on selected quasi-identifiers.

Differential privacy adds controlled uncertainty to statistical outputs.

No anonymization technique automatically provides perfect protection in every situation.

The choice of technique depends on the intended use of the data and the privacy risk.

SECURITY AND PRIVACY PRECAUTIONS

Do not use real personal information for classroom demonstrations unless properly authorized.

Use fictional or properly de-identified datasets.

Protect any mapping table used for pseudonymization.

Do not publish sensitive information unnecessarily.

Consider possible linkage attacks using external datasets.

Evaluate privacy risks before releasing an anonymized dataset.

Do not assume that simply removing names makes a dataset anonymous.

Select anonymization techniques according to the intended purpose and risk.

RESULT

Different data anonymization techniques were successfully studied and applied to a sample student dataset.

Data masking, pseudonymization, generalization, k-anonymity, and differential privacy were examined to understand how personal information can be protected while retaining useful information for analysis.

CONCLUSION

Data anonymization is an important technique for reducing privacy risks when data needs to be analyzed or shared.

In this practical, direct identifiers were masked and replaced through pseudonymization. Generalization was then used to reduce the precision of quasi-identifiers. k-anonymity was demonstrated by grouping records according to generalized quasi-identifiers. Differential privacy was studied using the concept of adding controlled noise to statistical results.

The practical demonstrates that privacy protection and data utility must be balanced. Different techniques provide different types and levels of protection, and the appropriate method depends on the nature of the dataset, the intended purpose, and the potential privacy risks.

VIVA QUESTIONS AND ANSWERS

Q1. What is data anonymization?

Answer: Data anonymization is the process of transforming information to reduce the ability to identify individuals from the resulting data.

Q2. What is data masking?

Answer: Data masking hides all or part of a value by replacing characters with symbols or other values.

Q3. What is pseudonymization?

Answer: Pseudonymization replaces direct identifiers with artificial identifiers or pseudonyms.

Q4. Is pseudonymized data always anonymous?

Answer: No. If the pseudonymized information can be linked back to an individual, it may still be considered identifiable.

Q5. What is k-anonymity?

Answer: k-anonymity is a privacy model in which each combination of selected quasi-identifiers occurs in at least k records.

Q6. What does k = 2 mean?

Answer: It means each equivalence class based on the selected quasi-identifiers should contain at least two records.

Q7. What is differential privacy?

Answer: Differential privacy is a mathematical framework that limits the privacy loss associated with statistical analysis by introducing controlled uncertainty.

Q8. What is generalization?

Answer: Generalization replaces precise information with broader categories, such as replacing an exact age with an age range.

Q9. What is a quasi-identifier?

Answer: A quasi-identifier is information that may not directly identify a person but can contribute to identification when combined with other information.

Q10. What is the privacy-utility trade-off?

Answer: It is the balance between protecting individual privacy and maintaining the usefulness or accuracy of a dataset.

REFERENCES

Data Privacy and Information Security textbooks

NIST Privacy Framework and related privacy resources

General references on k-anonymity

General references on differential privacy

Python documentation for data-processing demonstrations

Access Date: 17 September 2026
