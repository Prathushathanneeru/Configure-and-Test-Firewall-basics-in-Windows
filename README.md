# Configure-and-Test-Firewall-basics-in-Windows
Configure and test  the basic firewall rules to allow or block the traffic in windows 
# 1.Open Configuration Tool in Windows
* In keyboard press "Win+R" then a small window opens.
* Type "wf.msc and Press Enter.
* This opens a **Windows Defender Firewall with Advanced Security**.
# 2.List Current Firewall Rules
* In left panel, click **"Inbound Rules"** or **"Outbound Rules"**.
* You will see a list of existing rules with names, programs, ports, and actions (Allow/Deny).
# 3.Add a Rule to Block Inbound Traffic on Port 23(Telnet)
* In the left pane, click "Inbound Rules" > in right pane, click "New Rule...".
* Select Port, click Next.
* Choose TCP, and enter 23 in Specific local ports.
* Click Next, select Block the connection, click Next.
* Choose when it applies (Domain, Private, Public), click Next.
* Name the rule something like Block Telnet, click Finish.
# 4.Test the Rule
* On the same system  or different system open command prompt and type the command:
* telnet <target-ip> 23
* Connection should be refused or timeout if the rule works.
* As per windows the SSH(port 22) is applicable to add
# 5.Remove the Test Block Rule
* In the **Windows Defender Firewall with Advanced Security**:
* Go to **Inbound Rules**,find your block(Block Telnet),right-click on it and click on **Delete**.
