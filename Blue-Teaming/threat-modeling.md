
# Table of Contents

1.  [Threat Modeling](#org736d795)
    1.  [Principles of Threat Modeling](#orgedbeadc)
    2.  [Threat Modeling Frameworks](#org54d3042)
        1.  [STRIDE Framework](#org3d1448d)
        2.  [PASTA Framework](#orge27d374)
2.  [Incident Response](#org4bac147)
    1.  [Incident Classification](#org29dac12)
    2.  [Computer Security Incident Response Team (CSIRT)](#org1c92f7b)
    3.  [Six Phases of Incident Response](#org0923ae8)
3.  [Implement threat modeling exercise for our web application](#org2264dad)
4.  [Create incident response playbook for common scenarios](#org31c67fd)
5.  [Resources](#orgd9a6fe0)



<a id="org736d795"></a>

# Threat Modeling

Threat modelling is the process of reviewing, improving, and testing the security protocols in place in an organisation&rsquo;s information technology infrastructure and services.

A critical stage of the threat modelling process is identifying likely threats that an application or system may face, the vulnerabilities a system or application may be vulnerable to.


<a id="orgedbeadc"></a>

## Principles of Threat Modeling

The threat modelling process is very similar to a risk assessment made in workplaces for employees and customers. The principles all return to:

-   Preparation
-   Identification
-   Mitigations
-   Review

It is, however, a complex process that needs constant review and discussion with a dedicated team. An effective threat model includes:

-   Threat intelligence
-   Asset identification
-   Mitigation capabilities
-   Risk assessment


<a id="org54d3042"></a>

## Threat Modeling Frameworks

To help with this, there are frameworks such as STRIDE and PASTA (Process for Attack Simulation and Threat Analysis).


<a id="org3d1448d"></a>

### STRIDE Framework

STRIDE, authored by two Microsoft security researchers in 1999 is still very relevant today. STRIDE includes six main principles:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
<caption class="t-above"><span class="table-number">Table 1:</span> STRIDE Principles and Descriptions</caption>

<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Principle</th>
<th scope="col" class="org-left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="org-left">Spoofing</td>
<td class="org-left">This principle requires you to authenticate requests and users accessing a system. Spoofing involves a malicious party falsely identifying itself as another. Access keys (such as API keys) or signatures via encryption helps remediate this threat.</td>
</tr>

<tr>
<td class="org-left">Tampering</td>
<td class="org-left">By providing anti-tampering measures to a system or application, you help provide integrity to the data. Data that is accessed must be kept integral and accurate. For example, shops use seals on food products.</td>
</tr>

<tr>
<td class="org-left">Repudiation</td>
<td class="org-left">This principle dictates the use of services such as logging of activity for a system or application to track.</td>
</tr>

<tr>
<td class="org-left">Information Disclosure</td>
<td class="org-left">Applications or services that handle information of multiple users need to be appropriately configured to only show information relevant to the owner.</td>
</tr>

<tr>
<td class="org-left">Denial of Service</td>
<td class="org-left">Applications and services use up system resources, these two things should have measures in place so that abuse of the application/service won&rsquo;t result in bringing the whole system down.</td>
</tr>

<tr>
<td class="org-left">Elevation of Privilege</td>
<td class="org-left">This is the worst-case scenario for an application or service. It means that a user was able to escalate their authorization to that of a higher level i.e. an administrator. This scenario often leads to further exploitation or information disclosure.</td>
</tr>
</tbody>
</table>


<a id="orge27d374"></a>

### PASTA Framework

PASTA (Process for Attack Simulation and Threat Analysis) - &ldquo;infosec never tasted so good!&rdquo;


<a id="org4bac147"></a>

# Incident Response

A breach of security is known as an incident. And despite all rigorous threat models and secure system designs, incidents do happen. Actions taken to resolve and remediate the threat are known as Incident Response (IR) and are a whole career path in cybersecurity.


<a id="org29dac12"></a>

## Incident Classification

Incidents are classified using a rating of urgency and impact:

-   Urgency: determined by the type of attack faced
-   Impact: determined by the affected system and what impact that has on business operations


<a id="org1c92f7b"></a>

## Computer Security Incident Response Team (CSIRT)

An incident is responded to by a Computer Security Incident Response Team (CSIRT) which is prearranged group of employees with technical knowledge about the systems and/or current incident.


<a id="org0923ae8"></a>

## Six Phases of Incident Response

To successfully solve an incident, these steps are often referred to as the six phases of Incident Response:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
<caption class="t-above"><span class="table-number">Table 2:</span> Six Phases of Incident Response</caption>

<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Action</th>
<th scope="col" class="org-left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="org-left">Preparation</td>
<td class="org-left">Do we have the resources and plans in place to deal with the security incident?</td>
</tr>

<tr>
<td class="org-left">Identification</td>
<td class="org-left">Has the threat and the threat actor been correctly identified in order for us to respond to?</td>
</tr>

<tr>
<td class="org-left">Containment</td>
<td class="org-left">Can the threat/security incident be contained to prevent other systems or users from being impacted?</td>
</tr>

<tr>
<td class="org-left">Eradication</td>
<td class="org-left">Remove the active threat.</td>
</tr>

<tr>
<td class="org-left">Recovery</td>
<td class="org-left">Perform a full review of the impacted systems to return to business as usual operations.</td>
</tr>

<tr>
<td class="org-left">Lessons Learned</td>
<td class="org-left">What can be learnt from the incident? I.e. if it was due to a phishing email, employees should be trained better to detect phishing emails.</td>
</tr>
</tbody>
</table>


<a id="org2264dad"></a>

# TODO Implement threat modeling exercise for our web application

-   [ ] Identify assets and data flows
-   [ ] Apply STRIDE methodology
-   [ ] Document potential threats
-   [ ] Propose mitigations


<a id="org31c67fd"></a>

# TODO Create incident response playbook for common scenarios

-   [ ] Ransomware incident
-   [ ] Data breach
-   [ ] DDoS attack
-   [ ] Phishing campaign


<a id="orgd9a6fe0"></a>

# Resources

-   [OWASP Threat Modeling](https://owasp.org/www-community/Threat_Modeling)
-   [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
-   [NIST SP 800-61: Computer Security Incident Handling Guide](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf)

