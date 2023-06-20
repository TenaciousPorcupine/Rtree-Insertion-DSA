# Problem Statement 1
## R Tree Insertion


To run the code either run the treesript.sh file which inputs data from data.txt and outputs the final rtree stucture to the file finaloutput.txt

    sh treescript.sh 
Or you can run the following codes to output the result onto the terminal

    gcc -c DSA_Assigment_Group_16.c
    gcc DSA_Assigment_Group_16.o
    ./a.out <filename.txt>

To change parameters of rtree structure, change the following code snippet in line 768 and edit the data you want to change as below:

    struct Rtree *rtree = new_rtree(<max_entries>, <min_entries>, <numofdimensions>);

The print structure is as follows :
- if node is a non-leaf node the following is printed 

[< ```depth``` >] Internal Node with <num_of_childs> children. Bounds : (<min of 1st dimension>, <min of 2nd dimesion> , ...) (<max of 1st dimension>, <max of 2nd dimesion>, ...>)
- if node is a leaf node, then it must have pointers to all tuples and is represented

[< ```depth``` >] Leaf Node: (<tuple_1>) (<tuple_2>) ... (<tuple_{num_of_tuples}>)
- If depth is zero it denotes the root node.
- All the leaf nodes are at the same depth.
