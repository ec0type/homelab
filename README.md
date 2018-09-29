# homelab
## Virtualization
I am using an customized version of VMware vSphere Hypervisor 6.7 for the following hardware:

- Intel i5 6500
- MSI H110M PRO-VD
- 16 GB DDR4 
- 128 GB SSD (ESXi)
- 2x 1 TB HDD (datastore)

## Building
To build the custom image you have to install [PowerCLI](https://my.vmware.com/de/web/vmware/details?downloadGroup=PCLI650R1&productId=614) from VMware and [ESXi-Customizer-PS](https://www.v-front.de/p/esxi-customizer-ps.html)

```powershell
.\ESXi-Customizer-PS-v2.6.0.ps1 -v60 -vft -load sata-xahci,net-e1000e,fw-ntpd,vmware-esx-dvfilter-maclearn