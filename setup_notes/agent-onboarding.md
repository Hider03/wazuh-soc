After installing Wazuh, through its all in one installation on a separate VM, I decided to add the other VM's that I have running on my proxmox set up.

The other two being a media VM, and an Infrastructure/Cloudflared VM.

Both VMs here are running Debian amd64. 

``` bash
wget https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_4.14.5-1_amd64.deb && sudo WAZUH_MANAGER='MY WAZUH IP' WAZUH_AGENT_GROUP='default' WAZUH_AGENT_NAME='new' dpkg -i ./wazuh-agent_4.14.5-1_amd64.deb
```

``` bash
sudo systemctl daemon-reload sudo systemctl enable wazuh-agent sudo systemctl start wazuh-agent
```