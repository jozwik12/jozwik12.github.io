---
title: 'Why on earth are we still using STL files?'
pubDate: '05.20.2024'
---

3D printing has an incredible community. Whenever you want to create something new, whether to print immediately or to browse for inspiration, you just need to visit popular design-sharing websites like Thingiverse or Printables.

I've explored these sites numerous times, and while I'm always amazed by the seemingly endless stream of ideas from the community, it bothers me that many designs only provide STLs, neglecting to include STEP files.

When comparing STEP files to STLs, there are several notable advantages:
- **they contain unit information**  
STL files are just a mesh of points, floating freely in space without any unit constraints. For instance, when you import a 3D Benchy, is it 30mm or 30m long? While context usually helps deduce the correct scale, it's not foolproof. In the metric system, this often means scaling down by a factor of 10 in Fusion 360 to get realistic dimensions. But what if the file was created in the imperial system? Leaving this to interpretation introduces potential errors.
- **their precision doesn't depend on mesh setting of the author**  
STLs are discrete models. Consider a hole or a peg—essentially, a circle.
![Example](/stl-vs-step-1.jpg)
STEP files can model such geometry accurately because they are designed for it. However, STLs approximate circles with line segments, turning them into hexagons. Default export settings are usually sufficient for most 3D printing applications, not sacrificing quality in a meaningful amount.
![Example](/stl-vs-step-2.jpg)
If the author deviates from these settings and uses, precision can suffer and there's not much you can do about it. Your best hope is reverse engineering the whole model. But the lower quality mesh, the harder it is to interpolate dimensions.
![Example](/stl-vs-step-3.jpg)
- **they are easily modified**  
Authors of the project often modify it to account for their printers' characteristics. That's especially visible when printing holes. For example, let's say that you want to create a hole for M5 bolt. You don't want to make the hole too small - the bolt won't fit or it will fit but will be very hard to turn (or will just thread into the material of the hole itself, not the nut). You don't want to make it too big as well - it will jitter. Theoretically, 5mm hole would be perfect (bolts are a bit undersized to have air gap that allow threading into the nut), but reality is often different. You need to offset the diameter by .1, .2, .3mm. How much? It depends on quite a few variables (slicer resolution, flow ratio, filament type and so on). The thing is, they're unique to your setup and almost never transferable to other users. 5.1mm hole on your printer may turn out to be 5.2mm wide, but on other printer it may be 4.9mm. If you're printing someone's STL file you are dead set on their dimensions. Modifications are possible - you can either use special program for STLs modification or reverse-engineer the whole model. Problem is first solution can be a pain to work with and second one is time consuming. And with STEP files that's straightforward - just import it and offset the dimension by however much you desire.
- **they can be universally transfered between any CAD software of your choice**  
While Fusion360 seems to be the most popular CAD software in 3D printing niche, alternatives, like
FreeCAD or OnShape are getting more popular each day. Add on more industry-focused programs
like SolidWorks, NX, or Catia and you get an explosive mix. Each of these programs has a preferred format that is tailored to the specific program/environment. Good luck trying to import .3mf file (Fusion format) to SolidWorks or NX. But STEP files act as a universal bridge, making it easy to transfer designs between different software environments.

STEP files are not without their flaws, as detailed in this [criticism](https://en.wikipedia.org/wiki/ISO_10303-21#Criticism), but they excel as a universal link between modern CAD software. They function like an adjustable wrench—versatile and universally applicable, though not always as precise as a dedicated tool.

Some argue that designers hesitate to share program-specific files for fear of judgment. Sharing such files reveals the entire design process, potentially opening up one's work to criticism. I disagree with this viewpoint for two reasons. First, everyone makes questionable design decisions - there are no perfect designs, only functional ones. Second, STEP files do not save design history, so no one can see the decisions you're reluctant to share.

Historically, you could argue that this debate is pointless, because in context of 3D printing those files were used in 2 use cases that were not overlapping. STEP files were used to exchange info between CAD programs (or users), but if you wanted to print your creation, you just *HAD* to make an STL file - it was the only type of file accepted by slicers. The thing is, that's not the case anymore - majority of the most popular slicers are able to import STEP files. And they are able to capitalize on the precision it brings.

In conclusion, there are increasingly fewer reasons to use STLs. Observing design-sharing websites like Printables or Thingiverse, more users are providing STEP files alongside STLs. This trend is a positive development, and I hope it continues.