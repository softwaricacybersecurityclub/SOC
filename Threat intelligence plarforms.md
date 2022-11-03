## What is cyber threat intelligence?
`Threat intelligence is the analysis of adversaries — their capabilities, motivations, and goals; and cyber threat intelligence (CTI) is the analysis of how adversaries use the cyber domain to accomplish their goals.`

Cyber threat intelligence is what cyber threat information becomes when it has been gathered, assessed in light of its dependability and source, and analyzed using rigorous and structured tradecraft processes by persons with in-depth knowledge and access to all available data. Like all intelligence, cyber threat intelligence adds value to cyber threat information by helping the consumer discover threats and opportunities while lowering their level of uncertainty.

>  Intelligence Definition: Taking in the external information from a variety of sources and analyzing it against existing requirements in order to provide an assessment that will affect decision making.

## How to define threat?
> **combination of intent, capability and opportunity.**

**Intent** is a malicious actor’s desire to target your organization 

**Capability** is their means to do so (such as specific types
of malware)

**Opportunity** is the opening
the actor needs (such as
vulnerabilities, whether it be
in software, hardware, or
personnel)

## Thread Data vs. Information vs. Intelligence
![[Pasted image 20221102080416.png]]
**Data**: Raw data collected from the environment 
**Information**: Answers questions using data and environment context 
**Intel**: Uses information + human analysis to drive Intel action and prioritize defensive actions 

## Threat Intelligence Platform Features 
Much of the Blue Team alerting will be based on indicator lists 
 * Known bad IPs, domains, hashes, etc.
Need a solution to: 
* Store analysis and threat information for known indicators 
* Perform automated / fast lookups via API 
* Record context about stored items (NOT just list)
    * Ex: IP 1.2.3.4 resolved to evilsite.com serving exploit kit on 2018-02-19 
* Find associations across multiple events 
* Sharing of indicators with other organizations 

## TIP Workflow

![[Pasted image 20221102081822.png]]

## Threat Intelligence Platform Products 
Self-Hosted, Free:
* MISP (Malware Information Sharing Platform) 
* CIF (Collective Intelligence Framework) 
* YETI (Your Everyday Threat Intelligence) 
* CRITS (Collaborative Research Into Threats) 
Cloud, Commercial: 
* ThreatConnect 
* AlienVault OTX 
* Threat Quotient 
* Anomali 

### MISP
** Why MISP? **
* A free, open-source analyst favorite 
* Capability of high-volume indicator storage 
* Great web UI and REST API interface 
* Classification and sharing functionality 
* Flexible indicator storage 
* Easy import/export 
* Integrates with TheHive for automated storage/analysis 

### MISP Workflow Overiew
Analyst Usage:
* Analyst creates new event
* All indicators, links, files, and notes are added as attributes
* Tags and other classifications (galaxies) applied
* Event reviewed, published to other organizations (if desired)

Automated usage through SOC tools:
* SIEM, SOAR, IMS use API to look up or push attributes to event
* Subscribed feeds automatically download external event data
* Anytime any of them are seen in live traffic = Alert

### MISP Event Illustration
 
![[Pasted image 20221102083921.png]]


 
 
