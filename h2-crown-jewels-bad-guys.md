# Homework 2

## Read and summarize
* Advanced Persistent Threats (APTs) are a class of threats aimed at compromising data for economic or military purposes. APTs are manually operated and differ from automated viruses and worms, which organizations have traditionally focused on mitigating.
* Traditional approaches, such as anti-virus software and patching, are insufficient to defend against APTs. APT actors use advanced tools, customized malware, and "zero-day" exploits that are not detectable or mitigatable by these methods.
* The "kill chain" model is a structure for analyzing the phases of an intrusion and guiding analysis for actionable security intelligence. The model emphasizes that APT adversaries must progress through each stage successfully, and one mitigation can disrupt the entire chain.
* Hutchins et al 2011 advocate for an intelligence-driven, threat-focused approach to study APT intrusions from the adversary's perspective. They highlight that intelligence-driven defense can lead to a more resilient security posture, and defenders can gain an advantage over APT actors by implementing countermeasures faster than adversaries can evolve.
* Threat modeling is a structured approach to identifying, understanding, and mitigating security threats in the design and development of software and systems. It emphasizes the importance of proactive security measures.
* Threat modeling requires asking yourself the following four key questions: 
  *  What are you building?
	*  What can go wrong?
	*  What should you do about these things that can go wrong?
	*  Did you do a decent job of analyzing these things?
*  STRIDE is a mnemonic that describes what can go wrong in security. The word is made from Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, and Elevation of Privilege.
	
The concept of intrusion kill chain is in my opinion a very powerful approach in the realm of cybersecurity. It offers a systematic way to understand and combat security breaches, which is valuable not only for organizations but also for individuals concerned about their online safety. Working in the field of software development, the kill chain model is quite relevant to my line of work as it provides a structured methodology for dealing with advanced threats like APTs. This approach helps in detecting, analyzing, and responding to intrusions effectively. 


## Make-belief boogie-man. Create a treath model for imaginary company.

My imaginary company is an airline company that specializes in luxury air travel. The company offers private jet services to elite clients, ensuring a seamless and secure travel experience. Their clients include high-profile individuals, corporate executives, and government officials.

Some of the business requirements are:
* Data Privacy and Security: the company deals with sensitive customer information, including travel itineraries, personal details, and payment information. Protecting this data from breaches and ensuring the privacy of their clients is paramount.
* Operational Continuity: the company must maintain uninterrupted services. Any disruption in flight schedules or critical system downtime would not only result in financial losses but also harm their reputation.
* High-Level Service: ensuring the safety and comfort of their clients during air travel is essential to the business. Any compromise in this area could result in a loss of clients and reputation damage.

Threat analysis:
There are various things that could potentially go wrong if the system is not protected properly. Below the STRIDE Mnemonic is used to discover some threats:

1. What can go wrong?
  * Spoofing:
     * Unauthorized individuals may attempt to spoof their identity to gain access to customer data or systems.
  * Tampering:
    * Malicious actors might tamper with flight scheduling systems or in-flight security controls.
  * Repudiation:
    * Customers or employees may deny their involvement in particular activities, such as confirming a flight booking.
  * Information Disclosure:
    * Inadequate protection of customer data may lead to unauthorized information disclosure.
  * Denial of Service:
    * Malicious actors may attempt to disrupt flight scheduling systems or in-flight services.
  * Elevation of Privilege:
    * Unauthorized users may exploit vulnerabilities to gain elevated privileges in booking or scheduling systems.

 2. What are we going to do about it?
	* Implement strong authentication mechanisms, such as multi-factor authentication, to ensure the validity of user identities.
	* Implement strong encryption for customer data.
	* Use secure communication protocols to protect data in transit.
	* Maintain detailed logs of customer interactions and system activities, including flight bookings.
	* Strict access controls and authentication mechanisms to protect data.
	* Regularly audit and monitor systems for suspicious activities.
	* Use load balancing and redundancy in critical systems to ensure high availability and reduce the risk of service disruptions.
	• Regularly update and patch system components to address known vulnerabilities.

 3. Did we do a good enough job?
	* The effectiveness of these measures will be continuously assessed through regular security audits, compliance checks, and real-time monitoring of systems. Any incidents or breaches will trigger incident response protocols and post-incident analysis to enhance security practices continually.

## Incident analyses: Equifax Data Breach

The Equifax data breach in 2017 was a significant cyber incident where the personal and financial data of approximately 143 million Americans was compromised. Attackers exploited a vulnerability in the Apache Struts web application to gain unauthorized access to sensitive customer information. (Fruhlinger, 2020) Below is the analysis using the cyber kill chain framework:

1. Reconnaissance:
Attackers likely conducted initial reconnaissance to identify vulnerable targets. In this case, Equifax's web applications containing sensitive data.

2. Weaponization:
The attackers weaponized the vulnerability in the Apache Struts web application framework to craft a specific attack payload.

3. Delivery:
Attackers delivered the malicious payload through a targeted web application using the identified vulnerability.

4. Exploitation:
The vulnerability in the web application was exploited, providing unauthorized access to Equifax's systems.

5. Installation:
Once inside the network attackers likely installed malware or backdoors to maintain persistence and control over the compromised systems.

6. Command and Control (C2):
Attackers established command and control channels to communicate with the compromised systems which allowed them to execute commands and extract data.

7. Actions on Objectives:
With persistent access and control the attackers exfiltrated massive amounts of sensitive customer data, such as names, social security numbers, birthdays and credit card information.

## Starting a lab. Installing Debian on virtual box.
The first step was to install virtalbox on my windows 10 machine. In order to do that I downloaded the installer and run it. After the virtualbox was installed, the next step was to download the debian image for which amd64 was the correct one for my machine. After that I opened virtualbox and created a new virtual machine, typed the name for my virtual machine "DebianTest", chose the type Linux, version Debian 64bit, memory size 2000MB and hard disc 20GB. After that I selected the downloaded Debian iso image from the virtual CDROM under the Storage tab in settings. After that I booted the machine and followed the OS installation steps.


## References:
Hutchins et al, 2011. "Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains". Available at: https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf

Federal Trade Commission, 2022. "Equifax Data Breach Settlement". Available at: https://www.ftc.gov/enforcement/refunds/equifax-data-breach-settlement

Fruhlinger, J., 2020. "Equifax data breach FAQ: What happened, who was affected, what was the impact?". Available at: https://www.csoonline.com/article/567833/equifax-data-breach-faq-what-happened-who-was-affected-what-was-the-impact.html

Shostack, A., 2014. "Dive In and Threat Model!".
