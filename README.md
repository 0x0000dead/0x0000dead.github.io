## Digital Lab.
### Task: 
Assume that you work for the Digital Processing Lab. They ask you to write a program with an input binary matrix `A`, which contains the pattern to search on other binary matrix `B`.   
The input file include the size and elements for both `A` and `B`. The recognition process consists in scanning row by row (horizontal scanning) the matrix B, when a pattern is located on `B` you must mark this pattern. To mark a located pattern change 1 to 2 and 0 to * on `B`.  
The output file of your program will be the matrix `B` with the located patterns marked.  
### Input
The first line of the input contains the size of `A`, next lines contains the matrix `A` row by row, next line contains the size of `B` and next lines contains the matrix `B` row by row.
### Output
The output is the matrix B with the located patterns marked.

Usage:
---
There are 2 version: User input / Google tests input
### User input usage: 
Via console: `mkdir build && cd build && cmake .. && make` then `./digital <input_file> <output_file>`.
### Google test usage:
Via console: `mkdir build && cd build && cmake .. && make` then `./digital`.

Complexity:
---
My implementation is `O(n1*n2*m1*m2)` time complexity, where n1,n2 - row/col size of martix `A` respectively. And m1/m2 - row/col size of matrix `B` respectively.

Mathematically proved, that there should be linear solution. So it's `Baker-Bird` algorithm. It can be found [e.g here](https://ocw.snu.ac.kr/sites/default/files/NOTE/4047.pdf). Due to not deep knowledge of KMP and Aho-Corasick algorithm, which using in `Baker-Bird` I haven't enough time to implement this `O(n1*n2+m1*m2)` solution.
