<h1>Update a File With a Python Algorithm</h1>


<h2>Description</h2>
In this project, I used Python to create an algorithm that modifies a file containing a list of allowed IP addresses. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 
- <b>Jupyter Notebook</b>

<h2>Project walk-through:</h2>

<p align="center">
Define a Python function called update_file which takes two parameters: import_file (the name of the file to be updated) and remove_list (a list of IP addresses to be removed from the file): <br/>
<img src="https://i.imgur.com/h4m3MW4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
The with open(import_file, "r") as file: statement is used to open the file specified by import_file for reading:  <br/>
<img src="https://i.imgur.com/RmD2VW8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
file.read() reads the contents of the file and stores it in the variable ip_addresses: <br/>
<img src="https://i.imgur.com/K7QdQmt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Use split() to convert the immutable string data to a list, so it can be modified:  <br/>
<img src="https://i.imgur.com/kkArz5T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a 'for loop' to iterate over each element in the ip_addresses list:  <br/>
<img src="https://i.imgur.com/oKPVO0Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
A conditional statement checks if the element is present in the remove_list. If it is, it means the IP address should be removed:  <br/>
<img src="https://i.imgur.com/rLpzMEq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Inside the loop, if an IP address is found in remove_list, it is removed from the ip_addresses list using ip_addresses.remove(element):  <br/>
<img src="https://i.imgur.com/u6B9xtu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
After removing the specified IP addresses, the code joins the modified ip_addresses list back into a string (with IP addresses separated by spaces) using " ".join(ip_addresses):  <br/>
<img src="https://i.imgur.com/3ceb418.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
A new with open(import_file, "w") as file: statement is used to open the same file, but this time for writing.
file.write(ip_addresses) writes the updated content back to the file:  <br/>
<img src="https://i.imgur.com/kQDGvAE.png" height="80%" width="80%" alt="8"/>
<br />
<br />
A new with open("allow_list.txt", "r") as file: statement is used to print the modified list of ip addressed from the file:  <br/>
<img src="https://i.imgur.com/70liqqs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
