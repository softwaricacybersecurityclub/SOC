** Requirement  of SOC solutions: **
* Track all alerts and potential incidents
* Collect and organize threat intelligence
* Log correlation, enrichment and alerting 
* Automation of invetigation actions
* Making a repository of security team documents and info

### Tools for SOC Data Organization and Search

**Incident Management System (IMS)**
* Tracking alerts, incident status and associated indicators
* Otherwise known as Security Incident Response Platforms (SIRP)

**Threat Intelligence Platform (TIP)**
* Collection of indicators and higher-level intelligence info

**Security Information and Event Management (SIEM)**
* Log collection, indexing, search, correlation and alerting

**Security Orchestration, Automation and Response (SOAR)**
* Automation of common tasks, orchestration of workflow

**Knowledge Database / Source Code Repositories**
* For all SOC documents/code, playbooks, and use cases

### Options of IMS

**Options**
1. Traditional ticketing solutions
2. SIEM built-in solutions
3. Security-tailored ticketing 

**Traditional Ticketing **
* BMC Remedy
* RT 
* Redmine

**Commercial, security-oriented **
* Resilient
* Archer
* ServiceNOW
* CyberCPR

**Open Source, security-oriented**
* Thehive
* RTIR - Req. Tracker for IR
* FIR - Fast Incident Response

### Incident Management Systems - Systems View
* IMS receives alerts, creates case in ticket queue
* Cases assigned to analysts by cases or specific task
* Analyst works case to completion or escalates
* Associate observables with cases across time

![[Pasted image 20221017165648.png]]

### Incident Management System Features
1. Incident management systems vary greatly
2. Test them carefully before choosing one
3. Commercial is not always better than open-source
4. This will be one of your main tools; **you MUST enjoy using it**

**Some non-obvious, but important and useful features include:**

* Rich text .
+ Inline pictures / tables .
+ Indicator database integration .
* Mass close/open/edit actions .
* Hierarchical tickets .
* API .
* Tagging / attack-cycle alignment
* Keyboard navigation
* Built in knowledge database/wiki
* Workflow customization
* Automation / API access
* Activity "wall"

### TheHive: IMS

* Outstanding free IMS: Used for class virtual machine
* Incidents are organized and assigned by case
	* Cases follow steps in a pre-made case template (playbooks)
	* Cases have tasks that to be completed
	* Tasks have associated worklogs
	* Cases can have observables assigned to them
	* Observables can be enriched by analyzers enabled in Cortex engine

#### Playbooks

Playbooks mean different things to different SOCs
*In this class: "a set of expected actions for alert response"*
* Often implemented through your IMS or SOAR platform
* Contain required and optional steps for analysis and closure
* Guide analysts toward standardized analysis and completeness
* Unique for each type of case (phishing vs. malware playbooks)

**TheHive: Workflow Illustrated**

![[Pasted image 20221017173927.png]]

#### TheHive: Automatic Case Creation with Context
1. Events collected in SIEM, items of interest become alerts
2. Alerts sent to TheHive for triage
* New case created for all accepted alerts
3. Case is populated with field from alert:
* Parses fields from alert
* IP addresses, domains, usernames, hostnames, etc.
* Pulls in additional info if available
* Tasks created from designated case template (playbook)

 `Case names shoold be meaningfull and convey priority`

**Cisco SOC/ book, Crafting the InfoSec Playbook**
`{ UNIQUE_ID}-{HF, INV}-{$EVENTSOURCE }-
{SREPORT CATEGORY}: $DESCRIPTION `
1. ID: Most significant digits indicate source
2. "High-Fidelity" or "Investigative" detection
3. Event Source: Correlates with unique ID
4. Category: Malware, Policy, APT, etc.
5. Description of what the rule attempts to detect

#### TheHive: Working a case 
Assigned tasks show up in "My tasks"

![[Pasted image 20221018074150.png]]
Tasks can be part of task groups
* Investigation Questions: Aligned with "kill chain" or other
    * Delivery: "How many malicious emails were delivered? Where did it come from?"
    * Exploit/Install: "What exploit does the file use? What files does it drop?”
    * C2: "What domain is used for command and control?”
* Response Actions
    * "Delete message from all inboxes"
    * "Reset all compromised passwords"
     * "Submit sample to antivirus vendor"

Tasks populated from case template (playbook) must be completed.

#### TheHive: case and task assignment

**Both cases and tasks can be assigned to an analyst
* Not all IMSs do this - more granular assignment
* Enables easier collaborative / tierless SOC operations
` Newer analytst takes easier tasks then a professonal one.`

![[Pasted image 20221018122748.png]]
Fig- Case Template in TheHive

#### Incident Categorization Frameworks
There are many options for categorization. Here are a few:
1. VERIS: Vocabulary for Event Recording and Incident Sharing
* Captures 4 A's: Actor, Action, Asset, and Attributes (how affected)
* Yearly DBIR report data collected in this format
2. US-CERT Incident Reporting System Categories
+ Medium-level detail &
+ Designates "what" and "how" and impact 
3. Tags
+ Track any arbitrary data

#### Classification Options: VARIS

**Actor:** Whose actionns affected asset?
**Action:** What actions affected the asset?
**Assets:** Which assets were affected?
**Attributes:** How was the asset affected?
![[Pasted image 20221018123945.png]]

#### US-CERT Incident Categorization
NCISS-based scores from 0-100 based on weighted categories:
* Functional: "No impact" to "DoS/Loss of Control"
* Information: "No impact" to "Destruction of critical system"
* Recoverability: "Regular" to "Not recoverable"
* Attack Vectors
	* Web, Phishing, Ext. Media, Impersonation, Improper Usage, Theft, etc.
* Incident Attributes
   * Location of Observed Activity — "DMZ" through "Safety Systems"
   * Actor characterization and potential impact

#### Incident Management System Summary
Your IMS is one of the most important pieces of software!
- Test the interface, or you will be miserable!
- Cases should be created from alerting source
- Context from alert should be parsed into fields
- Task level assignment makes work balancing easy
- Observables should be entered — ideally automatically
- Playbooks guide you through tasks
- Close with categorizations for metrics
