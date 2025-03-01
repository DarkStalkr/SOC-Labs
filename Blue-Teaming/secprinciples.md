
# Table of Contents

1.  [Principles of Security](#org26cb8cc)
    1.  [CIA Triad](#org11e91cf)
        1.  [Confidentiality](#orga1c2861)
        2.  [Integrity](#org8a6d186)
        3.  [Availability](#org23f93f2)
    2.  [Principles of Privileges](#org63c8ddd)
        1.  [PIM & PAM](#org3a823c8)
    3.  [Security Policies Models](#orgfc232f8)
        1.  [Bell-La Padula Model](#org3e47c68)
        2.  [Biba Integrity Model](#org471554d)
        3.  [Clark-Wilson Model](#orga149cf3)
    4.  [Implement lab demonstration of Bell-La Padula model](#org7004309)
    5.  [References](#orgf3c8995)



<a id="org26cb8cc"></a>

# Principles of Security


<a id="org11e91cf"></a>

## CIA Triad


<a id="orga1c2861"></a>

### Confidentiality

Information is only accessible to authorized individuals.


<a id="org8a6d186"></a>

### Integrity

Data remains accurate and unmodified during storage and transmission.


<a id="org23f93f2"></a>

### Availability

Systems and data are accessible when needed.


<a id="org63c8ddd"></a>

## Principles of Privileges

Levels of access can be given to individuals based of 2 primarily factors:

1.  The individual&rsquo;s role/functions within the organisation.
2.  The sensitivity of the information being stored on the system.


<a id="org3a823c8"></a>

### PIM & PAM

1.  Privileged Identity Management (PIM)

    -   Monitors and manages privileged accounts
    -   Provides just-in-time access to privileged resources
    -   Follows principle of least privilege

2.  Privileged Access Management (PAM)

    -   Controls and monitors privileged access
    -   Implements session recording and auditing
    -   Manages credential vaulting


<a id="orgfc232f8"></a>

## Security Policies Models


<a id="org3e47c68"></a>

### Bell-La Padula Model

Works by granting access users pieces of data, only on their need to know basis:

-   Uses a hierarchical structure
-   No write down, no read up model

    ┌────────────────┐
    │  TOP SECRET    │
    └────────────────┘
            ▲
            │ No Read Up
            │
    ┌────────────────┐
    │    SECRET      │
    └────────────────┘
            ▲
            │
    ┌────────────────┐
    │  CONFIDENTIAL  │
    └────────────────┘
            ▲
            │
    ┌────────────────┐
    │  UNCLASSIFIED  │
    └────────────────┘
            │
            ▼ No Write Down

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
<caption class="t-above"><span class="table-number">Table 1:</span> Bell-La Padula Model Evaluation</caption>

<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Advantages</th>
<th scope="col" class="org-left">Disadvantages</th>
</tr>
</thead>
<tbody>
<tr>
<td class="org-left">Policies related in this model can be replicated to real life organizations</td>
<td class="org-left">Users may not have access to pieces of information, but will know of their existence</td>
</tr>

<tr>
<td class="org-left">Provides strong confidentiality protection</td>
<td class="org-left">May inhibit information sharing and collaboration</td>
</tr>

<tr>
<td class="org-left">Well-suited for military and government applications</td>
<td class="org-left">Doesn&rsquo;t address integrity concerns</td>
</tr>
</tbody>
</table>


<a id="org471554d"></a>

### Biba Integrity Model

-   Focuses on data integrity rather than confidentiality
-   No read down, no write up
-   Prevents data corruption from lower integrity levels


<a id="orga149cf3"></a>

### Clark-Wilson Model

-   Uses transformation procedures to maintain integrity
-   Implements separation of duties
-   Enforces well-formed transactions


<a id="org7004309"></a>

## TODO Implement lab demonstration of Bell-La Padula model

-   [ ] Set up user accounts with different clearance levels
-   [ ] Demonstrate read/write restrictions
-   [ ] Document findings


<a id="orgf3c8995"></a>

## References

-   [NIST SP 800-12: An Introduction to Information Security](https://csrc.nist.gov/publications/detail/sp/800-12/rev-1/final)
-   [NIST SP 800-53: Security and Privacy Controls](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r5.pdf)

