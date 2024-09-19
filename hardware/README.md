# FLEXI Hardware Construction

Hello there! Now, this may be fairly non-standard, but I'm here to explain to you how to build your own **FLEXI (any pronouns)**! The [original paper](https://osf.io/dbg6h/) on FLEXI is wonderful, but flawed. And in attempting to construct a FLEXI for the Robot Studio, this became clear to me. My name's Melodie Jaeger (she/they) and I will be guiding you through everything that was overlooked in the hustle and bustle that can come with trying to meet paper submission deadlines. 

In this document, I will be going over a few key topics that are necessary in order for you to construct your very own FLEXI. The instance of FLEXI that I built ended up being named **Violet (she/her)** and I will be using that designation to delineate between her and FLEXI as a wider designation for the project. The original paper neglected a few details here and there, and while I had access to Dr. Alves-Oliveira and her files on the project, not everybody does, so an addendum became necessary. As well, this addendum will serve as a gallery of photos of **Violet**, for reference on what FLEXI \textit{should} look like, approximately. Outside of this introduction, I'll try to avoid unnecessary fluff as much as possible. Without further adieu, let's get into it!

## BoM Addendum 

First up, the BOM! I've included a list of everything that was excluded from the original BoM that is necessary for basic functioning of FLEXI, in the file `bom_addendum.csv`.

Not included in this mini-BoM is zipties, which I think are pretty common
for labs to have, and aren’t *necessary*, but will help you with cable management. A solder station and a bit of heat-shrink wouldn't hurt, either.

Oh, and make sure the USB-A to USB-C cable is right angle or 180 degree on the USB-C end. This is necessary for proper fitting of the faceplate over the Pixel.

## Aluminum Parts Fabrication

Next, since most of the structural parts of FLEXI are made of cut aluminum, I'm including some guidance on that. I can't tell you how to work whatever equipment is available to you, but I can advise on buying the material and laying it all out. 

A note for buying the stock, I was able to make an 8" by 8" sheet of .190" thick aluminum work for the largest part, `circular_base.dxf`. If you're not deeply confident in your ability to set up your cutting equipment with precision, you probably want to get a larger sheet, as this part has a diameter of 200 mm, allowing for only 3 mm of tolerance (8" = 203 mm). For purchasing the materials, I've included a little table of what to get, in the file `alu_stock.csv`.

The [OSF](https://osf.io/dbg6h/) repo contains the .dxf files for cutting all the parts for FLEXI, and then you can use a nesting software, such as [Deepnest](https://deepnest.io/) to arrange the parts on your stock sheets. 

## Faceplate 

The faceplate is a rather simple piece, made of a 3D printed part, `faceplate.stl`, and 2 M2.5 threaded heat-set inserts. I chose to paint the one on **Violet** a lovely lilac shade. This, in general, is one of the easiest parts to base little customizations and fun details around.(TODO: add heat insert image)

## Construction

Another goal of this document is to supplement the original instructions for building FLEXI. In building **Violet**, I had a lot of trouble with these instructions, especially since it looks like they tried to fit the entire process on one page, with varying results. There are also simply a few typos and mistakes that I'd like to save you some time with. Concerning the directions on page 1185 of the original paper:

- There is no direction on what fasteners to use for what. Use your best guess/intuition for this, and for most parts of the construction, it'll be fine. The kits in the BoM have plenty nuts and bolts.
- Step 1 is very unclear about standoffs and spacers. I used M3 x 8 standoffs to attach the makerbeams to the part labelled "square base". I used a stack of washers for the parts labelled simply "spacers". Alternatively, for this step, you can use M3 screws and spacers, but the holes are sized for M4. It's probably fine either way.
- In Step 2, the motor labelled "Dynamixel motor" is the XH540-W270-T motor called for in the BoM.
- In Step 3, I would advise not attaching the phone plate just yet. What you should do is attach the phone case to the phone plate, using the faceplate as a jig to make sure everything fits together properly. (TODO: include pics of this process)
- Also, in Step 3, the motor labelled as "Motor B" is the 2XC430-W250-T, and each of the two axes connected by the neck parts requires an idler. Look in the manuals for the idlers in the BoM to see which motors they correspond to. 
- Oh, and in Step 3, the part labelled "150MM Makerbeam" is, in fact, supposed to be a 100mm Makerbeam. Save yourself the headache of disassembly and reassembly.
- Step 4 is a bit tricky, so I've included an image that should help guide you through it: 
 
![control board assembly](images/board_assem.PNG)

The remainder of the original instructions for building FLEXI are pretty simple and easy to follow, aside from the wiring. 


## Wiring

The wiring documentation in the original paper is... lacking. I'm not convinced that this isn't a strange choice, but you may have noticed that it calls for a car charger for the Surface Pro, and then that is wired into a barrel plug in parallel with the U2D2. If there is future work on the desin of FLEXI, this is the most obvious place to start. I feel like a well-designed and very minimal PCB could handle some of this shall we say... jank.

 **Note**, by the way, that the U2D2 is wired differently for FLEXI than what the U2D2 [e-manual](https://emanual.robotis.com/docs/en/parts/interface/u2d2/) says. Otherwise, I found that the manuals from Robotis for the motors and U2D2 were very helpful.

The wiring on FLEXI truly isn't all that complex. In putting the thing together myself, I elected to forego the crimp connectors in the BoM for some good ol' fashioned splicing with heat-shrink and solder. (TODO: include image of this) If you don't know how to splice wires, you can find a ton of great online guides. Follow the wiring diagram included with the original paper, and use the barrel connector included in `bom_addendum.csv`. 

In addition, there is a lot of wiring involved in making all of the connectivity that FLEXI needs to function. Some of the cables needed for this can be found in `bom_addendum.csv`, but basically, you just need to be able to pass a lot of data between the Surface, the Pixel, and the U2D2. Here's a wiring diagram that I found useful:

![FLEXI wiring diagram](images/FLEXI%20wiring.png)

