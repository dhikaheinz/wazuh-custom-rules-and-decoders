# Wazuh Custom Decoders and Rules

This project contains custom decoders and rules for Wazuh, created by me. Some rules are based on SOC Fortress rules, and some are my own decoders and rules.

### How to use

- Put rules and decoder files under `/var/ossec/etc/rules` and `/var/ossec/etc/decoders`.
- Put under `/var/ossec/integrations` for integrations script
- Put under `/var/ossec/active-response/bin/` on agent side for active response script.

### Install wazuh-agent with interactive script

You can install the Wazuh Agent by running the following command:

For Linux agent

```sh
curl -sSL https://raw.githubusercontent.com/dhikaheinz/wazuh-custom-rules-and-decoders/main/install-agent.sh -o install-agent.sh && bash install-agent.sh
```

For Windows agent

```sh
Invoke-WebRequest https://raw.githubusercontent.com/dhikaheinz/wazuh-custom-rules-and-decoders/main/install-agent.ps1 -OutFile install-agent.ps1; powershell -ExecutionPolicy Bypass -File .\\install-agent.ps1
```

The script will ask about:

- Wazuh Agent version
- Wazuh Manager IP address
- Wazuh Agent group (empty for 'default')
- Authentication key (optional)
- Install quarantine-malware.sh (optional)

**Note:**  
For security, always review scripts before running them directly from the internet.

### Disclaimer

Feel free to use it, you can redistribute it and/or modify it under the terms of GPLv2.
Cybersecurity is hard, so let's work together.

### Updates

I will update rules and decoders if the projects I work on require them.
