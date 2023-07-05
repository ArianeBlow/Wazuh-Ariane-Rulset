# Wazuh SoC Bad Actor Detection
## Windows Defender action sending to Wazuh:


### Install Wazuh agent : 
```cmd
.\wazuh.exe "Wazuh server IP"
```


### Edit wazuh conf on the host :
(Edit : C:\Program Files (x86)\ossec-agent\ossec.conf)
```xml
  <localfile>
    <location>Microsoft-Windows-Windows Defender/Operational</location>
    <log_format>eventchannel</log_format>
  </localfile>
```

### Restart Wazuh Agent on host : 
```cmd
net stop WazuhSvc
net start WazuhSvc
```
