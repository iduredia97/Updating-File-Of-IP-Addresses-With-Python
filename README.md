# Updating-File-Of-IP-Addresses-With-Python
## Description
My organization has restricted access to specific information and resources to only allow IPs contained in an allowed IP addresses list. This list is contained in the file: allow_list.txt. Another list identified as: remove_list has been created for IP addresses that are no longer allowed to have access to this content and need to be removed from the allowed IP addresses list.
## Overview
This Python script is designed to manage access to restricted information and resources by maintaining a list of allowed IP addresses (allow_list.txt). It removes IP addresses specified in a remove_list from the allowed list and updates the file accordingly.
## How It Works
* Reads the IP addresses from the allow_list.txt file.
* Compares them against a predefined list of IPs to remove (remove_list).
* Removes any matching IPs from the allowed list.
* Writes the updated IP list back to allow_list.txt.
* Prints the updated contents of the file.
* The following code is my algorithm written in Python using Python 3 syntax.

The following code is my algorithm written in Python using Python 3 syntax.

