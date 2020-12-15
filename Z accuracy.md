I have recently begun to wonder if my V2's Z heights sometimes exhibit some kind of subtle math error (a rounding error, perhaps?)  The results of this hypothetical error are most visible when using Z-hop.  Consider, with fairly stock z settings (x16 microstepping):
### 0.2 Z-hop
![Zhop](https://raw.githubusercontent.com/shiftingtech/Voron/main/Images/x16_interpolate_hop.jpg)
vs
### no Z-hop
![no Zhop](https://raw.githubusercontent.com/shiftingtech/Voron/main/Images/x16_interpolate_nohop.jpg)
There are a handful of horizontal lines running all the way through the part, as if a few layers were slightly out of spec height.

Now, the most obvious explination for the characteristic lines is a mechanical issue that's exagerated by the extra hopping.  Still, I wanted to test if that's all that's going on.  Note: all photos were taken at whatever angle of light started to show the first surface abberations.  I wanted to make sure that the layer errors weren't simply being hidden by lighting angle in some photos

It seemed to me that if I reduce my microstepping, any small math errors would likely get lost, but any actual mechanical issues would remain largly unchanged.
I printed an object with Z hop, but with my microstepping reduced to 2 (step_distance=0.02).  Full steps would have been great, but a step_distance of 0.04 would have meant my 0.2 layers didn't divide nicely by the step_distance.  That seemed like an unnecessary complication.

### x2 microstepping, with 0.2 z-hop
![x2 Microstepping, with 0.2 Z-hop](https://raw.githubusercontent.com/shiftingtech/Voron/main/Images/x2_nointerpolate_hop.jpg)
To my eye, this print is as good as the no-zhop print, but with zhop.  I had some challenges with this setting though.  With such a low microstepping, it was extremely hit-or-miss whether or not QGL would actually succeed.  (Also, fun facts:  want to make your fancy 3d printer sounds like a classic Dot Matrix printer?  This is how you do it....)

Of course, it is always possible that the motors were somehow fundamentally performing differently at the vastly reduced microstepping: they certainly SOUNDED different...  So this brought me to one more test:  x4 microstepping, with interpolation turned on.  
(note:  the move to X4 microstepping wasn't really part of the test, I just did that so QGL would be a little more usable)
### x4 microstepping, interpolation on, with 0.2 z-hop
![x4 microstepping, interpolation, with 0.2z-hop](https://raw.githubusercontent.com/shiftingtech/Voron/main/Images/x4_interpolate_hop.jpg)

So, first of all, I'm liking this oddball configuration on Z:  x4 microstepping, interpolation on. But it also seems to bear out my theory:  when we're running very small step_distances, there may be some sort of math error as a result.

