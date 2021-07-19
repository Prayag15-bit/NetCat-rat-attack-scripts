# NetCat RAT Scripts

A *Remote Access Trojan* (RAT) is a malware program that includes a back door for administrative control over the target computer. RATs are usually downloaded invisibly with a user-requested program -- such as a game -- or sent as an email attachment. Once the host system is compromised, the intruder may use it to distribute RATs to other vulnerable computers and do other crazy stuffs

So, in this repository, I created a very simple script using a traditional tool available and used worldwide *i.e.* "Nmap-NetCat"

# What is NetCat

*NetCat* (often abbreviated to nc) is a computer networking utility for reading from and writing to network connections using TCP or UDP. The command is designed to be a dependable back-end that can be used directly or easily driven by other programs and scripts. At the same time, it is a feature-rich network debugging and investigation tool, since it can produce almost any kind of connection its user could need and has a number of built-in capabilities.

Using this NetCat, I basically tried to establish what-so-called as a *"Reverse Shell"*

# A Brief Overview about Reverse Shell

1. Usually, whenever we talk about how hackers intrude someone's system, the most common answer is :- "*They use various tools and methods to gain access to a target's system and after gaining access, they hack any bit of information essential*"
2. So, in order to avoid such things from happening, the companies created some application, which today is known as a "FIREWALL". In computing, a firewall is a network security system that monitors and controls incoming and outgoing network traffic based on predetermined security rules. These security systems monitor the network traffic and as a result, it can greatly help in stopping such attacks
3. Now a days, even people are becomiong more and more aware about Trojans, Malwares etc. They can tell whether a file or any kind of program is harmful for their systems or not. Or maybe, a hacker is trying to hack into their systems or not. Keeping that in mind, the concept of *Reverse Shells* can be used.
4. The principle of Reverse Shell says that :- "*In order to gain access to someone's machine, the hacker will not try to access the system. Instead, the user itself will provide the access without being known of anything"*
5. The Reverse Shell can be used to gain access to a user's machine in just miliseconds and the user will not even be aware of what is going on.

# How to perform the attack 
1. This script is only available for RedHat based linux systems for now. So that means, both the attacker and target machine must be a RedHat based Linux System (Either it may be a "VIRTUAL MACHINE" or a "FULL-FLEDGED-MACHINE"
2. Clone the repository in the attacker's RHEL machine

*git clone https://github.com/Prayag15-bit/NetCat-rat-attack-scripts.git*

3. After the cloning is done, go inside the directory

*cd NetCat-rat-attack-scripts*

4. Inside you can find two folders :- One will be with the name "ATTACKER's SERVER" and the other will be "TARGET's SERVER"

# For Attacker's Machine
1. Go inside the "Attacker's Server" directory and run the provided script

*bash Attacker-script.sh*

This will basically create a listener on top of the Attacker's Machine and will continuously try to listen to the port specified in the script (The port number I provided in this case is 5000).

2. Now, go back and this time, go into the "Target's Server" directory and open the script using your editor of choice (Either gedit or nano or vi/vim)
3. Replace the "<Attacker's_Server_IP_address>" part with the actual Attacker's Machine IP address.
4. Save the file and exit
5. Now, everything is set at Attacker's Side and now it is time to move to Target's Side

# For Target's Machine
1. First things first, this reverse shell attack can be done even on remote machines. So, it is essential that the Taerget's Machine (Whether local or remote) should run the script that the Attacker has configured in his/her Machine. The method of making the target to run the script will completely depend on Attacker
2. Before the Target runs his script, make sure the Attacker's Machine Listener is already set and running
3. As soon as the Target Machine runs the script, the attacker will receive a message on his/her terminal that the connection from *<Target_system_IP>* is received

# AND THERE YOU GO!!!! THE REVERSE SHELL IS ESTABLISHED AND THE ATTACKER NOW WILL HAVE COMPLETE ACCESS TO A TARGET's COMMAND LINE INTERFACE
