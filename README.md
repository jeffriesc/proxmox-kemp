# proxmox-kemp
This is a guide on installing Kemp Load Balancer on Proxmox VE.

1. Open your instance of Proxmox and login
2. Click on the node you wish to add the Kemp Load Balancer VM to
3. Navigate to the Shell
4. Begin by entering `wget https://kemptechnologies.com/files/packages/current/Free-VLM-VMware-OVF-64bit.zip` and press enter
5. Then unzip the downloaded: `unzip Free-VLM-VMware-OVF-64bit.zip`
    1. There will be a few different files unzipped 
6. Now unzip the `LoadMaster-VLM-[VERSION].RELEASE-VMware-OVF-FREE.zip` file.
    1. In my case it was **VERSION** `7.2.50.0.187` resulting in the the following code `unzip Free-VLM-VMware-OVF-64bit/LoadMaster-VLM-7.2.50.0.18765.RELEASE-VMware-OVF-FREE.zip`
7. Now you we want to add the .ovf file into your list of VM's using the following line of code. `qm importovf [ID] LoadMaster-VLM-[VERSION].RELEASE-VMware-VBox-OVF-FREE.ovf [SERVER]`
    1. I set my **ID** to `107` and chose `local` as the **SERVER** for the following code `qm importovf 107 LoadMaster-VLM-7.2.50.0.18765.RELEASE-VMware-VBox-OVF-FREE.ovf local`

Before launching the VM go into the Hardware tab and change the SCSI Controller to **VMware PVSCSI**

*You may also want to double check that Start at Boot is enabled under the VM Options. 

That's it! You've successfully imported the Kemp Load Balancer into Proxmox and you can now start it and begin configuring it. NetworkChuck has a great walkthrough on this over on Youtube. Check it out [Here](https://youtu.be/LlbTSfc4biw).




