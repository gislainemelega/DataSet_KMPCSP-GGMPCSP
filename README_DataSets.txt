
***************************************************************************
*									  *
*			   DataSet_KMPCSP-GGMPCSP			  *
*									  *
***************************************************************************

- How the data set is generated:

I.    Each 3 classes are generated with the same items types (length and wire configurations) and demand matrix (same number of items and periods) - the difference between them is the capacity, which varies according to the parameter Factor;

II.   EVERY item has nonnull demand at least in one period (regardless which wire configuration is requested);

III.  Items length range between 1 and 11 using up to 2 decimals;

IV.   Demand matrix has integer elements ranging from 0 up to 20;

V.    Number of items length varies between 10, 25, 40 and 55;

VI.   Number and types of tensions are the same in all instances (|T| = 7, f[tau] in {0, 8, 10, 12, 14, 16, 18};

VII.  Mold length is fixed in W = 90 meters;

VIII. Number of periods varies between 5, 10 and 15;

IX.   Only 3% of demand matrix elements is nonnull.


***************************************************************************

- How to read a "ClassXXExXX.dat" file:

According to the disposal of the elements in the file, we read the following parameters:

|I|	|T|	|P|	|K|	Factor     W      c
Cap[p]   --- (for p=1, ..., |P|)
f[tau]   --- (for tau=1, ..., |T|)
w[i]     --- (for i=1, ..., |I|)
h[i][p]  --- (for i=1, ..., |I| and p=1, ..., |P|)
d[i][beta][p] --- (for i=1, ..., |I|; beta=1, ..., |T| and p=1, ..., |P|)

where

I = set of items;

T = set of wire configurations;

P = set of periods;

K = set of available molds;

Factor = multiplier to calculate the capacity;  (see section 6.1 Data set of the manuscript)

W = mold length;

c = cost of a meter of steel wire;

Cap[p] = number of available molds in period p;

f[tau] = number of steel wires in the wire configuration tau;

w[i] = length of item i;

h[i][p] = unit holding cost of item i in period p;

d[i][beta][p] = demand of item i with wire configuration beta in period p.


***************************************************************************

End of README file.
