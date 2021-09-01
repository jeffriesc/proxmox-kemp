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

In my case it was **VERSION** `7.2.50.0.187`
```
unzip Free-VLM-VMware-OVF-64bit/LoadMaster-VLM-7.2.50.0.18765.RELEASE-VMware-OVF-FREE.zip
```

Now you we want to add the .ovf file into your list of VM's using the following line of code. `qm importovf [ID] LoadMaster-VLM-[VERSION].RELEASE-VMware-VBox-OVF-FREE.ovf [SERVER]`

I set my **ID** to `107` and chose `local` as the **SERVER**
```
qm importovf 107 LoadMaster-VLM-7.2.50.0.18765.RELEASE-VMware-VBox-OVF-FREE.ovf local
```







