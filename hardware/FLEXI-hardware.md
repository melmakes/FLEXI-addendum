# FLEXI Hardware Construction

Hello there! Now, this may be fairly non-standard, but I'm here to explain to you how to build your own **FLEXI (any pronouns)**! The [original paper](https://osf.io/dbg6h/) on FLEXI is wonderful, but flawed. And in attempting to construct a FLEXI for the Robot Studio, this became clear to me. My name's Melodie Jaeger (she/they) and I will be guiding you through everything that was overlooked in the hustle and bustle that can come with trying to meet paper submission deadlines. 

In this document, I will be going over a few key topics that are necessary in order for you to construct your very own FLEXI. The instance of FLEXI that I built ended up being named **Violet (she/her)** and I will be using that designation to delineate between her and FLEXI as a wider designation for the project. The original paper neglected a few details here and there, and while I had access to Dr. Alves-Oliveira and her files on the project, not everybody does, so an addendum became necessary. As well, this addendum will serve as a gallery of photos of **Violet**, for reference on what FLEXI \textit{should} look like, approximately. Outside of this introduction, I'll try to avoid unnecessary fluff as much as possible. Without further adieu, let's get into it!

## BoM Addendum 

First up, the BOM! I've included a list of everything that was excluded from the original BoM that is necessary for basic functioning of FLEXI, in the file `bom_addendum.csv`.

Not included in this mini-BoM is zipties, which I think are pretty common
for labs to have, and aren’t *necessary*, but will help you with cable management.

## Aluminum Parts Fabrication

Next, since most of the structural parts of FLEXI are made of cut aluminum, I'm including some guidance on that. I can't tell you how to work whatever equipment is available to you, but I can advise on buying the material and laying it all out. 

A note for buying the stock, I was able to make an 8" by 8" sheet of .190" thick aluminum work for the largest part, `circular_base.dxf`. If you're not deeply confident in your ability to set up your cutting equipment with precision, you probably want to get a larger sheet, as this part has a diameter of 200 mm, allowing for only 3 mm of tolerance (8" = 203 mm). For purchasing the materials, I've included a little table of what to get, in the file `alu_stock.csv`.

The [OSF](https://osf.io/dbg6h/) repo contains the .dxf files for cutting all the parts for FLEXI, and then you can use a nesting software, such as [Deepnest](https://deepnest.io/) to arrange the parts on your stock sheets. 

## Construction

Another goal of this document is to supplement the original instructions for building FLEXI. In building **Violet**, I had a lot of trouble with these instructions, especially since it looks like they tried to fit the entire process on one page, with varying results. There are also simply a few typos and mistakes that I'd like to save you some time with. 

## Wiring

The wiring documentation in the original paper is... lacking. I'm not convinced that this isn't a strange choice, but you may have noticed that it calls for a car charger for the Surface Pro, and then that is wired into a barrel plug in parallel with the U2D2. **Note**, by the way, that the U2D2 is wired differently for FLEXI than what the U2D2 [e-manual](https://emanual.robotis.com/docs/en/parts/interface/u2d2/) says. Otherwise, I found that the manuals from Robotis for the motors and U2D2 were very helpful.



