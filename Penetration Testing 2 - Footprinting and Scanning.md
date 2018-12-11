2 - Footprintig and Scanning

2.1 - Only run on a network with permission

2.2 - Mapping a Network
	Local and Remote Networks
	E.g. Asks for a penetration test on 200.200.0.0/16 scope
		Ping sweeping
			Echo - Reply ICMP packets
			Linux: fping -a -g range (fping -a -g 200.200.0.0/16 2> /dev/null)
				-a = Alive
				-g = sweep instead of standard ping
			NMAP
			nmap -sn 200.200.0.0/16
			nmap -sn -iL hostslist.txt
				-sn = for a ping sweep.
				-iL = for input list from file. 
				-sL = List scan
				-Pn = Treat all as alive (Skip discovery)
				-PS/PA/PU/PY[postlist]: TCP SYN/ACK, UDP ot SCTP discovery on given ports
				-PE/PP/PM: ICMP Echo, timestamp, and netmask discovery probes
				-PO[Protocol list]: IP Procotol Ping
				
	Should have a list of live hosts that are respondong to ping
	2.2.3 OS Fingerprinting
		Send network requests and analyze the response, possible because of small differances in the network stack implementations in different OS. 
		Send a series of specific requests and analyse every bit of the responses creating a signature. 
		
		
		
	
				
			