# Inverse Matrix Finder
### [한글](READMEKR.md)
Old Matrix Finder From 2016... (KMLA AP Computer Science Class)

Works fine most of the time, but errors are reported in some edge cases. Do not use this in a precise operation.

If you want to change the decimal rounding, change [here](https://github.com/anaclumos/InverseMatrixFinder/blob/5fd78f958a49401d1022fc22ab70a0ac788968ee/Matrix.java#L109).

### Example Output

```console
➜  KMLA-APCS-Inverse-Matrix-Finder git:(master) java InverseMatrixFinder

This is an Inverse Matrix Finder.
How it works is simple.
We first set [A|I], and convert it to [I|B] with Gausssian Elimination and Back Substitution.
Then, B is the inverse matrix of A!

How many columns and rows will the matrix have? : 10
For Matrix A, Initialize Random values?
1      : Yes
Others : No
Decide : 1
For Matrix I, Initialize Identity?
1      : Yes
Others : No
Decide : 1

This is A in [A|I]:
-8.0    -2.0    +8.0    -3.0    +7.0    +8.0    -4.0    +2.0    +4.0    -7.0
-5.0    +7.0    -4.0    +1.0    +2.0    +6.0    +6.0    -5.0     0.0     0.0
-8.0    +7.0    +10.0   +8.0    +3.0    -1.0    -3.0    -7.0    +3.0    -8.0
+1.0    -1.0    +4.0    +3.0    +10.0   +2.0    -10.0   -7.0    -9.0     0.0
+3.0    +10.0   +10.0   -2.0    -7.0    -2.0    +1.0    +5.0    +5.0    -7.0
-2.0     0.0    -7.0     0.0    +2.0    -4.0    -2.0    +4.0    +1.0    -4.0
+6.0    -8.0    -10.0   +10.0   +8.0    +5.0    -2.0    -8.0    +10.0   +4.0
+6.0    +7.0    -9.0    +8.0    +9.0    +7.0    +8.0    +10.0   +8.0    -4.0
-5.0    -1.0    -10.0   +9.0    -7.0    -3.0    -6.0    -4.0    -10.0   +7.0
+1.0    +7.0    -6.0     0.0    +5.0    +1.0    +2.0    +10.0   -6.0    +10.0

This is I in [A|I]:
+1.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0    +1.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0    +1.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0    +1.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0    +1.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0    +1.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0    +1.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0     0.0    +1.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0    +1.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0    +1.0

***** After converting [A|I] to [I|B] form *****

This is I in [I|B]:
+1.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0    +1.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0    +1.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0    +1.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0    +1.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0    +1.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0    +1.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0     0.0    +1.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0    +1.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0    +1.0

This is B in [I|B], the inverse matrix of A.
-0.034  -0.007  -0.039  +0.045  +0.036  -0.016  +0.008  +0.021  -0.01   -0.023
-0.009  +0.058  -0.002  +0.021  +0.073  +0.039  +0.026  -0.028  -0.003  +0.039
+0.001  -0.045  +0.036  -0.009  -0.019  -0.067  -0.017  +0.005  -0.014  +0.009
-0.009  -0.056  +0.048  -0.014  -0.035  -0.058  -0.015  +0.055  +0.037  -0.014
-0.016  -0.006  +0.033  +0.018  -0.044  +0.026   0.0    -0.001  -0.049  +0.029
+0.061  +0.037  -0.06   +0.019  +0.038  -0.054  +0.006  +0.025  +0.042  -0.023
-0.046  -0.007  +0.034  -0.033  -0.091  -0.056  -0.056  +0.045  -0.032  -0.028
+0.03   -0.054   0.0    -0.021  -0.008  -0.01   -0.021  +0.031  +0.018  +0.019
+0.019  +0.006  +0.013  -0.04   +0.043  +0.032  +0.066  -0.043  -0.018  +0.036
+0.003  -0.008  +0.018  -0.031  +0.004  -0.032  +0.042  -0.047  -0.008  +0.076


Check if A * A^(-1) returns I: 
+1.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0    +1.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0    +1.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0    +1.0     0.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0    +1.0     0.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0    +1.0     0.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0    +1.0     0.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0     0.0    +1.0     0.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0    +1.0     0.0
 0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0     0.0    +1.0
Error: 3.5143762899814136E-16
Calculation time = 0.017s
```