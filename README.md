Integrity Verifier
==================

``BSTree`` and ``HCTree`` are programs for creating data structures with embedded information. ``BSTree`` and ``HCTree`` can both be used to determine whether the original data was modified or not. ``BSTree`` can also be used to pinpoints which item (if any) has been modified.

http://web.ics.purdue.edu/~pritchey/courses/cs426/project.pdf

Download
--------
```
$ git clone https://github.com/lirongyuan/IntegrityVerifier.git
```

GUI Setup:
----------
A program with graphic user interface -- integrityVerifier.java is built for this project.
```
$ javac integrityVerifier.java
$ java integrityVerifier
```

GUI Usage:
----------
A. Input for part1a:

* Tree construction:

  * Data File: ``BST/bst_test_data.txt``

  * Key File: ``BST/test_key.txt``

* Tree verification:

  * Tree File: ``BST/1a_clean.txt`` or ``BST/1a_dirty.txt``

  * Key File: ``BST/test_key.txt``

B. Input for part1b:

* Tree construction:

  * Message File: ``HCT/huff_test_mssg.txt``

  * Key File: ``HCT/test_key.txt``

* Tree verification:

  * Tree File: ``HCT/1b_dirty.txt`` or ``HCT/1b_clean.txt``

  * Key File: ``HCT/test_key.txt``

C. Input for part2:

* Tree construction:

  * Data File: ``BST/bst_test_data.txt``

  * Key File: ``BST/test_key.txt``

* Tree verification:

  * Tree File: ``BST/2_clean.txt`` or ``BST/2_dirty.txt``

  * Key File: ``BST/test_key.txt``

Setup:
------
Alternatively, you could use the programs in terminal.
```
$ javac BSTree.java
$ javac HCTree.java
```

Usage:
------
To get the usages for the programs, type the following:
```
$ java BSTree
$ java HCTree
```



