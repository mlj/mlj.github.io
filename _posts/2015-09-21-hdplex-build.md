---
layout: post
title: HDPLEX H1.S fanless Haswell build
---

Last winter I finally had enough of fan noise from my desktop computer and started to plan a fanless desktop build. I wanted a small form factor, Haswell architecture and the best possible integrated GPU.

In a fanless build the crucial component is the case. I narrowed my list down to Streacom FC8EVO (MiniITX, max. TDP 95 W), Akasa Euler (ThinITX, max. TDP 35 W) and the HDPLEX H1.S (ThinITX or MiniITX, max. TDP 65 W).

The Akasa would have been the cheapest and also the smallest. But the combination of a ThinITX motherboard and a low maximum TDP limits the choice of possible components, which in turn can push the price up. The Streacom is the opposite; factoring in the price of the power supply it would have been around 20% more expensive than the Akasa and the largest of the three. In the end I chose the HDPLEX H1.S, in part because of promising early reviews and in part because a MiniITX motherboard I had on my list of compatible motherboards suddenly dropped substantially in price on Amazon.

I recycled two SSDs and memory from a previous build. All that was left was to pick a CPU. To the get the best GPU available with Haswell I would have had to choose an i5 or an i7, but I chose an i3-4330 as a balance between price and the optimal GPU.

The build took about four hours and, as expected, required patience and some creative cable management. I would not recommend this as a first-time build as you have to plan ahead and figure out exactly how to squeeze all the components in, and the instructions leave some important steps out. Photographs of the motherboard you plan to use are crucial. Keep an eye out in particular for conflicts between the heat pipes, power connectors and vertically mounted batteries. With my chosen motherboard the heat pipes leave only two of the SATA connectors in the clear and block the vertical mini-PCIe slot for the included Wifi and Bluetooth card.

{% include image.html img="images/hdplex1.jpg" title="Case components" caption="There a plenty of pieces to keep track of." %}
{% include image.html img="images/hdplex2.jpg" title="USB cable" caption="The thick black cable is a double USB cable that had to be gently bent out of the way when the lid came on." %}
{% include image.html img="images/hdplex3.jpg" title="Motherboard" caption="The mini-PCIe slot is obscured by the heat pipes on the left, as are the remaining SATA slots." %}
{% include image.html img="images/hdplex4.jpg" title="Front panel" caption="The fanless PSU is attached to the front panel." %}
{% include image.html img="images/hdplex5.jpg" title="Front panel detail" caption="The green coil had to be nudged a bit in order to plug the connector next to it." %}
{% include image.html img="images/hdplex6.jpg" title="Vertical plate" caption="The vertical plate holds the heat pipes in place, but the external power cable connector conflicts with one of the screws that attach it to the case and it cannot be moved further right without interfering with the heat pipes." %}
{% include image.html img="images/hdplex7.jpg" title="Complete build" caption="The complete build fills almost all available space." %}

The results are excellent. I have now had this system for almost a year and have been surprised by its stability and performance. Under light load the temperature hovers in the 35°C-40°C range. As I am writing this, the ambient temperature is 19°C and `sensors` reports the following:

```
Physical id 0:  +36.0°C  (high = +80.0°C, crit = +100.0°C)
Core 0:         +36.0°C  (high = +80.0°C, crit = +100.0°C)
Core 1:         +35.0°C  (high = +80.0°C, crit = +100.0°C)
```

After a period of slightly heavier load, such as after a longer coding session where I swap between editing, compiling, running tests and so on, the temperature will fluctuate around 55°C, spiking to 60°C under full load.

I have not subjected the system to a stress test like Prime95 but I would not be surprised if the temperature approached the danger zone under such conditions. But the load that a stress test puts the system under is unlike anything it will experience with my usage pattern and it is not what I built the system for.

The only issue I have had is interference with mobile phones. If I place a mobile close to the case, the screen will go blank or fill with random noise. Something here is not shielded the way it should be. I have not looked into this and it may simply be caused by something like a cheap HDMI cable.

Component list:

  * [HDPLEX H1.S fanless case](http://www.hd-plex.com/hdplex-h1.s-fanless-computer-case.html) with 120W Internal AC-DC and 160W DC-ATX Fanless Power Supply
  * [ASRock H97M-ITX/ac motherboard](http://www.asrock.com/mb/Intel/H97M-ITXac/)
  * [Intel Core i3-4330](http://ark.intel.com/products/77769/Intel-Core-i3-4330-Processor-4M-Cache-3_50-GHz)
  * 2 x [Corsair XMS3 4GB DDR3 1333MHz C9](http://www.corsair.com/en/cmx4gx3m1a1333c9)
  * [Crucial BX100 250GB SATA SSD](http://www.crucial.com/usa/en/ct250bx100ssd1)
  * [Corsair Force 3 SSD 120GB SATA SSD](http://www.corsair.com/en-gb/force-series-3-120gb-sata-3-6gbps-solid-state-hard-drive)
