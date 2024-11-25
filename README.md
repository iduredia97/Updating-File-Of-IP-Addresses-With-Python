# Updating-File-Of-IP-Addresses-With-Python
## Description
My organization has restricted access to specific information and resources to only allow IPs contained in an allowed IP addresses list. This list is contained in the file: ```allow_list.txt```. Another list identified as: ```remove_list``` has been created for IP addresses that are no longer allowed to have access to this content and need to be removed from the allowed IP addresses list.
## Overview
This Python script is designed to manage access to restricted information and resources by maintaining a list of allowed IP addresses ```allow_list.txt```. It removes IP addresses specified in a ```remove_list``` from the allowed list and updates the file accordingly.
## How It Works
* Reads the IP addresses from the ```allow_list.txt``` file.
* Compares them against a predefined list of IPs to remove ```remove_list```.
* Removes any matching IPs from the allowed list.
* Writes the updated IP list back to ```allow_list.txt```.
* Prints the updated contents of the file.
* The following code is my algorithm written in Python using Python 3 syntax.

The following code is my algorithm written in Python using Python 3 syntax.

```Python
# Assign 'import_file' to the name of the file 'allow_list.txt'

import_file = "allow_list.txt"

# Assign 'remove_list' to a list of IP addresses that are no longer allowed to access restricted information. 

remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

# Build 'with' statement to read in the initial contents of the file

with open(import_file, "r") as file:

  # Use '.read()' to read the imported file and store it in a variable named 'ip_addresses'

  ip_addresses = file.read()

# Use '.split()' to convert 'ip_addresses' from a string to a list

ip_addresses = ip_addresses.split()

# Build iterative statement
# Name loop variable 'element'
# Loop through 'ip_addresses'

for element in ip_addresses:
  
  # Build conditional statement
  # If current element is in 'remove_list',
  
    if element in remove_list:

        # then current element should be removed from 'ip_addresses'

        ip_addresses.remove(element)

# Convert 'ip_addresses' back to a string so that it can be written into the text file 

ip_addresses = " ".join(ip_addresses)    

# Build 'with' statement to rewrite the original file

with open(import_file, "w") as file:

  # Rewrite the file, replacing its contents with 'ip_addresses'

  file.write(ip_addresses)

# Build 'with' statement to read in the updated file

with open(import_file, "r") as file:

    # Read in the updated file and store the contents in 'text'

    text = file.read()

# Display the contents of 'text'

print(text)
```
