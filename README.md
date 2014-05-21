SimpleScalar 3.0 with piecewise linear branch predictor
=======================================================

What is piecewise linear branch predictor?

see http://faculty.cse.tamu.edu/djimenez/pdfs/isca05_dist.pdf


Piecewise linear branch predictor suggested in the paper above is implemented and can be evaluated via following command:
```Shell
sim-bpred -bpred piecewise [-bpred:piecewise _n_ _m_ _h_] [other simulator options] [program binary] [program args]
```
It can be configured with 3 parameters, n, m, and h. See the paper linked above §5.1, §6.3 for more details on these parameters.


Every other functionality remains the same as original distribution including sample branch predictors.


Note that this version of SimpleScalar simulator is configured to be compiled on Mac OS X 10.9 only.
To compile on Linux or other os, you should re-download the whole simulator from http://www.simplescalar.com/ then replace original bpred.c, bpred.h, sim-bpred.c with the files on this repo.

Every modification from original distribution is commented with prefix 'XXX'. So find
```C
// XXX: blahblah...
```
or
```C
/* XXX: blahblah... */
```
to see what modifications were made.
