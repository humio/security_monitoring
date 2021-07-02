# Windows Best Practice Security Monitoring
A Winlogbeat config that can form the basis of a security monitoring data collection effort.
This is an example of a way to implement and operationalize the NSAcyber guidance on what to log on a windows based OS
Addtional sources have been added to provide data needed to detect or determine a possible compromise or misconfiguration.

## Vision
This project should provide an easy way to get started with collecting data from windowsbased platforms in order to 
support SecOps and provide "forensic readiness" - before you need it, by having relevant monitoring in place before during and after a given IT securty incident.

Addtionally the data collected can be leveraged in conjuction with sigma rules from external sources or allow for custom quries and alerts to proactivly hunt for TTP in your infrastrucutue. 

provide the capability to prove what did not happen, should there be a case where you want to "go back and validate" against a priviously IOC or exploit.

Lastly we hope collecting the log data can help day to day hardning efforts or answer questions in relation discover root cause outside of SecOps use case. As this will allow you to know your infrastructure better than an adversary and thus gain leverage by being able to spot their activity in the inital phases of the cyber kill chain

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
If you haven't heard back from a maintainer within 7 days of creating an issue or making a pull request, please feel free to ping them on the relevant post.

Maintainers will also be in charge of both versioning and publishing future releases of the project. This includes adding versioning tags and adding to the changelog file.
 
The active maintainers involved with this project include:
  
   * [ssi@humio.com](https://github.com/ssi0202)

# Reference
https://github.com/nsacyber/Event-Forwarding-Guidance

Make sure to read the notes within the config file itself at it contains changes that needs to be implemented in order to gain full value of the logs you are collecting and ensure that the relavant eventids are generated correctly prior to enabling the event forwarding