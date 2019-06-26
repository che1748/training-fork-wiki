High performance computing is overwhelmingly done on a Unix (or Linux) operating system. You will need to become familiar with Unix and the terminal. In addition, you will need to be able to connect to the FSL supercomputing clusters from a local machine of your choice.  
\
If you are unfamiliar with Unix/Linux, read through the [FSL’s Unix tutorial](https://marylou.byu.edu/documentation/unix-tutorial/). (Another good resource is [this tutorial](https://www.msi.umn.edu/sites/default/files/Intro_to_Linux_Fall2015_0.pdf) from the Minnesota Supercomputing Institute.) You should also spend some time practicing what you are reading about. A good way to practice is to use [this online Unix terminal](https://www.tutorialspoint.com/unix_terminal_online.php). It is a bit slow, but it is a useful place to start. Once you have practiced a bit you might find [this cheat sheet](https://files.fosswire.com/2007/08/fwunixref.pdf) helpful.  
\
Once you are familiar with Unix commands, you will need to decide what computer you will use for doing research. You will use this computer to communicate with the super-computer, for coding and to do other research tasks. You have three different options for a local computer to do your work: (1) a personal laptop, (2) [a CAEDM lab computer](https://caedm.et.byu.edu/wiki/index.php/CAEDM_Labs#Lab_Locations), or (3) a computer in my student offices. (Note: I do have a computer set up for this, but there is not guarantee that it will always be available to use.)  
\
The operating system that is installed on the local machine has an impact on the software you can use to do your work. Because the super-computers run Linux, it is often convenient to use a local machine that is also running Linux. However, this is not necessary, and may not be desirable if you do not feel comfortable with it. This is a choice you will have to make for yourself; I have no preference what you use, I simply want you to be productive :).  
\
There are CAEDM computers available with Linux, and the machine in my lab is a Linux box. If you have a personal laptop, you may decide to experiment with installing Linux alongside Windows or in a virtual machine. (Note: there are many “flavors” of Linux that you can install. [Ubuntu](https://www.ubuntu.com/desktophttps://www.ubuntu.com/desktop) is a particularly user-friendly version that you may want to look up, if you decide to go this route.) Again, this is up to you.  
\
Once you have decided what machine and operating system to use, attempt to log in to the FSL head node at ssh.fsl.byu.edu. Procedures for different operating systems are outlined below. Some additional information can be found on the FSL website.  

### Linux/Mac
If the operating system on your local machine is some flavor of Linux then connecting to or transferring data with the FSL clusters is straightforward via the terminal with SSH, SCP and RSYNC. ([Here is a tutorial for SCP and RSYNC](https://linuxtechlab.com/files-transfer-scp-rsync-commands/)). Mac machines are Unix machines under the hood, and they also have a terminal. As such they can also access the FSL via SSH, SCP or RSYNC. More details about these commands can be found by a Google search.  
### Windows  
Windows has recently begun a project to incorporate a native Linux shell as a subsystem on Windows. Details regarding installation and use can be found at [this website](https://msdn.microsoft.com/en-us/commandline/wsl/about). This is one of the harder methods to set up initially, but once you do it tends to be the most straight forward and least buggy way of using Linux on Windows. Essentially it is like running a Linux operating system inside of Windows and it can do most of what a Linux shell can do.  
\
If you don't want to use the Windows subsystem for Linux (WSL), connecting via ssh can be done with a program called Putty. You will need to follow the instructions at the [Putty](http://www.putty.org/) website to install it on windows and to connect to the FSL.  
Unfortunately, Putty cannot do file transfers. A common FTP client for transferring files is [FileZilla](https://filezilla-project.org/). Again, you will need to follow the instructions at the website to install FileZilla and to learn to use it to transfer files.  
\
You have one other potential option for both ssh and FTP commands. [Bitvise](https://www.bitvise.com/index) is a putty-like program that combines SSH and FTP commands into a single software package. I have never used it, but details on installation and use can be found on its website.  
### SSH Keys
It can be annoying to repetitively enter your password when copying files to and from a cluster. It is possible to set up a secure key between your machine and a remote server so that you don’t have to enter your password every time you log in or copy files or use git. [This tutorial](https://confluence.atlassian.com/bitbucketserver/creating-ssh-keys-776639788.html) shows you how to create an SSH key, and [this one](https://www.cyberciti.biz/faq/how-to-set-up-ssh-keys-on-linux-unix/) shows you how to set up password-less log-ins. (Note: Due to security requirements, the FSL no longer allows passwordless logins to their server. Every time you log into the FSL you will need to provide your password and a verification code from your phone).  
\
Before moving on from this task, you should:
* Have chosen a local machine and operating system,
* Be able to log on to/log off from the FSL,
* Be able to create, move, and delete files and directories on the cluster,
* Be able to copy files and directories to/from your local machine to the cluster
* Set up SSH keys as desired
