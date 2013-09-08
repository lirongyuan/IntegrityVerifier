Program Description
=========

Part 1: Integrity verification

For this part of the project the goal is to write software for creating data structures, with embedded information, that will subsequently be used to determine whether the original data was modified or not.

Part 1a: A balanced search structure

Given n sorted and distinct data items d_1 < d_2 < ... < d_n, the goal is to write software that creates a binary tree T that

1. has O(log n) depth because, for every node v of T , if the subtree of v contains m items then the item at v has rank between m/4 and 3m/4;

2. has the "search property" (i.e., the item at each node v of T is greater than any item in v's left subtree and smaller than any item in v's right subtree);

3. encodes a hash-based message authentication code (HMAC) of the concatenation of all the (d_i)s (in sorted order).

Part 1b: A Huffman coding tree

Given a message M (as an array of bytes) and an alphabet Σ of n symbols along with their respective probabilities, the goal is to write software that creates a Huffman tree T that

1. corresponds to a prefix-free binary code with minimum expected codeword length;

2. encodes a hash-based message authentication code (HMAC) of the message being compressed.

Part 2: Pinpointing the corrupted item

This part will use the binary search tree from part 1a. Because for large n the θ_T is so much longer than the number of bits in an HMAC, this part consists of storing 1 + log n HMACs in the θ_T , using the scheme presented at
CombinatorialGroupTesting.pdf.

The goal of the software is that, given the n sorted items and the HMAC key K, produces the tree T with the 1 + log n HMACs stored in its θ_T (as many times as will fit). You have to also write software that, given a properly created T, pinpoints which item (if any) has been modified.

Instructions
=========
In terminal, type the following:

$ javac integrityVerifier.java

$ java integrityVerifier

A. Input for part1a:

Tree construction:

  Data File: BST/bst_test_data.txt

  Key File: BST/test_key.txt

Tree verification:

  Tree File: BST/1a_clean.txt or BST/1a_dirty.txt

  Key File: BST/test_key.txt

B. Input for part1b:

Tree construction:

  Message File: HCT/huff_test_mssg.txt

  Key File: HCT/test_key.txt

Tree verification:

  Tree File: HCT/1b_dirty.txt or HCT/1b_clean.txt

  Key File: HCT/test_key.txt

C. Input for part2:

Tree construction:

  Data File: BST/bst_test_data.txt

  Key File: BST/test_key.txt

Tree verification:

  Tree File: BST/2_clean.txt or BST/2_dirty.txt

  Key File: BST/test_key.txt

Working parts
=========
1. Balanced search tree(BSTree.java) and Huffman tree(HCTree.java) are both working correctly.

2. An awesome graphic user interface program(integrityVerifier.java) is built for this project.

3. If you prefer to use the programs in terminal, type "java BSTree" or "java HCTree" to get the usages.


