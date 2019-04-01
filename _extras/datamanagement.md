---
layout: page
title: Data Management Tips
---
[The following is distilled from a _Nature_ Toolbox article that was published on 1 April 2019: Perkel, J.M. 11 ways to avert a data-storage disaster. _Nature_ **568**, 131-132 (2019). [https://www.nature.com/articles/d41586-019-01040-w](https://www.nature.com/articles/d41586-019-01040-w)]

**Tips for managing your data**

1. **3-2-1**: Fires, floods, and theft all happen -- not to mention bitrot (the deterioration of storage media over time). So, keep at least three copies of your data, on two different media, at least one of which is off-site. (And be sure to store your local copies under proper environmental conditions!)

2. **Talk to the experts**: Make your institution’s professionals your first call. Ask IT team colleagues about free or low-cost backup options available; your librarian about data management strategies; and your grant officers about regulations regarding how, and how long, to store data

3. **Safeguard privacy**: Private data, such as student information, cannot be stored just anywhere. And if those data are lost or stolen, you could face consequences. If you have, or plan to store such data, speak to your institution’s IT team for advice.

4. **Manage your data**: Make your backups more effective, and more future-proof, by developing a data-management plan. Establish file-naming conventions and organizational strategies -- for instance, that each project gets its own directory, with dedicated subdirectories for data and code. Decide which data will be backed up, and which can be discarded. Determine where different data types will be backed up, and how often. And, document everything: Keep a copy of your data management plan where people can find it, and annotate your experiments with README files that indicate the experiment, the file structures, required applications or scripts, and so on. 

5. **Share with others**: Your colleagues may also need access to your data. Can someone else understand what the data are and where they’re located if you’re not around? Make sure they have access and permissions to the data and that they are able to understand what the files are and how they are organized (see **Manage your data**).

6. **Be realistic**: Once you develop a backup strategy, discuss it in the lab. Is it accessible to new colleagues, or only command-line experts? Is it doable after pulling an all-nighter? And how effective is it? Simulate what would happen if disaster should strike: What data will you lose, and what can you recover?

7. **Automate**: The thing about backups is, you need them when you least expect it. So don’t rely on remembering to run a backup -- automate them.

8. **Test your backup**: Do your backups actually work? Test them to find out. Make sure you can actually open key files, and that you have the required applications to read them. Use checksums to ensure data integrity. And test the files on a different system if possible, as, if your primary computer should fail, you won’t have access to its contents.

9. **Protect your raw data**: Always backup your raw data. And keep it safe: Duplicate the data before working with it, and open it read-only. An errant file-open command in write mode (e.g., in Python: `f = open (filename, ‘w’)`) instead of read (`‘r’`) is all it takes to wipe out a file for good.

10. **Keep one backup offline**: An always-on backup system is a recipe for disaster. If your computer is hacked, or suffers a power-spike, the backup system can also be compromised. So keep at least one backup offline, just in case.

11. **Plan ahead**: Storage media don’t last forever, so periodically review your backup strategy to make sure it’s current. Do you still have devices that can read the backups? Is it time to migrate to a newer platform? And don’t neglect your cloud storage: companies can shift priorities, or you can lose your passwords. So double-up on those too, just in case.

12. **Expect the unexpected**: Make periodic disaster assessments to safeguard your hardware. If you live in a flood zone, the basement may not be the best place to store a server. If you live in an earthquake-prone area, you might anchor your computers so they don’t fall over. And if your computers are located near fire-control sprinklers, you might raise them off the ground, or shield them from potential leaks.
