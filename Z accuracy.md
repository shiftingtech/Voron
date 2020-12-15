I have recently begun to wonder if my V2's Z heights sometimes exhibit some kind of subtle math error (a rounding error, perhaps?)  The results of this hypothetical error are most visible when using Z-hop.  Consider, with fairly stock z settings (x16 microstepping):
###0.2 Z-hop
![Zhop](https://raw.githubusercontent.com/shiftingtech/Voron/main/Images/x16_interpolate_hop.jpg)
vs
###no Z-hop
![no Zhop](https://raw.githubusercontent.com/shiftingtech/Voron/main/Images/x16_interpolate_nohop.jpg)
There are a handful of horizontal lines running all the way through the part, as if a few layers were slightly out of spec height.

Now, the most obvious explination for the characteristic lines is a mechanical issue that's exagerated by the extra hopping.  Still, I wanted to test if that's all that's going on.

It seemed to me that if I reduce my microstepping, any small math errors would likely get lost, but any actual mechanical issues would remain largly unchanged.
I printed an object with Z hop, but with my microstepping reduced to 2 (so step_distance=0.02)  

###x2 microstepping, with z-hop
![x2 Microstepping, with Z-hop](https://raw.githubusercontent.com/shiftingtech/Voron/main/Images/x2_nointerpolate_hop.jpg)

