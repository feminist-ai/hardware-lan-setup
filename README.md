# hardware-lan-setup
Get your own LAN and hardware running to host a Feminist AI LAN Party

More readable and updates coming soon, please stay tuned 😎

-----

1. Supply list and buying instructions
- equipment you definitely need
- how to measure and choose compatibility
-> largest things must fit in together in some sort of lego geometry, how to choose dimensions?
-> many steps to double check the dimensions:
---> GPU will be one of the largest (length)
---> power supply
---> heat sink
---> all with clearance
-> case and motherboard have to fit the same form factor
-> CPU and motherboard must match (form factor) and make sure that the CPU and the head sink for the CPU appropriately fit

2. computer setup

look at case manufacturer for recommendations on installation.

- power supply setup
- necessary tools and space to put it together
-> small screwdriver
--> make sure you have a flexible toolset that works for yourself iFixit has a good one but similar is also okay.
-> a place to hold screws and small materials
- order of operations
-> follow instruction sets!
-> motherboard fits where the faceplate sits
-> open casing on both sides
-> put the motherboard in but first ground yourself against static electricity
-> screw in motherboard (it should line up because there is a standard)
--> while you do that, try to make sure that you don't touch the contacts / traces / metal
--> if you want to build using a strap then you can touch more stuff
--> always use screws that came from the vendor !!!

- then put in the hard drive
--> if your motherboard comes a protective area for the harddrive make sure that you order a harddrive that fits that protective area. For example, many gaming motherboards already have advanced heat sinks for your harddrive, so you can order a bare harddrive rather than a more expensive harddrive with its own heat sink. In our case, we accidentally didn't check this beforehand and had to improvise a small bit of sticky tape to install the hard drive without directly gluing it to the motherboard. Remember: improvisation can be a nice way to fit together bits of a computer!

TODO: update shopping list with proper harddrive and memory sticks

- DDR memory choice and installation (DDR 5 changes the way that you can pin memory into motherboards, so make sure that you have DDR memory that fits your motherboard)
- pretty much everything on your motherboard is keyed so before you press in your memory line it up and make sure it looks like the pins line up and the gap in teh middle lines up. this is a good rule for any of your other connectors too, the pins, any divets or other clear gaps should line up between the cables and what you push in
- when installing the RAM get it lined up properly and then push it evenly on both sides down until it clicks into the board

- install GPU
--> make sure that when it fits, it's supported correctly by the case and by the PCI connects on the motherboard (for example, it might have a support bar to support the graphics card.)
--> make sure the other motherboard header connections (cables) aren't blocked or inaccessible due to the GPU. For example you migth also want to make sure your cables don't get in the way of hte GPU fans.
- for example, our GPU had screws that go into the front of the case and this was enough to hold it up properly
- if your GPU might block other cords, you can plug those in first so that you don't have to move the GPU again to get to the cables

- install CPU
--> pull up whatever caging element from the motherboard for the CPU, it will usually look like a small gate (this is related to the form factor standard - which you shoudl have already checked in your shopping)
--> follow the directions for your particular enclosure, there are a few different ways that the latches work
--> there will be a keying symbol (like on mine it is a triangle) in the corner to help you orient it. match the key on your CPU to the motherboard. take off sticky area and make sure your placement is correct.
--> there are many small pins on a cpu and on the motherboard connection to the CPU. If you don't connect it correctly, you can break both the CPU and teh connections for the motherboard.
--> carefully place the CPU so that the keys are matching and the CPU connects flat onto the motherboard. TO test that all pins are correctly matched, place your finger on the CPU and try to wiggle it gently back and forth. If the CPU moves, not all of the pins are installed properly. If that happens, pick up the CPU again, recheck the key and then gently place it again on the mount and try to make sure all four corners are even and appropriately placed.
--> then close the cage/enclosure

- install heat sink
--> follow heat sink instructions for installation! For example, on our installation we needed to remove the plastic mounts before installing the heat sink.
-->  It can be useful to also look at your motherboard instructions to ensure there aren't any special placement instructions for your heat sink
--> usually the heat sink instructions will tell you how to exactly set up the mounting before installing the heat sink itself.
--> wave bye to your CPU before you install it and thank it for its hard work
--> then GLUEEEEE (we actually decided it was bad because it should be liquid-y!) - we want the best transfer of heat to the heat sink, you want liquidy because air bubbles in the heat sink will be awful for your CPU since AIR is not a good convection). If you want a long life for your CPU (which you do), you want a glue/paste that is high quality. You'll be able to tell the difference !
--> put the glue near the middle and spread up and down.
--> then, place the heat sink in the middle and wiggle it in circles applying light pressure down and back and forth to appropriately spread the glue across the CPU and heat sink attachment. You want an even application with no air bubbles.
--> Then you'll screw in the heat sink to attach to the hardware mounts that you already installed as per the heat sink instructions you followed. If you have one with springs, make sure the screws are lined up correctly and screw each side a little bit at a time until they catch and then keep going one little bit by little bit until both sides are evenly screwed in
--> then you want to install the fans on each side of your heat sink. They need to attach to the motherboard for power, and you might need to read the motherboard instructions to make sure that the connectors you use are appropriately marked as main CPU fans because some BIOS will get angry if the CPU fans aren't on the correct connections.
--> there will usually be a keyed setup, where you can see guiding lines on the side of the power connectors and those will match up with some guides on the motherboard. In our case, there were two small divets in both.
--> ours had some RGB lighting and then extra plugs with connectors on the motherboard for those connections
--> because our motherboard only had one power connector for the CPU fans, it also came with a splitter that allows you to power 2 fans for the power connector of one! ;)

- hooking up power!
your power supply came with a bunch of funky looking cables so that everything in your computer gets power! you'll run that cabling from the power supply connectors to your board/cards.
- again, pay attention to keying, everything should match before you push it in
- apply even pressure when possible
- look at the specs on your motherboard (complete with version) to see if it has one or many power sources

- hook up the rest of your cables.
- you might need to remove your fans or move things around to get all cables installed


3. network equipment and setup
- example setup with switch

4. installations
- operating system
- python, cuda
- download models: huggingface CLI / llamafiles / pytorch etc
- setup inference or training

5. attendees
-> adapters to bring
-> how to link multiple computers together
-> network addressability

6. example LAN use cases

-> attacking larger LLMs
-> sharing model and data files locally
-> communal training


------

Software setup

- shared file server
- shared psql or other reachable database
--> note wrt psql clients that some will not play nice with local connections
- vllm serving for llms
- comfyui + flux or other models via docker for image gen

