# homelab
## Virtualization
I am using an customized version of VMware vSphere Hypervisor 6.5 for the following hardware:

- Intel i5 6500
- MSI H110M PRO-VD
- 16 GB DDR4 
- 128 GB SSD (ESXi)
- 2x 1 TB HDD (datastore)

## Building
To build the custom image you have to install [PowerCLI](https://my.vmware.com/de/web/vmware/details?downloadGroup=PCLI650R1&productId=614) from VMware and [ESXi-Customizer-PS](https://www.v-front.de/p/esxi-customizer-ps.html)

```powershell
.\ESXi-Customizer-PS-v2.6.0.ps1 -v65 -vft -load sata-xahci,net-e1000e,fw-ntpd,vmware-esx-dvfilter-maclearn
```
Parameter:
> -v65 means we will use Version 6.5
> -vft will use the online depot from vfront
> -load will download and add the following ESXi packages