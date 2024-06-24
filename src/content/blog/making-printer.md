---
title: 'Making printer Mk1'
pubDate: '01.10.2022'
updatedDate: '04.25.2024'
---

I was familiar with many types of 3D printing, mostly due to college courses that covered various technologies and industrial applications. However, the idea of owning and using one never particularly appealed to me.

That changed one fateful weekend during my fourth year of college. I woke up one Saturday with a sudden inspiration: I not only wanted to own a 3D printer but also to learn everything there was to know about them.

I dove headfirst into this new interest, spending the entire weekend (yes, the entire weekend) watching videos and reading articles. In the process, I had a revelation. I decided I wouldn't buy a 3D printer — I was going to *make* one.

Using the information I gathered, I set the following design guidelines:

1. **The technology was going to be FDM/FFF printer**  
Mostly due to popularity of that technology. I didn't want any "exotic" materials, so no need for SLS. And building SLA seemed like too much hastle (they're not that DIY-friendly) and wanted to avoid mess in my leased appartament
2. **It's going to be as cheap as possible**  
I was a college student - that point is self-explainatory
3. **Kinematics - Cartesian**  
I decided on Cartesian kinematics for 2 reasons. It's the simplest one. And I didn't know that CoreXY exists.
4. **The form factor was going to be similar to common hobby 3D printers**  
While I hadn't decided on specific dimensions or axis arrangements, I knew I wanted Cartesian kinematics. I looked to existing hobby printers like the Prusa i3 or Creality Ender for guidance, figuring their form factors were chosen for good reasons. Even if I didn't understand those reasons, I expected to encounter similar challenges and make similar decisions
5. **Self-contained**  
3D printer parts can be divided into standard, off-the-shelf hardware (nuts, bolts, aluminum extrusions, etc.) and non-standard parts, like fixtures. The former can be purchased, but the latter are unique to each printer model and usually 3D printed or machined on CNC machines. For an added challenge, I decided not to use another 3D printer to make my 3D printer. That’s what I meant by self-contained.

So, with that in mind, I came up with a first design in Fusion360. It may sound anticlimactic, but it actually took me tens of hours making and unmaking hundreds of decisions to get this:

![First design](/making-printer-1.jpg)

The design satisfied most of my guidelines, but the fifth guideline—self-containment—proved particularly challenging and exciting. Online shops had almost all the standard hardware I needed. If something wasn’t available locally in Poland, I turned to Aliexpress, accepting a longer wait time.

The non-standard fixtures were a different story. Theoretically, I could use the 3D printer owned by the student club I was a part of (CNC Scientific Student Club), but I found a different, cheaper, and jankier solution.

I would use *plywood*:

![Plywood parts](/making-printer-2.jpg)

Plywood had two important advantages. First, I could easily work with it using the hand and power tools I had on hand. Second, it was didn't cost me a penny — I found it in my parents' basement. Though not very precise, it didn't need to be - it was a temporary solution. Once the printer was up and running, its first task would be to print proper fixtures for itself. The printer would, quite literally, print itself!
But before it would work I needed to get to work. I decided to make a prototype:

![Printer semi-assembled](/making-printer-3.jpg)

Once I had confidence that my setup would work (or at least it has a chance to do so) I added frame and couple of other important bits to my assembly and made this:

![Printer assembled](/making-printer-4.jpg)

And yes, the PSU is definitely lying on top of laundry basket. Might have been a fire hazard, but I was too excited to care about that.
And I was excited, because it worked!

<video width="720" height="540" controls>
  <source src="../../../making-printer-5.mp4" type="video/mp4">
</video>

Of course, the first prints were not perfect. But they never are.

![First print](/making-printer-6.jpg)

I didn't know it at the time, but it was just the beginning of a long journey...

