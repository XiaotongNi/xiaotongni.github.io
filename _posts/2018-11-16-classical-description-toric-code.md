---
layout: post
title: A very brief explanation of toric code
---

This is a very brief explanation of toric code for people without quantum information background.


### Toric code

Toric code is the prototype of many other 2D topological quantum error correcting codes. A variant of the toric code, the surface code, is what experimentalists plan to implement in the near future in solid state systems.

In this post, we will consider toric code with bit-flip noise. Under this restriction, the toric code becomes quite similar to a classical parity check code. However, you will need to accept some weirdness which I'm not going to explain. In the following figure, each edge represents one qubit (you can treat them as classical bits in this post). Note that we will use periodic boundary condition, which means that you can think the lattice is embedded on a torus. Together, the whole lattice encodes 2 qubits. Since classical bits are just the special case of qubits, we can also use the toric code to encode 2 classical bits. We claim that each encoded classical bit is equal to the parity of the qubits in the corresponding blue boundaries in the figure.

<img src="/toric_code_tutorial/toric_code_example.svg" alt="toric_code" class='center'/>

In the figure, we use small "x" to denote bit-flip errors happened on the qubits. Unlike classical error correction, we cannot direct measure each qubit. What we can do is measure the parity of four qubits adjacent to each plaquette. Without errors, all the parity should be even. Therefore, what we measure is the parity of the number of errors adjacent to each plaquette. We will put a dot at the plaquettes. Now we can state the decoding problem: **Given the location of the dots, decide whether we need to apply bit-flips to the encoded classical bits.** This is equivalent to deciding the parity of the number of "x" on each blue boundary.


