# Authentication vs Identification

**Identification**, also known as recognition, has the goal of establish an **identity** from available information. It provides an answer to the question "Who are you?"

Authorization is the process of **using supported "evidence"** to corroborate an asserted (claimed) **identity**.
This means that authentication provides an answer to the question "Are you who you claim to be?"
The authentication of an "actor" is made by a user that interacts via software with hardware elements. **User authentication** is also called AuthN, which is different from AuthZ (authorization).

The authorization can use different **factors**: we typically have three levels of authentication, known as **1/2/3 factors authentication**. The three levels are:
- **Knowledge**: first factor is based on **something only the user knows** (PIN, password)
- **Ownership**: something **only the user possesses** (Smartphone, smart card, token)
- **Inherence**: something **the user is** (for example a **fingerprint**)
When more than one factor is employed we speak about **MFA (Multi-factor authentication)**.
Each factor has cons:
- Knowledge has risks related to storage and demonstration
- Ownership: theft, cloning, unauthorized use
- Inherence: counterfeiting and privacy
# Digital authentication model

This model was defined by NIST.

![[Pasted image 20241016102604.png]]

The applicant is the person that is trying to authenticate himself.
The applicant is being asked to provide an **authenticator enrollment**, if the process has success the applicant become a subscriber.
The system needs to verify if the enrollment is correctly bind to the identity.
The verifier has the goal to verify the credentials.
#