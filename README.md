# Windows Best Practice Security Monitoring
A Winlogbeat config that can form the basis of a security monitoring data collection effort.
This is an example of a way to implement and operationalize the NSAcyber / CFCS guidance on what to log on a windows based OS
Addtional sources have been added to provide data needed to support detection capability and identify and adress misconfiguration.

## Vision
This project should provide an easy way to get started with collecting data from windowsbased platforms in order to 
support SecOps and "Forensic Readiness" - before you need it, order for you to have it when you need it. By having relevant monitoring in place before during and after a given IT security incident.

Addtionally the data collected can be leveraged in conjuction with sigma rules or custom streaming queries and alerts to proactivly hunt for TTP's in your infrastrucuture. 

Another thing we aim to provide is the capability to prove what did not happen. Likewise, should there be a case where you want to "go back and validate" against new IOC data, published exploit being attempted (ex. via sigma rule) or determine how "deep" a given intrusion actually was.

Lastly we hope collecting the log data can help day to day hardning efforts or answer questions in relation root cause analysis outside of SecOps use case. 

knowing your infrastructure better than an adversary translates into leverage, as you become able to spot their activity in the inital phases of the cyber kill chain.

## Governance
This project is maintained by employees at Humio ApS.
As a general rule, only employees at Humio can become maintainers and have commit privileges to this repository.
Therefore, if you want to contribute to the project, which we very much encourage, you must first fork the repository.
Maintainers will have the final say on accepting or rejecting pull requests.
As a rule of thumb, pull requests will be accepted if:
 
   * The contribution fits with the project's vision
   * All automated tests have passed
   * The contribution is of a quality comparable to the rest of the project
 
The maintainers will attempt to react to issues and pull requests quickly, but their ability to do so can vary.
If you haven't heard back from a maintainer within 7 days of creating an issue or making a pull request, please feel free to ping them on the relevant post in the Humio community slack channel

Maintainers will also be in charge of both versioning and publishing future releases of the project. This includes adding versioning tags and adding to the changelog file.
 
The active maintainers involved with this project include:
  
   * [ssi@humio.com]

# Reference
https://github.com/nsacyber/Event-Forwarding-Guidance

https://cfcs.dk/globalassets/cfcs/dokumenter/vejledninger/cfcs-vejledning-logning.pdf (in Danish)

Make sure to read the notes within the config file itself at it contains changes that needs to be implemented in order to gain full value of the logs you are collecting and ensure that the relavant eventids are generated correctly prior to enabling the event forwarding
