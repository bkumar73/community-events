# Ansiblefest 2020 - Centralized RBAC for Networks with Ansible Tower

This repository contains example playbooks, inventory and variable files to support automation across network devices from multiple vendors including:

* Cisco
    * NXOS
    * IOS
* Arista
* VyOS
* Cumulus

The advantage of using Ansible to automate networking devices is that it provides a centralized toolset that can interact with different vendor devices simultaneously. Tower further extends the value of using Ansible for Network Automation by providing a built-in, encrypted credential store, SCM integration and full RBAC capabilities. 

As part of the Ansiblefest 2020 breakout session, 3 use cases were highlighted:

1. Ansible Tower RBAC: Levels of Access
2. Network Configuration as Code with Git Workflows
3. Centralized Network Device Secrets

# Ansible Tower Configuration as Code

In an effort to emphasize Configuration as Code (CaC) wherever possible, Ansible Tower may also be configured from a set of defined variables and source from a Git repository. The Ansible connection below was used to configure Tower in support of the demos:

[https://github.com/redhat-cop/tower_configuration](https://github.com/redhat-cop/tower_configuration)

# GNS3 Network Simulator 

The GNS3 Network Simulator is used to emulate the devices: 

[GNS3](https://www.gns3.com/software/download)

[GNS3 Topology](network_automation/assets/gns3-topology.png)

# Playbooks

| Playbook Name  | Description  |
|---|---|
| device_gather_facts.yaml  | Gather facts from multiple network devices  |
| network_report.yaml  | Gather facts from multiple network devices and produce a templated Jinja 2 report |
| cisco_nxos_declarative.yaml  | Configure Cisco NXOS Multi-Layer Switch from defined variable values  |
| ping.yaml  | Perform a network PING using vendor modules to verify Ansible can connect to network devices with valid credentials |

## Tower Surveys

Here are a few screenshots to capture the survey settings used in the demo's. Taking this a step further, the variable used to populate the `hosts` for the playbook runs can match a specific parameter in the firing webhook or be based on reference branches in the Source Code Management tool.

[Multi-Vendor Device Inventory Host Variable](network_automation/assets/tower-survey.png)

# Connect

Reach out on [Twitter](https://twitter.com/arctiqhart), [GitHub](https://github.com/arctiqhart) or the [Arctiq Website](https://www.arctiq.ca)!