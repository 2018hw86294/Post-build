# Post-build
This playbook is created to apply the post build configuration on "Windows" host machines.

as Hole Descriptions:

**computername: It updates the computer name in host machines. This need to be given in the host inventory.

server_config: This is the basic configuration role. it includes below tasks:

Rename the Administrator user to AdminBol.

Set the time zone given in ansible variables. Default is "Eastern standard time". (Select the specific timezone with ansible tower survey option.

Rename the ethernet to server's IP address.

- Disable IPV6 and UAC.

-Add the default service account and defined users in "user admin" variable. It need to be added with survey option.

*disk_initialize*: It initialize and format the raw disk added in the host machine.

domainjoin: It added the server in the defined domain etc. This requires additional access to add the server in the domain. ADMIN USERNAME and ADMIN PASSWORD need to passed as extra variables to add the server in domain.

securitystandards: It disable the firewall for domain, public and private profiles. grouppolicy: This task updates the policies with gpudpate command.

services: It verifies the different agent service are running in the server.

configure the same on host machines. It also ensures basic agent checks given in the SOP.

report: This generates an HTML report and send it to central location. This captures all the information which is updated in the host machine.
