# Isomorpher

The file *isomorpher.cpp* is a C++ program that allows you enter an input graph in the [Peregrine](https://github.com/pdclab/peregrine) format and it will exhuastively generate all V! isomorphic variants of the pattern (where V is the number of vertices). It writes each variant in a seperate output file in the current directory and can addtionally generate LaTeX source code that displays each of them. 

The program accepts two file inputs, one named **pattern.graph** that contains each of the edges of the source pattern. An example of this is shown below for a "house" patern: 
```
1 2
1 4
1 5
2 3
2 5
3 4
```

The other input is only neccesary for the purposes of the LaTeX display. It should be named **pattern.txt** and contain the absolute coordinates of the vertices in the graph, where 0 0 is the top center position. Regardless of the order of the edges in .graph file, the .txt must have each coordinate on the line number respective to which vertex it corresponds to. An example of this for the "house" pattern: 
```
-0.75 -1
0.75 -1
0.75 -2
-0.75 -2
0 0
```

To run the program, use 
```console
g++ isomorpher.cpp
./a.out
```
Since it is exhuastively generating all patterns, be wary of patterns with large amounts of vertices.
