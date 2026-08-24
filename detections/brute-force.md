\# Brute Force Detection



\## Objective



Detect repeated failed login attempts on a Windows endpoint.



\## Data Source



\- Windows Security Event Log

\- Wazuh

\- Event ID 4625



\## Detection Logic



Repeated Event ID 4625 events from the same source

may indicate a brute-force or password-guessing attempt.



\## Investigation



The following information should be analyzed:



\- Source IP

\- Target username

\- Timestamp

\- Number of failed attempts

\- Target host

\- Successful login after failed attempts



\## MITRE ATT\&CK



Technique: T1110 - Brute Force



\## Conclusion



Further investigation is required to determine whether

the activity represents malicious password guessing.

