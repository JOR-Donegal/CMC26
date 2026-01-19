# SMART
You should carry these exercises out on a real physical machine if possible, VMs do not show SMART counters.

You may not install software in the computer labs. 

Find a free SMART tool monitor online. I use _Crystal Disk Info_ but use the one from your own hard disk manufacturer.

<figure>
<img src = "https://jor-donegal.github.io/CMC26/images/fig8.png">
<figcaption>Fig 8. Crystal Disk Info.</figcaption>
</figure>

I have installed a basic disk utility, almost every hard disk manufacturer has their own. Ideally, you should use the tool for the disk in your own system; e.g. a tool from Seagate, Hitachi, Western Digital, etc. 

Locate the tool, install it and test your system. My system is showing six hard drives, a mixture of HDDs and SSDs. If you have an SSD, most of the counters will give you meaningless data. 

But what are these values, what do they mean, are they significant? 

Firstly, do some background reading and understand what SMART is and why it may be important. Then find a list of the attributes reported and what they mean. See if you can locate any good reference which tell you what attributes to monitor and whether you can do predictive failure analysis on that basis. 

This module does NOT assume a knowledge of Linux; however, I am going to ask you to look up a basic tool used in Linux systems for SMART. Find __smartmontools__, understand what they are. 

In data centre environments, I would use these in Linux for predictive failure analysis. Knowing which attributes to consider and what the numbers mean, that’s the challenge!