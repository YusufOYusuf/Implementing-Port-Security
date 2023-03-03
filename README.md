<h1>Implementing Port Security</h1>


<h2>Description</h2>
In this lab, I learned to implement port security. Port security controls how many MAC addresses can be learned on a single switch port. This feature is implemented on a port-by-port basis.
<br />



<h2>Environments Used </h2>

- <b>Ubuntu 20.04.2 LTS</b> 

<h2>Utilities and Language </h2>

- <b>PuTTY SSH Client</b>

<h2>Program walk-through:</h2>

<p align="center">
From the left sidebar navigate to PuTTY and enter in your Host Name, port, and connection tyoe and click open<br/>
<img src="https://i.postimg.cc/D0kJZhBw/Screen-Shot-2023-03-02-at-11-26-55-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
  
<br />
type in the following commands to enter configuration mode  <br>
en <br>
conf t <br>
<img src="https://i.postimg.cc/vTVKrrrv/Screen-Shot-2023-03-02-at-11-31-18-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />



<br />
Now enter the following commands to in configuration mode to implement port security for the e0/1 interface <br>
interface e0/1 <br>
switchport mode access <br>
switchport port-security <br>
switchport port-security maximum 5 <br>
switchport port-security violation protect <br>
switchport port-security mac-address sticky <br>
end <br>
<img src="https://i.postimg.cc/JzY4dmwd/Screen-Shot-2023-03-02-at-11-36-24-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />



<br />
Now type in the following commands to enable mode to observe port security configuration<br>
show port-security <br>
show port-security interface e0/1 <br>
<img src="https://i.postimg.cc/GppzdF5m/Screen-Shot-2023-03-02-at-11-39-48-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />

  
  
  
