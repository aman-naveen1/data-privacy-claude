PRACTICAL – 7

STUDY AND EVALUATION OF PRIVACY-ENHANCING TECHNOLOGIES (PETS)
AIM

To study Privacy-Enhancing Technologies (PETs) such as Virtual Private Networks (VPNs), Tor, secure messaging applications, encryption, and privacy-preserving technologies, and to understand their role in protecting user privacy.

OBJECTIVES

To understand the concept of Privacy-Enhancing Technologies.

To study different types of PETs.

To understand how VPNs protect network traffic.

To understand how Tor provides anonymity at the network level.

To study end-to-end encryption in secure messaging.

To compare different privacy-enhancing technologies.

To understand the limitations of PETs.

To identify appropriate technologies for different privacy requirements.

INTRODUCTION

Privacy-Enhancing Technologies (PETs) are technologies and techniques designed to reduce unnecessary collection, exposure, or misuse of personal information.

PETs can help protect different aspects of privacy, including:

Confidentiality

Anonymity

Pseudonymity

Data minimization

Communication privacy

Location privacy

Identity protection

Examples of PETs include:

Virtual Private Networks (VPNs)

Tor

End-to-end encrypted messaging

Encryption

Anonymous communication systems

Privacy-preserving computation

Differential privacy

Data anonymization

TECHNOLOGIES SELECTED

For this practical, the following technologies are studied:

VPN

Tor

End-to-end encrypted messaging

Encryption

Differential privacy

WHAT IS A PRIVACY-ENHANCING TECHNOLOGY?

A Privacy-Enhancing Technology is a technical measure designed to help protect personal information and reduce privacy risks.

PETs do not necessarily make a person completely anonymous or eliminate every privacy risk.

For example, a VPN can encrypt traffic between a device and the VPN server, but it does not automatically make all online activity anonymous.

Similarly, end-to-end encryption protects message content from being read by unauthorized parties, but other information such as account or communication metadata may still exist depending on the service.

PET 1 – VIRTUAL PRIVATE NETWORK (VPN)

A VPN creates an encrypted connection between a user's device and a VPN server.

Simplified structure:

USER DEVICE
|
| Encrypted Connection
|
v
VPN SERVER
|
|
v
INTERNET

6.1 PURPOSE OF VPN

A VPN can help:

Protect network traffic from local network observers.

Secure traffic when using untrusted networks.

Hide the user's IP address from websites by presenting the VPN server's IP address.

Provide secure remote access to organizational networks.

6.2 ADVANTAGES OF VPN

Encrypts traffic between the device and VPN server.

Useful on public Wi-Fi.

Can help reduce exposure to local network monitoring.

Can provide secure remote access.

6.3 LIMITATIONS OF VPN

The VPN provider may be able to observe certain connection information.

A VPN does not automatically provide complete anonymity.

Websites can still use cookies, browser characteristics, accounts, or other tracking mechanisms.

VPN services differ in their privacy practices.

A VPN does not protect against malware or phishing by itself.

6.4 OBSERVATION

A VPN primarily provides protection for network traffic between the user and the VPN server. Trust in the VPN provider remains an important privacy consideration.

PET 2 – TOR

Tor stands for The Onion Router.

Tor is a network designed to help provide anonymity by routing traffic through multiple relays.

Simplified structure:

USER
|
v
GUARD RELAY
|
v
MIDDLE RELAY
|
v
EXIT RELAY
|
v
INTERNET

7.1 HOW TOR WORKS

Tor uses multiple layers of encryption and routes traffic through a series of relays.

Each relay generally knows only the information necessary for its part of the route.

This makes it more difficult for a single network observer to associate the user directly with the final destination.

7.2 ADVANTAGES OF TOR

Helps provide network-level anonymity.

Makes traffic correlation more difficult for some observers.

Can help users access websites without directly exposing their normal IP address.

Can provide access to privacy-oriented services.

7.3 LIMITATIONS OF TOR

Browsing can be slower.

Tor does not protect the user from every form of tracking.

Logging into a personal account can reveal the user's identity to that service.

Malicious websites can still present security risks.

Tor does not make a user immune to malware or phishing.

7.4 OBSERVATION

Tor provides stronger anonymity properties than a conventional VPN in some threat models, but it should not be treated as a guarantee of complete anonymity.

PET 3 – END-TO-END ENCRYPTED MESSAGING

End-to-end encryption (E2EE) is a method in which messages are encrypted on the sender's device and decrypted on the intended recipient's device.

Simplified model:

SENDER
|
| Encrypted Message
|
v
SERVER
|
| Encrypted Message
|
v
RECIPIENT
|
v
Decrypted Message

8.1 PURPOSE

The main purpose of E2EE is to prevent intermediaries from reading the content of messages while they are being transmitted or stored on servers.

8.2 ADVANTAGES

Protects message content from unauthorized interception.

Helps protect private conversations.

Reduces the ability of service infrastructure to read message content when properly implemented.

8.3 LIMITATIONS

Metadata may still be available depending on the service.

If a device is compromised, messages may be exposed.

Screenshots or forwarding can expose information.

Account compromise can create privacy risks.

E2EE does not protect users from social engineering.

8.4 OBSERVATION

E2EE is primarily designed to protect the content of communications rather than guarantee complete privacy in every aspect of communication.

PET 4 – ENCRYPTION

Encryption converts readable information into ciphertext.

Example:

Plaintext:
DATA PRIVACY

    |
    | Encryption
    v


Ciphertext:
[Unreadable Encrypted Data]

    |
    | Decryption
    v


Plaintext:
DATA PRIVACY

9.1 USES OF ENCRYPTION

Encryption can be used for:

Secure web communication.

Secure file storage.

Messaging.

Online banking.

Cloud storage.

Password and credential protection systems.

Secure databases.

9.2 ADVANTAGES

Protects confidentiality.

Reduces the impact of unauthorized access to encrypted data.

Can protect information both in transit and at rest.

9.3 LIMITATIONS

Encryption does not protect data after it has been legitimately decrypted.

Poor key management can compromise security.

Compromised endpoints can expose plaintext.

Weak passwords or insecure implementations can reduce protection.

PET 5 – DIFFERENTIAL PRIVACY

Differential privacy is a mathematical approach to limiting the privacy loss that can result from statistical analysis.

Instead of publishing exact information, a privacy mechanism can add controlled noise to statistical results.

Example:

Actual number of users = 1,000

Published result = 997

The difference is introduced to reduce the ability to determine whether a particular individual's information contributed to the result.

10.1 APPLICATIONS

Differential privacy can be used in:

Statistical analysis

Research

Census-type datasets

Machine learning

Data analytics

10.2 ADVANTAGES

Provides a mathematical privacy framework.

Can allow useful statistical analysis while reducing individual-level disclosure.

Can be applied to aggregate data.

10.3 LIMITATIONS

Adding too much noise can reduce data accuracy.

Correct privacy parameters must be selected.

It does not necessarily protect raw data if that raw data is separately exposed.

COMPARISON OF PETs

Technology	Main Purpose	Main Protection	Major Limitation
VPN	Secure network connection	Traffic confidentiality	Trust in VPN provider
Tor	Network anonymity	IP/network anonymity	Slower and not complete anonymity
E2EE	Secure communication	Message confidentiality	Metadata/endpoints may remain exposed
Encryption	Protect information	Confidentiality	Requires secure key management
Differential Privacy	Protect statistical information	Individual privacy in analysis	May reduce accuracy

EXPERIMENT – OBSERVING IP ADDRESS CHANGES WITH A VPN

AIM:

To understand how a VPN can change the public IP address presented to websites.

PROCEDURE:

Connect the computer to the internet.

Record the public IP address shown by an IP-checking service.

Connect to a trusted VPN service.

Check the public IP address again.

Compare the two IP addresses.

Disconnect the VPN.

Check the IP address again.

OBSERVATION:

Before VPN:

Public IP: __________________________

After VPN:

Public IP: __________________________

After Disconnecting VPN:

Public IP: __________________________

RESULT:

The experiment demonstrates that a VPN can cause websites to see the VPN server's public IP address instead of the user's normal public IP address.

EXPERIMENT – ENCRYPTION DEMONSTRATION

AIM:

To demonstrate the basic concept of encryption.

Example:

Original message:

"DATA PRIVACY"

After encryption:

"[Ciphertext]"

After decryption:

"DATA PRIVACY"

PROCEDURE:

Select a sample message.

Apply an encryption mechanism.

Observe the ciphertext.

Decrypt the ciphertext using the appropriate key.

Compare the decrypted message with the original.

OBSERVATION:

The encrypted message is not directly readable as ordinary plaintext. Using the appropriate decryption mechanism restores the original message.

RESULT:

The basic process of encryption and decryption was successfully demonstrated.

PRIVACY THREAT MODEL

A threat model identifies what needs to be protected and from whom.

Example:

ASSET:

Private communication

THREAT:

Network interception

PET:

End-to-end encryption

ASSET:

IP address

THREAT:

Network-level tracking

PET:

Tor or VPN

ASSET:

Statistical dataset

THREAT:

Individual identification from published statistics

PET:

Differential privacy

ASSET:

Stored confidential files

THREAT:

Unauthorized access

PET:

Encryption

PRIVACY-ENHANCING TECHNOLOGY SELECTION

The appropriate PET depends on the privacy requirement.

For secure public Wi-Fi:

VPN can be useful.

For network anonymity:

Tor can provide anonymity properties.

For private messaging:

End-to-end encryption can protect message content.

For protecting stored information:

Encryption can protect data at rest.

For publishing statistics:

Differential privacy can reduce individual-level privacy risks.

LIMITATIONS OF PETs

PETs are useful but do not provide absolute privacy.

Important limitations include:

No single technology protects against every privacy threat.

Incorrect configuration can reduce effectiveness.

Endpoints can be compromised.

Service providers may still collect metadata.

Users can accidentally disclose their own information.

Social engineering attacks are not prevented by encryption alone.

Privacy depends on the technology, implementation, configuration, and threat model.

BEST PRACTICES

The following practices can improve privacy:

Use strong and unique passwords.

Enable multi-factor authentication where available.

Use end-to-end encrypted messaging for sensitive communications.

Keep operating systems and applications updated.

Use encryption for sensitive stored data.

Be careful when using public Wi-Fi.

Understand the privacy policy of VPN providers.

Avoid entering unnecessary personal information online.

Review application permissions.

Use privacy-enhancing technologies according to the specific threat model.

FINDINGS

The practical produced the following findings:

Privacy-enhancing technologies address different privacy threats.

VPNs primarily protect traffic between the user and VPN server.

Tor provides network anonymity through multi-hop routing.

End-to-end encryption protects communication content from unauthorized intermediaries.

Encryption protects information from unauthorized access when correctly implemented.

Differential privacy helps reduce privacy risks in statistical data analysis.

No PET provides complete protection against all threats.

Proper configuration and user behavior are essential for effective privacy protection.

CONCLUSION

Privacy-Enhancing Technologies are important tools for reducing privacy risks in modern digital systems.

In this practical, VPNs, Tor, end-to-end encryption, encryption, and differential privacy were studied and compared.

The practical demonstrates that each technology addresses a different privacy problem. VPNs can protect network traffic from certain observers, Tor can provide anonymity properties, end-to-end encryption protects message content, encryption protects stored or transmitted information, and differential privacy helps protect individuals during statistical analysis.

However, PETs do not guarantee complete privacy. Their effectiveness depends on correct implementation, configuration, the user's behavior, and the specific threat model.

RESULT

The study and evaluation of Privacy-Enhancing Technologies was successfully completed. The working principles, advantages, limitations, and appropriate applications of VPNs, Tor, end-to-end encryption, encryption, and differential privacy were studied.

VIVA QUESTIONS AND ANSWERS

Q1. What is a PET?

Answer: PET stands for Privacy-Enhancing Technology. It is a technology or technique designed to reduce privacy risks and protect personal information.

Q2. What is a VPN?

Answer: A VPN creates an encrypted connection between a user's device and a VPN server and can hide the user's normal IP address from websites.

Q3. Does a VPN provide complete anonymity?

Answer: No. A VPN can improve privacy in certain situations but does not guarantee complete anonymity.

Q4. What is Tor?

Answer: Tor is a network that routes traffic through multiple relays to provide anonymity properties.

Q5. What is end-to-end encryption?

Answer: End-to-end encryption protects message content so that it is encrypted on the sender's device and decrypted on the intended recipient's device.

Q6. What is differential privacy?

Answer: Differential privacy is a mathematical framework for limiting privacy loss when information is learned from statistical data.

Q7. What is the main difference between VPN and Tor?

Answer: A VPN generally routes traffic through a VPN provider's server, while Tor routes traffic through multiple relays designed to provide anonymity properties.

Q8. Does encryption protect against malware?

Answer: No. Encryption protects information from certain forms of unauthorized access, but it does not by itself protect a device from malware.

Q9. Why is key management important?

Answer: If cryptographic keys are lost, stolen, or improperly managed, the security provided by encryption can be significantly reduced.

Q10. Can one PET protect against every privacy threat?

Answer: No. Different PETs address different threats, so technologies should be selected according to the specific privacy requirements and threat model.

REFERENCES

NIST Privacy Framework

NIST Cryptographic Standards and Guidelines

Tor Project Documentation

General references on Virtual Private Networks

General references on End-to-End Encryption

General references on Differential Privacy

Access Date: 17 September 2026
