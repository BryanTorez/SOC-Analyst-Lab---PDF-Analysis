<h1>SOC Analyst Lab - PDF Malware Analysis</h1>


<h2>Description</h2>
USB's can often lead to a security compromise if proper security measures are not in place. Such as disabling the usage of USBs, having a proper EDR solution, or sometimes proper security awareness training. Although some companies utilize a Cloud solution as a replacement for what a USB has to offer such as transferring files in and out of the environment there are still quite a bit of organizations that do utilize USBs. One, they can be cheaper. Two, it is something you own. Three, it is portable. In this walk-through project, we'll be going over a lab provided by 'Blue Team labs' called, 'Suspicious USB Stick' where we'll be analyzing the contents that were found in a USB after a startup company has been compromised. I'll be using REMnux, a Linux malware analysis toolkit, to help with analyzing these contents, and if you aren't sure how to get started with REMnux. I'll leave a link in the description for you down below. Let's get started to get started with this lab.


<h2>Applications Used </h2>
REMnux Malware Toolkit Website (https://docs.remnux.org/install-distro/get-virtual-appliance)
Blue Teams Labs Login Website (https://blueteamlabs.online/login)

<h2>Walk-through Project:</h2>

<p align="center">
You want to head over to Blue Team Labs and create an account. Once you create an account and log in, you want to head over to challenges at the top from there you want to search up 'Suspicious' and the one that you want to click on is 'Suspicious USB Stick'. Click on 'start challenge'. : <br/>
<br />
<img src="https://snipboard.io/SKWgji.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/t6dWjO.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/296s5t.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Let's quickly go over the scenario. "One of our clients informed us that they recently suffered an employee data breach. As a startup company, they had a constrained budget allocated for security and employee training. I visited them and spoke with the relevant stakeholders I also collected some suspicious emails and a USB drive an employee found on their premises. While I am analyzing the suspicious emails, can you check the contents on the USB drive? What I'll do is right-click this download file and then click on the copy link address. :  <br/>
<br />
<img src="https://snipboard.io/R2C1fw.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
The reason why I'm doing this is that I am using REMnux for my file analysis and I am currently SSH'd into my REMnux machine. Again, if you don't know how to get started with REMnux, I'll leave a link in the description down below. : <br/>
<br />
<img src="https://snipboard.io/ZSC3XJ.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
I am going to type in 'wget' and paste my link. Once it's done downloading, I'll type in 'ls' and my file is right there. I'll type in 'unzip aqC' and hit 'tab' on your keyboard for auto-completion. From here it will ask me for a password. If we go back over to Blue Team Labs we can see that the password is 'btlo'. Type in 'btlo' back in the machine. Now we have two files that we unzipped. There is one that is called 'BTLO.txt' and then another one called 'USB.zip'. Let's type in 'ls' again one last time to see a new folder that was created called 'BTLO Suspicious USB'. :<br/>
<br />
<img src="https://snipboard.io/sJt4h2.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/MWKfXq.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/rOZBMd.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/qx5V3B.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/MJCGzd.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/3LArbT.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/MQ2CU7.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/mVQBxE.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Let's go ahead and change to that directory. Type in 'cd BTLO\ Suspicious\ USB/' and then type 'ls'. Here are the two files that we extracted I'll display the file 'BTLO.text' by typing 'cat BTLO.txt'. It says, "This FREE challenge is owned and provided by https://blueteamlabs.online. Please don't distribute these files outside of our platform - we give them away for free anyway." I'll clear out the screen by typing 'clear'. Now let's go ahead and unzip our 'USB.zip' file by typing 'unzip USB.zip'. It'll ask for another password.  <br/>
<br />
<img src="https://snipboard.io/71pXQB.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/6kECcn.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/SbQ386.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/lw5y1N.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/O69c4P.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
<br />
If we go back over to the site, it says "inner ZIP: infected". I'll type in 'infected' in all lowercase in the machine. Now we have two additional files. One is the 'autorun. inf' and then the other one is a 'README.pdf' file. Type 'clear' to clear the screen and type in 'ls' to see the directory that you need to change into. Type 'cd USB". Type 'ls' one more time. Now we have another directory called 'autorun'. Let's go ahead and change into that directory after typing in 'ls' one last time. We can see our two files but first, let's go ahead and clear out the screen here by typing 'clear'. :  <br/>
<br />
<img src="https://snipboard.io/H2UGjL.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/1bdnB4.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/otyqEY.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/XVDKQj.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/KH67B5.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/nmMPfN.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/2r4RSG.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
The first thing I'm going to do is obtain a file hash for these two particular files. To do that, I'll type in 'sha256sum *' into the machine. This will tell REMnux to generate a 'Sha256' hash on these two files. I'll open up my trusty notepad and let's go ahead and copy and paste these values in there. Now that we generated a file hash, the next thing that you can do is search on virus total to see if anybody else has analyzed these files:  <br/>
<br />
<img src="https://snipboard.io/jNlWwP.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/sEKwvQ.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/nTxMbv.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/Dbl5ar.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Before we do that, let's continue with this analysis. Whenever you download any type of file you don't always want to trust the file extension that you see. For example, we can see that this file is called 'readme.pdf'. Now you don't want to always trust that this particular file is a PDF file just because it says PDF. You might ask, "But Bryan how do we determine if that file is a PDF file or not?" This is where a magic number comes in handy, AKA a file signature. These are essentially the first couple of bytes that make up a file. In other words, these bytes are how the operating system can determine the file's file type. :  <br/>
<br />
<img src="https://snipboard.io/gZLi6m.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
I'll show you a site that I love to use. So if you go to Google and search "Gary Kesler magic number". You want to select the first result which is "GCK File Signatures Table". Click on that and from here I can do a ctrlt+f to 'find'. I'll type in 'PDF'. So this right here is our magic number or file signature for a PDF file. The first couple of bytes are '25', '50', '44', and '46'. Now if I head back over into my SSH session within Linux there is a command called 'file'. If I enter that, it will allow you to determine the type of this particular file. For example, I'll type in 'file readme.pdf' and it spits out, "Hey it's a PDF document!". But how did 'file' determine that? It is based on the magic number SL file signature which is what we see right here. :  <br/>
<br />
<img src="https://snipboard.io/5KZVDb.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/8ToFQ9.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/PIR7kW.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/bDQtGs.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/prRf8U.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/AaVT80.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
If you wanted to see the first couple of bytes for any kind of file. You can download a third-party tool called 'HxD'. Within Linux, we have a command that we can use called 'xxd'. For example, we can type and enter 'xxd README.pdf'. Look at that we have a bunch of information here. :  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
:  <br/>
<br />
<img src="https://snipboard.io/bfcRXU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/OPXwiH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
