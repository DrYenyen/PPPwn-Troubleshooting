# PPPwn-Troubleshooting     
Beginning to end PPPwn troubleshooting. 
      
# PPPwn Windows GUI 
[PPPwn Tinker](https://github.com/DrYenyen/PPPwn-Tinker-GUI)    
      

# Windows Desktop side troubleshooting.     
1. Troubleshooting on windows is not straightforward but you can try the following things.
2. Confirm your ethernet adapter is NOT bridged with anything. 
3. Try changing the Npcap version to an older one.         
4. Confirm your ethernet adapter is functional by going into device manager and looking at "netword adapters" if there are any issues try reinstalling your adapter driver. 
5. If using Python preferably go to C++ otherwise make sure Python , Pip and Scapy are installed.   
6. Try a different windows device as sometimes no matter what you do issues cannot be resolved without reinstalling windows.      
       
# PS4 side troubeshooting.         
1. Failed to get IP when pressing on "Test Internet Connection" Usually a PC side issue look above for troubleshooting or check your PS4 internet settings by looking below.      
           
# Setting up the PS4 internet connection  
On your PS4  
1. Go to **Settings** and then **Network**   
2. Select **Set Up Internet connection** and choose Use a **LAN Cable**  
3. Choose **Custom** setup and choose **PPPoE** for IP Address Settings  
4. Put in anything as **Username** and ***Password*** it is recommended for it to be 1 letter that's the same in both fields for better compatibility.
5. Choose **Automatic** for *DNS Settings* and *MTU Settings*
6. Choose **Do not use** for *Proxy Server*   
7. Go back and be ready to press on *Test internet connection*      
     
# Putting the goldhen or VTX payload on a usb          
Format a usb drive to exFAT               
Copy the goldhen.bin file onto your usb drive  for Goldhen          
Copy the payload.bin file onto your usb drive  For VTX           
Then plug the usb into your PS4              
       

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
3. If on a Mac try a windows device......    or if already on windows try changing the Npcap version to an older one if on Windows.       
       

# Stage 3:             
0. Any issues here usually result in a kernel panic=console shutting down.        
[+] STAGE 3: Remote code execution    
[*] Sending LCP terminate request...    
[*] Waiting for PADI...    
[+] pppoe_softc: 0xffffabd634beba00    
[+] Target MAC: xx:xx:xx:xx:xx:xx      
[+] Source MAC: 97:df:ea:86:ff:ff    
[+] AC cookie length: 0x511    
[*] Sending PADO...    
[*] Waiting for PADR...     
[*] Sending PADS...     
[*] Triggering code execution...     
[*] Waiting for stage1 to resume...      
[*] Sending PADT...     
[*] Waiting for PADI...        
[+] pppoe_softc: 0xffffabd634be9200      
[+] Target MAC: xx:xx:xx:xx:xx:xx     
[+] AC cookie length: 0x0      
[*] Sending PADO...     
[*] Waiting for PADR...      
[*] Sending PADS...     
[*] Waiting for LCP configure request..     
[*] Sending LCP configure ACK...     
[*] Sending LCP configure request...     
[*] Waiting for LCP configure ACK...     
[*] Waiting for IPCP configure request...     
[*] Sending IPCP configure NAK...         
[*] Waiting for IPCP configure request...          
[*] Sending IPCP configure ACK...     
[*] Sending IPCP configure request...      
[*] Waiting for IPCP configure ACK...            
1. Console shutdown happens ocasionally on its own but if it persists try changin to a different IPV6 for the exploit settings usually marked by "old", "Stable", "new" or "beta".      
2. If issues persist recheck all your files and etc.         

# Stage 4:   
1. If you get     
[+] STAGE 4: Arbitrary payload execution    
[*] Sending stage2 payload...     
[+] Done!      
2. But only get the "PPPwned" message then there is an issue with the payload on the USB or HDD.      
3. Reformat the USB to EXFAT and put "goldhen.bin" or "payload.bin" Goldhen or VTX Hen respectively.        
4. If no matter what you do the bin file does not load either factory reset the console or replace the HDD.    
      
# Misc issues Stage0: to Stage4:    
1. You may get some random errors here and there they are usually because of incorrect interface, incorrect files (resluts in kernel panic), incorrect firmware sellection or ocasionally incomplete dependencies.     

