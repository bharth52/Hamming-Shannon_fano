# Huffman-Shannon_fano
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.
# Aim

 To compute the Average Codeword Length, Entropy, Efficiency, Redundancy, and Variance for a
 discrete memoryless source using Huffman and Shannon-Fano coding based on the given
 probabilities and codeword lengths.
 
# Tools Required

 To compute the Average Codeword Length, Entropy, Efficiency, Redundancy, and Variance for a
 discrete memoryless source using Huffman and Shannon-Fano coding based on the given
 probabilities and codeword lengths.
 
# Program
```````````````````````````````````````````````````````````````````````````````````````````````````
import numpy as np
 import math 
L  = 0
 hs = 0
 p = []
 lk = []
 n = int(input("Enter the number of Samples : "))
 for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
 for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
 for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
 for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
 hs = round(hs,3)
 eff = hs / L
 eff = round(eff,3)
 red =  round(1 - eff,3) 
var = 0
 for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
 print()
 print(f"Average Codeword Length is : {L}")
 print(f"Entropy is : {hs}")
 print(f"Efficiency is : {eff*100} %")
 print(f"Redudancy is : {red}")
 print(f"Variance is : {var}")
``````````````````````````````````````````````````````````````````````````````````````````````````````````````````````
# Calculation
![image](https://github.com/user-attachments/assets/f764d7e6-2bb4-431b-9c4f-02554f2a8ded)

![image](https://github.com/user-attachments/assets/b2993e81-c4f6-4162-a019-0acd6c30f9b4)

![image](https://github.com/user-attachments/assets/e48e8490-1cb7-47ae-b376-775d967b9506)

# Results.

 For the given probabilities {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25}:
 
 Average Codeword Length: 2.625
 
 Entropy: 2.625
 
 Efficiency: 100.0%
 
 Redundancy: 0.0
 
 Variance: 0.484
