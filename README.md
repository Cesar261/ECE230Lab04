# Lab 04 - SOP/POS and KMaps

In this lab, you’ve learned how to apply KMaps, Sum Of Products and Products of
sums to simplify digital logic equations. Then, you’ve proven out that they work
using an implemented design on your Basys3 boards.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Summary
When it came to this lab it was the idea to simplify a Kmap and create one. We then implemented those simplified expressions in Verilog as minterm.v and maxterm. and verified in Vivado that they produced the exact same LED outputs as the unoptimized design.


## Lab Questions

### Why are the groups of 1’s (or 0’s) that we select in the KMap able to go across edges?
Due to the KMap rules we can group Edge variables similar to the ones in the middle that are neighbors 
### Why are the names Sum of Products and Products of Sums?
Sum of Products groups minterms where the output is 1 by ANDing variables together and ORing those resulting product terms.
on the other hand , Product of Sums (POS) groups maxterms where the output is 0 by ORing variables together and ANDing those resulting sum terms.
### Open the test.v file – how are we able to check that the signals match using XOR?
In this testbench, the XOR operator (^) compares the naive reference signal (led[0]) against the minterm and maxterm outputs (led[1] and led[2]). If both outputs match, the XOR calculation outputs a 0 and the testbench keeps running. But if there's any mismatch, XOR outputs a 1, causing the code to print an error, flip fail to 1, and stop the simulation immediately
