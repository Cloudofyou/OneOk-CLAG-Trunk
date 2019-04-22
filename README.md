## OneOk-CLAG-Trunk 

### Summary:

Get VRR/CLAG to trunk to downstream ESXi hosts with 2 VLANs
 
### Network Diagram:

![Network Diagram](https://github.com/Cloudofyou/OneOk-CLAG-Trunk/blob/master/documentation/OneOk-CLAG-Trunk.png)

### Setup

```
git clone https://github.com/cloudofyou/OneOk-CLAG-Trunk
cd OneOk-CLAG-Trunk
./bringitup
cd vx_simulation
vagrant ssh oob-mgmt-server
ssh server01
wget -O /home/cumulus/.ssh/authorized_keys "http://192.168.200.254/authorized_keys"
exit
ssh server02
wget -O /home/cumulus/.ssh/authorized_keys "http://192.168.200.254/authorized_keys"
exit
git clone https://github.com/cloudofyou/OneOk-CLAG-Trunk
cd OneOk-CLAG-Trunk/automation
./provision
```
