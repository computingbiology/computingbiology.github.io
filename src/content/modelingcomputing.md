+++
date = "26 Dec 2021"
draft = false
title = "Models of Computation"
author = "David Evans"
slug = "models"
+++

To reason precisely about what computers can and cannot do, we need
abstract models that capture the things we think are important but
avoid the complexities of physical objects.

<div class="shortsection">Models and Mathematics</div>

The physical world is messy and suffers from arbitrary limits &mdash;
  this applies both to the physical computing devices we use (which
  always have some probability of failing and can't even do arithmetic
  correcly) and even more so to biological systems we consider in this
  class. Mathematics is precise and unconstrained &mdash; we can
  define formal systems that always behave in the prescribed way, can
  do operations without generating heat, and can be
  infinite. Mathematical models are useful because we can reason about
  them using the formal tools of mathematics, and can abstract away
  physical complexities and finite limits of physical
  reality. Mathematical models have proven uncannily useful in
  understanding and predicting properties of the physical world, but
  when we use them we have to be mindful that they are abstractions
  that avoid many of the messy aspects of physical reality.

<div class="additionalreading">
<center><b>Additional Materials</b></center>

- Eugene Wigner. [_The Unreasonable Effectivenss of Mathematics in the Natural Sciences_](/docs/wigner1960.pdf).  Communications in Pure and Applied Mathematics, 1960.
- Richard Hamming. [_The Unreasonable Effectiveness of Mathematics_](/docs/hamming1980.pdf). The American Mathematical Monthly, 87(2), 81–90.
- For an important counter-argument, see Alon Halevy, Peter Norvig,
  Fernando Pereira, [_The Unreasonable Effectiveness of
  Data_](/docs/halevy2009.pdf), IEEE Intelligent Systems, 2009. See
  also Peter Norvig's talk [_The Unreasonable Effectiveness of
  Data_](https://www.youtube.com/watch?v=yvDCzhbjYWs), October
  2011. [Norvig](https://www.youtube.com/watch?v=PI8Fo1vzUPM) starts
  with the observation that Wigner's claims about the effectiveness of
  simple mathematics to explain the universe are valid for a
  physicist, but not for biology - very little in biology can be
  explained with a short, simple equation. (The rest of the talk is
  about effectiveness of ML to solve problems in vision and language,
  but doesn't return to biology.)
  </div>

<div class="shortsection">Modeling Computers</div>

To model a _computer_, we need to: (1) define
a set of mathematical objects that correspond to instances of the
computer we are modeling; and (2) define an execution model that shows
how any element in that set in that model executes. Note that when we
say _computer_ in theoretical computer science, we mean a complete
computing system &mdash; there is no separation between "hardware" and
"software" as there is in informal use of "computer" as a physical
device that doens't do anything without its program. In our
theoretical computing models, the input may include a description of a
program (and often does), but the mathematical object that we are
modeling includes everything needed to perform a computation.

An _execution_ of a computer takes (1) an _input_, (2) does _some
processing_, and (3) produces an _output_.  So, the execution model
for a model computer needs to explain how the input is represented
(typically by a finite string of bits), and how processing is done
(this typically requires defining some kind of abstract machine that
operates on the input, and uses some kind of _storage_ (also called
_memory_) to keep track of what it is doing), and a way to know when
an execution is finished and to interpret the final state of the
abstract machine (including its memory) as the _output_. 

<div class="additionalreading">
<center><b>Additional Materials</b></center>

- [Defining Computation](https://introtcs.org/public/lec_03_computation.html), Chapter 3 of Boaz Barak's [_Introduction to Theoretical Computer Science_](https://introtcs.org/) book (this is the book I have used when I teach or co-teach [cs3102: Theory of Computation](https://uvatoc.github.io/), so most additional materials lists will include other chapters from the book, which we refer to as the _TCS book_).

- Video lectures (by Nathan Brunelle) from [cs3102 course](https://uvatoc.github.io/f20/week2/): [_What is a Computer?_](https://www.youtube.com/watch?v=L3ueFMGM6pk) (7:30); [_Modeling Computers_](https://www.youtube.com/watch?v=Zg4FUYbwLqY&feature=emb_imp_woyt) (8:16).
</div>

<div class="shortsection"><a name="terminology"></a>Terminology</div>
We discuss two examples of computing models soon, but first introduce some important terminology. When discussing computing, several terms that are often used
informally are used in a very precise way and the precise definitions
of these terms are important for understanding what statements using
them mean both in theory, and what such statements imply in
practice. Some important terms to understand precisely:

- **Functions**: a _function_ is a relation that maps an input to an
    output. The set of possible inputs to a function is known as the
    _domain_; the set of possible outputs is its _codomain_. If the
    function is defined for all elements of the domain it is _total_;
    if not, it is _partial_. A function is defined by how it maps
    inputs to outputs, and there are many different ways to describe a
    function. A finite function (where the input size if fixed) can be
    defined by a table that gives the output for each possible input
    (as the input size becomes larger than a few bits, though, this
    becomes infeasible in practice, but it is still useful to think of
    functions this way). We can define more complex functions by
    giving the property the output should have. Note that the term
    function is often (mis)used by programmers and programming
    languages to mean a procedure for doing computation that takes
    some input parameters and returns an output. This is very
    different from a mathematical function, and the two should not be
    confused.
- **Algorithms**: an _algorithm_ is a precise description of steps to
    perform. An algorithm _computes_ a function if it is guaranteed to
    always produce a correct output for any input (that is, it
    implement the input-output mapping of the function). This means it
    must always finish and output a result, and the output it produces
    must be the correct output for the given input. We talk about
    _solving_ a problem by providing an _algorithm_ that computes a
    function that satisfies the requirements of the problem.


<div class="additionalreading">
<center><b>Additional Materials</b></center>

- A good discrete mathematics course should make you comfortable thinking about functions, and the terms used above. If you are not confident on this material, read Chapter 4 of Lehman, Leighton, and Meyer's [_Mathematics for Computer Science_](https://uvacs2102.github.io/docs/mcs.pdf) (this is the book often used for [cs2102: Discrete Mathematics](https://uvacs2102.github.io/)).

</div>

<div class="shortsection">Boolean Circuits and Turing Machines</div>

Two useful and widely used theoretical models of computers are
_Boolean circuits_ and _Turing machines_ (in this class, we will
assume clear understanding of these models, and some variations on
them, and may also use a replacement grammar model of computation
(Lambda Calculus), but will introduce it in class).  We provide a
refresher summary of these two models below, but won't provide a
detailed introduction to these models here. So, if you are not already
familiar with them follow the links in the Additional Materials below.

<table>
<tr><th width="15%">Model</th><th width="37%">Boolean Circuit</th><th width="48%">Turing Machine</th></tr>
<tr><td align="center">Input</td><td><b>Fixed-length</b> sequence of bits, each input bit is one input wire for the circuit</td><td><b>Finite</b> sequence of bits of <b>any length</b>, written from left to write on a infinite tape. When the machine starts execution the rest of the tape is blank, and the tape head is at the leftmost (first) input bit.</td></tr>
<tr><td align="center">Processing</td><td>Boolean logical operations (e.g., <span class="op">AND</span>, <span class="op">OR</span>, <span class="op">NOT</span>) connected in an acyclic graph. Each Boolean operation (sometimes called a <em>gate</em>) takes a few input bits (e.g., 2 for <span class="op">AND</span> and <span class="op">OR</span>, 1 for <span class="op">NOT</span>) and outputs one output bit)

</td><td>State machine with a tape head, each step it can read the current square on the tape, write a new symbol in that square, move (<span class="op">left</span>, <span class="op">right</span>, or <span class="op">halt</span>), and transition to an internal state</td></tr>
<tr><td align="center">Termination</td><td>Always terminates since circuit is acyclic</td><td>Terminates if a <span class="op">halt</span> transition is executed (but may run forever without producing any output)</td></tr>
<tr><td align="center">Output</td><td>Values on the output wires of the circuit</td><td>Sequence of symbols on the tape when the machine terminates</td></tr>

<tr><td align="center">Functions</td><td>All finite functions</td><td>
The <em>computable functions</em> (by definition &mdash; the computable functions are defined as the set of functions that can be computed by a Turing Machine)</td></tr>

</table>


<div class="additionalreading">
<center><b>Additional Materials</b></center>

- For an introduction to the Boolean circuit model of computation see [Chapter 3.3](https://introtcs.org/public/lec_03_computation.html#booleancircuitsec) of the TCS book, and these video lectures from [cs3102](https://uvatoc.github.io/f20/week2/): [AND-OR-NOT](https://www.youtube.com/watch?v=spadNZCSkmk) (4:32), [_Programming with AND, OR, NOT_](https://www.youtube.com/watch?v=GpVEm7bAqH0&t=4s) (9:35), [_Boolean Circuits_](https://www.youtube.com/watch?v=lim78IpB8AI) (10:31).

- For an introduction to the Turing Machine model of computation see [Chapter 6: Loops and Infinity](https://introtcs.org/public/lec_06_loops.html) (TCS Book) and these video lectures from [cs3102](https://uvatoc.github.io/f20/week8/): [_Turing Machines_](https://www.youtube.com/watch?v=Xx_GeourSOQ&feature=emb_imp_woyt) (5:37), [_Turing Machine Examples_](https://www.youtube.com/watch?v=wN5DPmz0hgg&feature=emb_imp_woyt) (11:40), [_What was Turing's Model Modeling_](https://www.youtube.com/watch?v=E-OK7hSyMNE&feature=emb_imp_woyt) (includes review of other computing models) (15:56), [_Turing Machine Execution_](https://www.youtube.com/watch?v=fulQIGM0jUQ&feature=emb_imp_woyt) (9:13). 


  </div>

<div class="shortsection">Universality</div>

One of the most important insights that comes from formally modeling
  computing is that the sets of functions that can be computed by
  particular computing models are very robust to slight (and sometimes
  even major) changes to the model, and many seemingly very different
  models of computing can compute exactly the same sets of
  functions. This ability to make one machine do anything is why
  programming is so powerful: using one simple (at least abstractly)
  computing engine, we can perform any computation by finding the
  right program.

For _finite functions_ (where the input to the function is a
fixed-length binary string), there is a Boolean circuit that computes
every finite function using only two-bit <span class="op">AND</span>,
two-bit <span class="op">OR</span>, and one-bit <span
class="op">NOT</span> operations. We can compute exactly the same set
of functions (that is, all finite functions) using Boolean circuits
composed of just two-bit <span class="op">NAND</span>. This can be
proven by showing how to compute the each of the <span
class="op">AND</span>, <span class="op">OR</span>, and <span
class="op">NOT</span> operations using a Boolean circuit made of only
<span class="op">NAND</span> gates. We call sets of gates that can be
used as the components of Boolean circuits that are capable of
computing every finite function a _universal gate set_.

For functions where the input length is unbounded (but still finite),
a Turing Machine is _universal_, in the sense that it can compute
every function that can be computed by every other ``reasonable''
computing model. (What it means for a computing model to be reasonable
is either circularly defined as those that are equivalent in power to
a Turing Machine, or defined intuitively as anything that could be
done by a human computer following precise rules with unlimited
scratch paper, which was what Turing was originally modeling, but also
covers many variations on Turing Machines as well as more different
computing models like replacement grammars and random-access memory
machines.) We can prove a computing model is _universal_, but showing
that it can simulate a Turing Machine; we can prove that it is no more
powerful than a Turing Machine by showing how a Turing Machine can
simulate the new model.



<div class="additionalreading">
<center><b>Additional Materials</b></center>

- TCS [Chapter 3.7: Equivalence of all these models](https://introtcs.org/public/lec_03_computation.html#equivalence-of-all-these-models) proves that several models are equivalent to the Boolean <span class="op">AND</span>,
<span class="op">OR</span>, <span class="op">NOT</span> circuits.
- This video lecture shows the equivalence of <span class="op">NAND</span> circuits: [_Equivalence of NAND and AON Computing Models_](https://www.youtube.com/watch?v=VlcURykDg_A&feature=emb_imp_woyt) (9:35).
- TCS [Chapter 9: _Universality and uncomputability_](https://introtcs.org/public/lec_08_uncomputability.html) explains universal machines and how they were used to show that some problems are uncomputable.
- This video lecture is on [_Universal Machines_](https://www.youtube.com/watch?v=Ij01xiZDN8k&feature=emb_imp_woyt). (Bonus: [_Dori-Mic and the Universal Machine!_](https://dori-mic.org/) - this children's book has been called ["The BEST babies' book about computational universality I've read."](https://www.amazon.com/review/R1TSEFIBYW9Y6I/ref=cm_cr_dp_title?ie=UTF8&ASIN=1495944980&channel=detail-glance&nodeID=283155&store=books).)
- To understand why there are some uncomputable functions (not necessary for this course, but you should want to know!), see [_Uncomputable Numbers_](https://www.youtube.com/watch?v=Cuf4zkYwGlQ&feature=emb_imp_woyt).
  </div>

# &nbsp;

**Next: [Computational Complexity](/complexity)**



