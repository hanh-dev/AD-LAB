## This is my practice place as an SysAdmin

1. ## Description:

Last week an ad popped up offering to speed up my laptop, so I ran PC Speed Booster Pro and let it 'optimize' everything. It does feel a bit quicker, but now I can't print at all — Word says the printer isn't available and the printers in Settings all show as offline. I need to print contracts this afternoon.

2. ## Resolution

2.1. Start Print Spooler service
- Spooler is the service that queues and routes print jobs, so while it is stopped nothing prints and queue can't even opened, let alone cleared. Every printer reading Offline at Once - software printers included - is the signature of the service being down rather than of any device being unplugged.

2.2. Set the spooler service's type to Automatic

2.3. Close and update ticket for client