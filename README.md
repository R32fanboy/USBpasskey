# USBpasskey
simple way to keep your information with you at all times


I'm sure there are already many different more professional ways to accomplish this, but I figured I would share this method nonetheless. 

A. Hardware/Software
    I'm using a generic 1Gb USB rubber bracelet someone happened to have lying around that sparked this idea. Use whatever you'd like, as long as it's a USB drive that won't drive you crazy having to find it and plug it in every time you want to access your browser session. I'm using Firefox on Ubuntu, the process will be slightly different on windows.  
B. Method.
    Data safety. I assume if you're walking around with a USB drive full of your browser session cookies and passwords that you want it protected lest you misplace it. Veracrypt comes in handy for this. Install veracrypt on the computer you're planning on using this with the most and from there get ready to partition your USB drive. I used GParted. You'll need two different partitions, one for your encrypted data, and one for the portable applications you're going to need to take this thing cross-platform. Make sure that when you partition the drive, you make the partitions slightly uneven so that you can tell them apart when you have to blindly choose a partition that isn't showing a label. 
    Now that you have two separate partitions, start up veracrypt and encrypt the *Second* partition, leaving the first unencrypted. Create a folder in your home directory where you will mount the encrypted volume, and then mount the volume there using Veracrypt. Once that's done, open your web browser (I use FireFox, not sure how it's handled in other browsers) and navigate to "about:profiles" and create a custom profile, choosing the directory you just mounted. Make this profile the default profile and close the web browser, then start it back up, navigating back to the profiles page and delete the rest of the profiles. You won't be neededing them anymore. Go ahead and browse around and log into a few things, letting firefox save the passwords when you do. 
    When you're done browsing, bring up VeraCrypt again and dismount the encrypted volume. If you bring up firefox now, all of your logged-in sessions are now gone. They'll be right back where you left them after mounting the volume again. 
    For added fun, I threw the windows portable VeraCrypt executable on the non-encrypted partition, along with a few other portable applications that would be useful to take with me on the road.  
