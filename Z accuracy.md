I have recently begun to wonder if my V2's Z heights sometimes exhibit some kind of subtle math error (a rounding error, perhaps?)  The results of this hypothetical error are most visible when using Z-hop.  Consider, with fairly stock z settings (x16 microstepping):
![Zhop](https://raw.githubusercontent.com/shiftingtech/Voron/main/Images/x16_interpolate_hop.jpg)
vs
![no Zhop](https://raw.githubusercontent.com/shiftingtech/Voron/main/Images/x16_interpolate_nohop.jpg)
There are a handful of horizontal lines running all the way through the part, as if a few layers were slightly out of spec height.


It seemed to me that I could test the theory, by significantly reducing my microstepping, so that any very small math errors would become "much less than a step" and get lost.
So I printed an object with Z hop, but with my microstepping reduced to 2 (so step_distance=0.02)  It did not exhibit the errors.
Next I needed to test whether it was 
