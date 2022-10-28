# Security Onion Import Node Cheat Sheet

## Operating System (CentOS7):
 - **username:** analyst
 - **password:** password2022
 
## SOC(Web) Interface:
 - **URL:** https://IP_of_server
 - **username:** analyst@securityonion.com
 - **password:** password2022
 
## IP Address Change Instructions:
 - Once the VM is imported, change network adapter(1) to NAT and power-on the VM.
 - Log into the security onion server and run the following command:
   ```sudo so-ip-update```
 - Reboot the machine.

## Import Datasets:
 -  To import PCAP files run the following command:
 ```sudo so-import-pcap <pcap1.pcap pcap2.pcap>```
 
 - To import windows event logs, run the following command:
 ```sudo so-import-evtx <file1.evtx file2.evtx>```

 - Import nodes will only allow you to import the same dataset once. If you would like to reimport the data, you will need to delete the content of the /nsm/import/ directory using the following command:
```sudo rm -rf /nsm/import/*```

 - To delete all Data in Elasticsearch (ie. Alerts, Hunt, and Cases data) run the following command:
```sudo so-elastic-clear -y```
