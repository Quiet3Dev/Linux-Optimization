# Linux-Optimization

NOTE: These tweaks are optional and do not need to be used to improve the DNS resolver. If you are going to use these tweaks, they tend to break some distros. I recommend trying to use the bare minimal distro in order to prevent any issues that may appear in the future using these tweaks. Use these tweaks at your own risk. I am not responsible for any hardware damages.


The Linux optimization folder is focused on trying to find ways to extract the maximum amount of performance from hardware by tweaking network settings. Performance tweaks are focused on laptop tweaks and high-end server tweaks; however, high-end servers can be tweaked for normal desktops; you just need to do trial and error. Sysctl network tweaks focused on the networking to extract the most data from the bandwidth at the same time do cause issues with device drop connections. These network tweaks will need to be modified for the user since each device will likely drop or stay connected to the point that holds all bandwidth. Grub tweaks are supposed to try to extend some features and remove features that could slow down tasks.

   Grub Tweaks Folder   
 ------------------------

Grub tweaks probably wouldn't need to be tweaked for users since a lot of the features don't improve performance. It's used to remove features that could slow down hardware parts or slow down network features that could be beneficial for Pi-Hole and Unbound. The maximum performance for Grub tweaks should be very low since just disabling and enabling features for the desktop or server pushes queries through DNS.

Recommendation User to Tweak: Optional


   Linux Performance Tweaks Folder   
 -------------------------------------

Linux performance tweaks have two sections: laptops and desktops or servers. Since both can be used, it is supposed to make laptops able to be used for Pi-Hole and Unbound. The laptop section will only have small tweaks since thermals on laptops tend to be limited and prevent laptops from going to sleep when the user closes the lid. Desktops and servers try to reach the maximum values of what Linux can handle before starting to break. These tweaks are recommended that users modify them towards specific devices since thermals, HDDs or SDDs, RAM, and CPU can be problems.

Recommendation User to Tweak: Yes

   Linux Sysctl Network Tweaks Folder   
 ----------------------------------------

Sysctl network tweaks have x86-64 processors, which focus more on throughput since Linux is already low-latency. This will force the network adapter to be able to get more data and, at the same time, force the CPU to be able to access more, allowing it to respond with a DNS request. Since it will depend on the network adapter and cables able to handle large amounts of network packets, the server can answer requests fast enough for time-sensitive applications.

For example, if you have CAT-6 cable to a Gigabit Ethernet port, it will be slower compared to CAT-8 cable to a Gigabit Ethernet port because of the transfer speed of CAT-8 cable; however, the problem is that it will be hard to detect the difference. The only recent difference found is with Pi-Hole updating the adlist faster and regex blocking faster by going through webpages.

Recommendation User to Tweak: Yes

   Linux Modify Network Adapter Folder   
 -----------------------------------------

Network adapter tweaks focus on increasing the maximum transmission unit (MTU) by using jumbo frames since it can increase from 1,500 default frames to 9,000 frames. However, supporting network adapters depends on the manufacturer since most servers use them for special reasons to be active. For transmit queue length (tx_queue_len), network adapters are allowed to go through the kernel, allowing them to answer packets through both Pi-Hole and Unbound. The downside of transmit queue length is that if the server is already loaded and the number of packets has been reached, it could cause delays or webpages could load improperly.

Recommendation User to Tweak: Yes

   Linux Miscellaneous Folder   
 --------------------------------

Miscellaneous folder is only used for finding out CPU speed, temperature, and disabling swap disks if the user wants extra information about hardware running. Disabling swap disks will only help if the system has more than 16 GB of RAM on the server or desktop.

Recommendation User to Tweak: Optional
