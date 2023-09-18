<h1>Firewall Application</h1>

<h2>Description</h2>
The Firewall Application monitors incoming and outgoing network traffic based on predefined rules and policies.
<br />

<h2>Languages and Utilities Used</h2>

- Java
  
<h2>Environment Used </h2>

- Visual Studio Code 

<h2>Program walk-through:</h2>

<p align="center">
Class Rule: <br/>
<img src="https://imgur.com/PbCSgG4.png" height="80%" width="80%" alt=""/>
  <br/>
  This class represents a rule for the firewall. Each rule has:
  <br/>
  sourceIP: The source IP address.
  <br/>
  destinationIP: The destination IP address.
  <br/>
  sourcePort: The source port number.
  <br/>
  destinationPort: The destination port number.
  <br/>
  The action to perform on traffic that matches this rule, which can be "ALLOW" or "DENY".
  It has a constructor to initialize these fields and a matches method to check if a given set of IP addresses and port numbers match the rule.
<br />
<br />

<p align="center">
Firewall Class:  <br/>
<img src="https://imgur.com/rzZKjG6.png" height="80%" width="80%" alt=""/>
  <br/>
This class represents the firewall itself. It contains a list of Rule objects to manage the rules.
 <br/>
The constructor initialises an empty list of rules.
 <br/>
The addRule method allows you to add new rules to the firewall by specifying source and destination IP addresses, source and destination port numbers, and the action to take (ALLOW or DENY). It creates a new Rule object and adds it to the list of rules.
 <br/>
The filter method takes in source and destination IP addresses, source and destination port numbers, and it iterates through the list of rules. It checks each rule using the matches method to see if it matches the given traffic. If a matching rule is found, it returns the action associated with that rule (ALLOW or DENY). If no matching rule is found, it defaults to "DENY."
<br />
<br />

<p align="center">
Main Method Class: <br/>
<img src="https://imgur.com/DhoQHfM.png" height="80%" width="80%" alt=""/>
  <br/>
In the main method, a Firewall object is created.
 <br/>
Two rules are added to the firewall using the addRule method to allow or deny traffic between specific IP addresses and port numbers.
 <br/>
Then, it simulates incoming and outgoing traffic by specifying source and destination IP addresses and port numbers.
 <br/>
Finally, it calls the filter method to determine the action to be taken for the simulated traffic and prints the result.
<br />
<br />

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
