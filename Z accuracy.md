I have recently begun to wonder if my V2's Z heights sometimes exhibit some kind of subtle math error (a rounding error, perhaps?)


It seemed to me that I could test the theory, by significantly reducing my microstepping, so that any very small math errors would become "much less than a step" and get lost.
So I printed an object with Z hop, but with my microstepping reduced to 2 (so step_distance=0.02)  It did not exhibit the errors.
Next I needed to test whether it was 
