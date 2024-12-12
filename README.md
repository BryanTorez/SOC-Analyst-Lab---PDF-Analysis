<h1>SOC Analyst Lab - PDF Malware Analysis</h1>


<h2>Description</h2>
USB's can often lead to a security compromise if proper security measures are not in place. Such as disabling the usage of USBs, having a proper EDR solution, or sometimes proper security awareness training. Although some companies utilize a Cloud solution as a replacement for what a USB has to offer such as transferring files in and out of the environment there are still quite a bit of organizations that do utilize USBs. One, they can be cheaper. Two, it is something you own. Three, it is portable. In this walk-through project, we'll be going over a lab provided by 'Blue Team labs' called, 'Suspicious USB Stick' where we'll be analyzing the contents that were found in a USB after a startup company has been compromised. I'll be using REMnux, a Linux malware analysis toolkit, to help with analyzing these contents, and if you aren't sure how to get started with REMnux. I'll leave a link in the description for you down below. Let's get started to get started with this lab.


<h2>Applications Used </h2>
REMnux Malware Toolkit Website (https://docs.remnux.org/install-distro/get-virtual-appliance)
<br />
<br />
Blue Teams Labs Website (https://blueteamlabs.online/login)
<br />
<br />
Virustotal Website (https://www.virustotal.com/gui/home/upload)

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
<img src="https://snipboard.io/hT5nIN.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
If you wanted to see the first couple of bytes for any kind of file. You can download a third-party tool called 'HxD'. Within Linux, we have a command that we can use called 'xxd'. For example, we can type and enter 'xxd README.pdf'. Look at that we have a bunch of information here. :  <br/>
<br />
<img src="https://snipboard.io/S17CP0.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/t38lcX.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
So these are the hexadecimal that we want to take a look at. If you recall the magic number is the first couple of bytes. So I'll type in "xxd README.pdf | head". Using the head, it will output the first 10 lines. Just like the first couple of bytes '25 50 44 46'. Looking at it in ASCII text, we see 'PDF -1.7'. :  <br/>
<br />
<img src="https://snipboard.io/6Ihc3j.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/HkcN9D.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/tIVl6o.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/D10AWy.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Now if we go back over to our Gary Kesler site. We can see that the first couple of bytes for a PDF document are '25 50 44 46'. In our case, it does match '25 50 44 46'. Now we can say for certain that this particular file is indeed a PDF file:  <br/>
<br />
<img src="https://snipboard.io/8qNlTS.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/NzZhoe.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/sXNOHl.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
I'll go ahead and clear out the screen. Type in 'ls' again. We do have another file called 'file autorun.inf'. What I can do is type in 'file autorun. inf'. It is a Microsoft Windows autorun file. Let's go ahead and check out what the contents are for that particular file here. So I'll run 'cat autorun.inf'. We do see 'open=readme.pdf' and 'icon=autorun.ico'.:  <br/>
<br />
<img src="https://snipboard.io/hK2CVU.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/kQP6WO.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/mUIxwZ.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/oSyP5K.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
By looking at this, we can assume that once this USB was inserted it would automatically run and open this particular document called 'README.pdf'. So how do we begin analyzing PDF documents? Well, when it comes to PDFs these file types contain what are called Elements, which can then be drilled down via objects. We can do this using various different tools however the one that we'll be using today is called 'peepdf'. It does come built-in with REMnux. So if you are following along, I do highly recommend that you spin up REMnex to perform your analysis. To use this tool all we need to do is just point it over to our 'peepdf README.pdf'. :  <br/>
<br />
<img src="https://snipboard.io/1X0KqT.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/rVdk1w.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
By using PDF, we can already see some elements that are listed here. It is quite hard to see because it is highlighted in blue but we can see that there is a number correlated with this particular element. The number represents the object, whereas the name represents the elements. So for example, our catalog element is within object number one, and a catalog in terms of PDFs. You can kind of think of this as a table of contents.:  <br/>
<br />
<img src="https://snipboard.io/r04LNd.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/QoigM3.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
At the bottom, we can see objects with JS code and this is within object number 27. We can see 'Suspicious elements', 'OpenAction, 'Names', 'AA', 'JS', 'Launch', and 'JavaScript'. I'll provide a link down below for you to learn more about what these are but essentially some of the more important ones are 'OpenAction', 'AA', 'JavaScript', and 'JS'. For 'OpenAction' and 'AA', this will automatically load whatever content or code that is listed within that object once the PDF had been double-clicked. As for 'JS' and 'JavaScript', this contains JavaScript code that can be used for nefarious purposes. So let's go drill into object number one which contains our 'Catalog' and 'OpenAction'. :  <br/>
<br />
<img src="https://snipboard.io/PfQkvo.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
To drill into an object, what we need to do here is type in 'peepdf -i README.pdf'. This will allow me to use PDF in an interactive mode. This means I can start interacting with the content itself. So I'll type in 'object 1' and this will drill into my object number one. From here, we can see 'Metadata', 'ViewerPreferences', 'MarkInfo', 'StructTreeRoot', 'OpenAction', 'Pages', 'Type', 'Lang', and 'Names'. We can see that 'OpenAction' points to object 27. :  <br/>
<br />
<img src="https://snipboard.io/PJhSeL.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/3hQuv9.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/rFDp5x.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/Lyr19J.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
So what this tells me is that when this PDF opens up. Whatever is in object 27 will be executed automatically. Let's drill into object 27 to take a look at its contents. Starting with the first one we do see '/Type /Action /S /JavaScript /JS'. So let's quickly go over what this particular object is doing. For the first line, the type and action, this is indicating that the object is an action. For the second one, this specifies that the action is a JavaScript action. Finally, the last one will export a data object called 'README'. Since it is 'nlaunch: 0' it is not going to open automatically upon exporting. Now if we scroll up just a little bit here we do see a suspicious element called 'Launch' and this is located under object 28. Let's drill into our object number 28 and see what kind of contents it has, but before I do that let's go ahead and copy this for object 27 and then paste it into our trusty notepad. :  <br/>
<br />
<img src="https://snipboard.io/p4Gzyn.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/DOACJM.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/XxeU4C.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/ZhyDVa.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/s6OJ0S.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/GgMCZ2.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
I'll type 'object 27' and 'object 28' in the notepad. Then in I'll type in 'object 28' back in the terminal. Now we have some commands going on now. Before we analyze this, let's go ahead and copy this out and I'll paste it into our notepad. Let's take a look at this command. So we can see 'cmd.exe /D:\windows\system32' and a bunch of various different arguments. What this command is essentially doing is that it will open up a command prompt where the directory is within windows 'system32'. This entire command is simply looking for the file name of 'README.pdf' under the directories of desktop or documents and if it does exist then it will automatically change into that directory and execute the 'README.pdf' file. Which would then display the bottom contents which is, "To view the encrypted content please tick the "Do not show this message again" box and press Open.":  <br/>
<br />
<img src="https://snipboard.io/LhRlDH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/aOYuev.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/JWPANl.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/oZNfj8.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/7pMc6Z.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Now if we scroll back up. We do have another suspicious element that is called 'AA'. Which will automatically launch when this PDF is opened and this is within 'object 3'. So let's drill into object three and take a look. Here we can see a lot of other elements. If we take a look at 'AA' again, we can see that it is pointing over to 28 and if you recall if we go back over to 'object 28' it executes this command right here using the command prompt. Now we know what happens immediately once the USB is plugged in. To recap, once the USB is plugged in it will automatically run this 'readme.pdf' file, which then executes this command prompt with this command. :  <br/>
<br />
<img src="https://snipboard.io/s17dvM.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/j42fVn.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/9hzUQ0.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/w0LoFk.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/iEkgKy.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/j42fVn.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/j42fVn.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
If we were to search up the file hash for this readme.pdf document. I'll go ahead and open up virus total.com. Let's search and paste in the file hash in the search bar. We can now see there is '43' security vendors flagging this as malicious. It is part of a Trojan dropper hack tool with a family label as 'swrort', 'meterpreter' and 'PID'. Now head over to community and scroll down until you see "Verdict: MALICIOUS and 'Confidence: 100/100'. We can see that there is a bunch of varara signature matches detect suspicious JavaScript in PDF and that's about it so that's pretty cool:  <br/>
<br />
<img src="https://snipboard.io/mO3FGC.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/dsVhQ5.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/uqnBV7.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/qC3Uhc.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/y7G6wB.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/pB4dIz.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Let's head over to Blue Team, level one, and start answering some of these questions. 
<br />
<br />
For question one, 'what file is the autorun.inf running? Well if we head over to our SSH and type 'cat autorun.inf'. This is running 'README.pdf'. So go ahead and copy and paste that in here then click 'Submit'.
<br />
<br />
Second question, 'does the pdf pass virustotal scan? (no malicious results returned) True or False? This is false because we did see a lot of security vendors flagging this 43 to be exact.
<br />
<br />
Third question, 'does the file have the correct magic number? Yes, it does because if you recall if we type in 'xxd README.pdf | head". We can see that the first couple bites are '25', '50', '44', and '46'. Which again if we head over to Gary Kesler for a proper PDF file document, the first couple bytes must start with '25', '50', '44', and '46'. :  <br/>
<br />
<br />
<img src="https://snipboard.io/vcgNTF.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/XqvjSh.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/fz0SDZ.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/N4Cput.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/1GbDWh.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/jaGx9h.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/89GCgB.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/2N8SWo.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/eYX87o.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/iVpF4I.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/AkVfG8.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
The fourth question, 'What OS type can the file exploit?' (Linux, Mac OS, Windows, etc.). This is going to be Windows. How do I know that? Well if we go back over to our notepad, the command 'command.exe' is pointing to the directory of 'C windows system32'. So that is why I am saying Windows.
<br />
<br />
The fifth question, 'A Windows executable is mentioned in the PDF file, what is it? It is 'cmd.exe'. 
<br />
<br />
Finally the last question, 'How many suspicious /OpenAction elements does the file have? Let's type in 'peepdf -i README.pdf'. With this, we're looking for 'OpenAction'. As we can see there is only one 'OpenAction'.: <br/>
<br />
<img src="https://snipboard.io/bhVHop.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/NvjYHc.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/XzEriV.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/jdBl1s.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/LZReus.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://snipboard.io/X5hN4q.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Now I know this was quite a high-level overview of how to analyze PDFs. By following along, I hope you are gaining more confidence in your ability to analyze PDFs. <br/>
<br />
<br />
<br />
<br />
<br />
