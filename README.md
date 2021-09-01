# proxmox-kemp
This is a guide on installing Kemp Load Balancer on Proxmox VE.

```
wget https://kemptechnologies.com/files/packages/current/Free-VLM-VMware-OVF-64bit.zip
```

```
unzip Free-VLM-VMware-OVF-64bit.zip
```

```
unzip Free-VLM-VMware-OVF-64bit/LoadMaster-VLM-[VERSION].RELEASE-VMware-OVF-FREE.zip
```
Ex.
```
unzip Free-VLM-VMware-OVF-64bit/LoadMaster-VLM-7.2.50.0.18765.RELEASE-VMware-OVF-FREE.zip
```

```
qm importovf [ID] LoadMaster-VLM-[VERSION].RELEASE-VMware-VBox-OVF-FREE.ovf [SERVER]
```
