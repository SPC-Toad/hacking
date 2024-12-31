# Junior pen testing path

## Defense in Depth
- Definition: Defense in Depth is the use of multiple varied layers of security to an organization's systems and data in the hopes that multiple layers will provide redundancy in an organization's security perimeter.

## CIA Triad (no this is not CIA.gov, this is made by NIST.gov)
- This is the security model that has become the industry standard.
1. Confidentiality
    - This element is the protection of data from unauthorized access and misuse
2. Integrity
    - Information is kept accurate and consistent unless authorized changes are made.
3. Availability
    - Information should be available when authorized users need to access it


## Privilege

### Privileged Identity Management (PIM) 
- Translate a user's role within an organization into an access role on a system.

### Privileged Access Management (PAM)
- The management of the privileges a system's access role has, amongst other thing

### Model for Confidentiality
- The Bell-La Padula Model
    - The Bell-La Padula Model is used to achieve confidentiality. This model has a few assumptions:
        1. Well defined organization's hierarchical structure
        2. Everyone's responsibilities/roles are well-defined.
    - How it works:
        - `no write down, no read up`
        - Example:
            - Person with TS/SCI can read Secret documents.
            - Person with Secret can not read the TS/SCI documents (might know the existence)
    
    <table style="width: 100%;">
        <tr>
            <th>
            advantage
            </th>
            <th>
            disadvantage
            </th>
        </tr>
        <tr>
            <th>
            Policies in this model can be replicated to real-life organisations hierarchies (and vice versa)
            </th>
            <th>
            Even though a user may not have access to an object, they will know about its existence -- so it's not confidential in that aspect.
            </th>
        </tr>
        <tr>
            <th>
            Simple to implement and understand, and has been proven to be successful.advantage
            </th>
            <th>
            The model relies on a large amount of trust within the organisation.
            </th>
        </tr>
    </table>

### Model for Integrity
- Biba Model
    - The Biba model is arguably the equivalent of the Bell-La Padula model but for the integrity of the CIA triad.
    - How it works:
        - `no write up, no read down`
        - Example:
            - No write up: A subject cannot write to an object at a higher integrity level. This prevents low-integrity subjects from contaminating high-integrity data.
        - No read down: A subject cannot read an object at a lower integrity level. This prevents high-integrity subjects from being corrupted by low-integrity data.
    
### STRIDE
<table border="1" style="border-collapse: collapse; width: 100%;">
        <thead>
            <tr>
                <th>Principle</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Spoofing</td>
                <td>This principle requires you to authenticate requests and users accessing a system. Spoofing involves a malicious party falsely identifying itself as another. Access keys (such as API keys) or signatures via encryption help remediate this threat.</td>
            </tr>
            <tr>
                <td>Tampering</td>
                <td>By providing anti-tampering measures to a system or application, you help provide integrity to the data. Data that is accessed must be kept integral and accurate. For example, shops use seals on food products.</td>
            </tr>
            <tr>
                <td>Repudiation</td>
                <td>This principle dictates the use of services such as logging of activity for a system or application to track.</td>
            </tr>
            <tr>
                <td>Information Disclosure</td>
                <td>Applications or services that handle information of multiple users need to be appropriately configured to only show information relevant to the owner.</td>
            </tr>
            <tr>
                <td>Denial of Service</td>
                <td>Applications and services use up system resources, these two things should have measures in place so that abuse of the application/service won't result in bringing the whole system down.</td>
            </tr>
            <tr>
                <td>Elevation of Privilege</td>
                <td>This is the worst-case scenario for an application or service. It means that a user was able to escalate their authorization to that of a higher level i.e. an administrator. This scenario often leads to further exploitation or information disclosure.</td>
            </tr>
        </tbody>
    </table>

### Incident
- A breach of security 

### Incident Response (IR)
- Actions taken to resolve and remediate the threat 

### Computer Security Incident Response Team (CSIRT)
- Pre-assigned group of employees with technical knowledge about the systems and/or current incident

#### Always reduce the attack surface!
- This can be assigning the minimum privilege level to users