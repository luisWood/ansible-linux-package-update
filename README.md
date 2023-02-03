# APT package update playbook

##### ***DISCLAIMER*** <br>
###### *Target machines are rebooted as a final step of the playbook*

<br>

--- 

### **Requirements** 
##### - Ansible

<br>

---

### **Configuration**
##### Edit ***hosts*** file under ***[general]*** with ip address and username like so: <br> <br> 

##### [general] <br>
##### {IP_ADDRESS_1} ansible-user="{MY_USERNAME_1}" <br>
##### {IP_ADDRESS_2} ansible-user="{MY_USERNAME_2}" <br>
##### {IP_ADDRESS_3} ansible-user="{MY_USERNAME_3}" <br>

<br>

---

## **Running** 
To run the playbook simply run the following command:

> ansible-playbook -i ./hosts update-apt-packages.yml -kK

##### **[-k]** - shorthand for [--ask-pass], will prompt for the password used to connect to targets 
##### **[-K]** - shorthand for [--ask-become-pass], will prompt for the sudo password
##### **[-i]** - To specify path to inventory file

<br> 

#### Targets will be updated, printing the last line of the update command. **The target is then rebooted**.

