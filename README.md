# Windows Best Practice Monitoring
A logcollector config that can form the basis of a windows based infrastructure Observability effort.

Initially build from a security monitoring perspective the Logscale Logcollector config has been expanded to facilitate observability for OPS teams in general. 

Initially conceived as a way to implement and operationalize the NSAcyber / CFCS guidance on what to log on a windows based OS.
Addtional sources have been added to provide data needed to support detection capability and identify and adress misconfigurations.

## Please read the references below to ensure your windows OS is configured correctly to generate the logs and/or events in the config.

Make sure to read the notes within the config file itself at it contains changes that needs to be implemented in order to gain full value of the logs you are collecting and ensure that the relavant eventids are generated correctly prior to enabling the event forwarding. 

If you plan to use winlogsbeat (non native logscale collector)use the OSS Version of winlogbeat/logstash in conjuction with Logscale.

## Vision
This project should provide an easy way to get started with collecting data from windows based platforms in order to 
build observability for all OPS and provide "Forensic Readiness" - before you need it. By having relevant monitoring in place before during and after a given incident reguardless if its security or windows infrastructure related.

From a security perspectuve the data collected can be leveraged in conjuction with sigma rules or custom streaming queries and alerts to proactivly hunt for TTP's in your infrastrucuture. In a similar fashion other ops teams can create alerting and dashboards of the data collected for their (non secops) use cases. the logdata have great value in diffrent use cases. Reguardless if its finding and fixing root cause, part of hardning efforts - having logs and the observability they provide on tab is a fundemental need for any OPS

Addtionally we aim to provide is the capability to prove what did not happen. Likewise, should there be a case where you want to "go back and validate" against new IOC data, published exploit being attempted (ex. via sigma rule) or determine how "deep" a given intrusion actually was. Similarly for other OPS depts, being able to rule out causes of incidents and poor performance helps.

Lastly we hope collecting the log data can help day to day hardning efforts or answer questions in relation root cause analysis outside of SecOps use case. 

Knowing your infrastructure is  key for all OPS teams in their day to day work with managing, building and changing infrastructure in a for the business safe and reliable manner.

## Governance
This project is maintained by employees at CrowdStrike
As a general rule, only employees at CrowdStrike can become maintainers and have commit privileges to this repository.
Therefore, if you want to contribute to the project, which we very much encourage, you must first fork the repository.
Maintainers will have the final say on accepting or rejecting pull requests.
As a rule of thumb, pull requests will be accepted if:
 
   * The contribution fits with the project's vision
   * All automated tests have passed
   * The contribution is of a quality comparable to the rest of the project
 
The maintainers will attempt to react to issues and pull requests quickly, but their ability to do so can vary.
If you haven't heard back from a maintainer within 7 days of creating an issue or making a pull request, please feel free to ping them on the relevant post in the Humio community slack channel

Maintainers will also be in charge of both versioning and publishing future releases of the project. This includes adding versioning tags and adding to the changelog file.

# Reference
https://github.com/nsacyber/Event-Forwarding-Guidance

https://cfcs.dk/globalassets/cfcs/dokumenter/vejledninger/cfcs-vejledning-logning.pdf (in Danish)

https://github.com/JSCU-NL/logging-essentials

https://github.com/SigmaHQ/sigma

https://github.com/Neo23x0/sysmon-config

https://github.com/Yamato-Security/EnableWindowsLogSettings

