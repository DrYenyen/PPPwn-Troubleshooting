# PPPwn-Troubleshooting
Beginning to end PPPwn troubleshooting.

# Windows Desktop side troubleshooting.


# Stage 0:         
1. Stuck on "[*] Waiting for PADI..." Make sure you are calling the correct ethernet interface.       
2. Stuck on "[*] Waiting for PADI..." Make sure the PS4 and PC(or other device) are connected via ethernet.          
3. Stuck on "[*] Waiting for PADI..." Make sure the PS4 internet settings are correctly set up and go to Settings>Network and press on "Test Internet Connection"     
4. Stuck on "[*] Waiting for PADR..." If using a usb to ethernet adapter it may not be compatible or simply try restarting the exploit proccess.   
5. Stuck on any of the below simply try restarting the exploit proccess.        
[+] pppoe_softc: 0xffffabd634beba00     
[+] Target MAC: xx:xx:xx:xx:xx:xx     
[+] Source MAC: 07:ba:be:34:d6:ab     
[+] AC cookie length: 0x4e0    
[*] Sending PADO...   
[*] Sending PADS...    
[*] Waiting for LCP configure request...    
[*] Sending LCP configure ACK...    
[*] Sending LCP configure request...    
[*] Waiting for LCP configure ACK...    
[*] Waiting for IPCP configure request...      
[*] Sending IPCP configure NAK...    
[*] Waiting for IPCP configure request...     
[*] Sending IPCP configure ACK...      
[*] Sending IPCP configure request...    
[*] Waiting for IPCP configure ACK...      
[*] Waiting for interface to be ready...     
[+] Target IPv6: fe80::2d9:d1ff:febc:83e4    
[+] Heap grooming... done or xx%       
simply try restarting the exploit proccess. 

     
4. For more look at *Windows Desktop side troubleshooting*            
       
	   
# Stage 1:
1. Any issues here usually result in a kernel panic=console shutting down.       
2. Console shutdown at "[*] Waiting for IPCP configure ACK..." happens ocasionally on its own but if it persists try changin to a different IPV6 for the exploit settings usually marked by "old" or "Stable".     
3. Console persistently shutting down at "[*] Waiting for IPCP configure ACK..." or "[+] Scanning for corrupted object..." try changing the Npcap version to an older one if on Windows.      
4. If on a Mac try a windows device......    
      

# Stage 2:     
0. If persistently stuck on the below  
[+] STAGE 2: KASLR defeat      
[*] Defeating KASLR...     
[+] pppoe_softc_list: 0xffffffff884de578    
[+] kaslr_offset: 0x3ffc000      
      
1. Any issues here usually result in a kernel panic=console shutting down.       
2. Console shutdown happens ocasionally on its own but if it persists try changin to a different IPV6 for the exploit settings usually marked by "old" or "Stable".     
3. If on a Mac try a windows device......       
       

# Stage 3              

