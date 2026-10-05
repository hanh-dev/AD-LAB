## This is my practice place as an SysAdmin
-----------------1-------------------------
1. ## Description:

Last week an ad popped up offering to speed up my laptop, so I ran PC Speed Booster Pro and let it 'optimize' everything. It does feel a bit quicker, but now I can't print at all — Word says the printer isn't available and the printers in Settings all show as offline. I need to print contracts this afternoon.

2. ## Resolution

2.1. Start Print Spooler service
- Spooler is the service that queues and routes print jobs, so while it is stopped nothing prints and queue can't even opened, let alone cleared. Every printer reading Offline at Once - software printers included - is the signature of the service being down rather than of any device being unplugged.

2.2. Set the spooler service's type to Automatic

2.3. Close and update ticket for client
-----------------2-------------------------
1. ## Description:

Since the firewall change last night nobody in the office can get to any website. Email still comes in and out and the internal systems are fine. Whoever did the work has gone on leave.

2. ## Resolution:

We need to clarify that the issue is internal user can't access any website out of it VLAN. This issue might be related to Router which will forward traffic in different network (private -> public).

In the access rules of Router, there is disabled rule (VLAN -> WAN). This is reason why users inside company could not browse any websites. I enable it and it is working fine now.


---------3-------------------------------------
1. ## Description:

Hi, this is Aisha. My coworker was trying to sort out my search not finding things and typed something in one of those black command windows. A gray error box came up and he had to go, so I've left it on the screen exactly as it was. I don't know if that means it worked or if something's still broken — can you look?

![alt text](image.png)

2. ## Resolution 

Upon my checking, the Error means "An instance already running so we couldn't start service twice." There is no any wrong with that. I have check the service status by command line, and it returns me running status of that one. Everything works perfectly.
