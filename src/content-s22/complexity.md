+++
date = "26 Dec 2021"
draft = false
title = "Cost of Computation"
author = "David Evans"
slug = "complexity"
+++

When we consider the _power_ of our [computing models](/models), we
have been concerned with understanding what functions can be computed
(in theory, which means without any arbitrary limits on their
execution) by different computing models. When we want to actual
compute using physical computers, _cost_ matters. 

For concerete computations where we already know the input and have an
implementation of the algorithm, we can measure the cost of executing
the algorithm by just running it and recording the cost. That cost
could be measured in _dollars_ (which is very natural and concrete,
now that you can use cloud computing to rent computers by the
[minute](https://aws.amazon.com/ec2/pricing/#:~:text=EC2%20usage%20are%20billed%20on,with%20a%2060%20second%20minimum.)
or [tenth of
second](https://azure.microsoft.com/en-us/pricing/details/functions/)),
and this makes sense if we need to perform a similar computation many
times in the same way. We could also measure computation cost in
_time_ (latency, how long it takes to go from input to output),
_throughput_ (how many times we can perform a computation in a time
period), and _memory use_ (how much memory is needed to complete the
computation). All of these could be converted to money cost, but the
actual conversion would depend on the available computing
infrastructure.

Measuring cost this way is unsatisfactory since (1) it assumes we
already have a complete and executable program and know that it will
finish the way we are running it for an acceptable cost (otherwise, we
won't know how long to wait for it to finish if we are running it on
our own computer, or how large a computing bill we might run up if we
just let it run on the cloud), and, more importantly for our purposes,
(2) it provides little insight into how the cost will change if we run
the program on a different (possibly larger) input and as computing
power per dollar changes.


## Asympototic Complexity Analysis

Instead, we usually want to understand how the cost of executing an
algorithm varies with the size of the input, and want to measure that
cost in a precise (but abstract) way. The main goal of _complexity
analysis_ is to understand the cost to perform different computations
in a way that allows us to reason about algorithms and problems
without considering the details of a particular computing platform,
but in a way that captures important aspects of how the cost scales
with the input.

Our goal is to capture the cost of a computation with a function whose
input is the size of the input to the computation (a natural number),
and whose output is a measure of the cost (a non-negative real
number): \\( \ f: \mathbb{N}_+ \rightarrow \mathbb{R}^+ \\).

The cost is usually running time, measured in terms of the number of
steps it takes for some abstract machine (typically a Turing Machine
or RAM machine) to complete the execution. So, for example, we might want to measure cost by defining a function, \\( f(n) \\), that takes as input the size of the input to the function to compute, and outputs the number of steps a Turing Machine would require to complete the computation.

Since counting exact steps of a Turing Machine (or a RAM machine) is
tedious and error-prone, and our main interest is how the cost scales
with the input size, often instead of trying to find an exact cost
function we instead use _asymptotic operators_ to provide a set of
functions that characterize the cost (that is, instead of finding an
exact function that maps the input size to a cost, we find an
(infinite) set of functions that includes one element that is the
exact cost function, but we don't know which one it is).

The operator we use to describe the set of functions that grow as
quickly as some function \\( f \\) is \\( \Theta(f) \\). So, the set
\\( \Theta(n^2) \\) would be the set of all functions that grow
asymptotically as quickly as \\( n^2 \\). The formal definition of
what "grow asymptotically as quickly as'' is important, and explained
in the Additional Materials, but the main intuition you should have is
that multiplying by a constant (e.g., \\( 7 n^2 \\)) or adding a
constant or slower-growing term (e.g., \\( 3 n^2 + 12 n + 238 \log n +
274\\)) doesn't change the asymptotic growth, so all of these
functions would be in \\( \Theta(n^2) \\).

When we are talking about algorithms, we should understand the cost
well enough to (nearly) always get a tight \\( \Theta \\) expression
that characterizes the cost.  When we are talking about _problems_
(that is, computing a function where we do not necessarily know that
algorithm to use), then it is rare to be able to find a \\( \Theta \\)
expression for the cost. Doing so would require knowing something
about the _best_ possible algorithm that solves the problem (we don't know how to do this, even for simple problems like multiplication of integers). Then, we end up needing other notations to describe larger sets of functions. The \\( 
O \\) (omicron, sometimes called "big Oh") operator produces the set of all functions that grow _no faster than_ its input function. So, \\( O(n^2) \\) would include the functions \\( g(n) = 17n^2 + 23 \\), \\( g(n) = 2n + 7 \\), and \\( g(n) = 6 \\) (the constant function which outputs 6 for all inputs). The \\( \Omega \\) (omega) operator produces the set of all function that grow _no slower than_ its input function. So, the set \\( \Omega(n^2)\\) would include \\( g(n) = n^2 \\), \\( g(n) = 1.3n^3 \\), and \\( g(n) = 2^n \\), but would not include \\( g(n) = 17n \log n \\). For any function, \\( f \\), the intersection of \\( \Omega(f) \\) and \\( O(f) \\) is \\( \Theta(f) \\).

<div class="additionalreading">
<center><b>Additional Materials</b></center>

- [Chapter 7: Cost](https://computingbook.org/Cost.pdf) of [_Introduction to Computing &mdash; Explorations in Language, Logic, and Machines_](https://computingbook.org/) (my introductory computer science book that was developed for [cs1120](http://xplorecs.org/)) is an introduction to complexity analysis. (It includes more formal definitions of \\( \Theta \\), \\( O \\), and \\( \Omega \\), as well as showing how to analyze the cost of example programs.)
- Video lectures from cs3102: [_Cost of Computing_](https://www.youtube.com/watch?v=5H6DvmEzwDY) (5:03), [_Asymptotic Operators_](https://www.youtube.com/watch?v=96XtkxDNDCs) (7:06), [_Big-Oh Examples_](https://www.youtube.com/watch?v=iG_BGStzPQE) (17:03), [_Common Misuses of Asymptotic Notation_](https://www.youtube.com/watch?v=WLV99-6ep2c) (5:51).
</div>

## Tractable and Intractable Problems

Informally, _tractable_ just means "easy to do", and _intractable_
means "not easy to do". In computing, we use these terms more
strongly, and define the _tractable_ problems as those for which an
algorithm is known that can solve them and its running time is no
worse than polynomial in the size of the input. This is the complexity
class, <span class="cclass">P</span>, which is defined as the set of
functions that can be computed by algorithms with running times in \\(
O(n^k) \\) where \\( k \\) is any constant and \\( n \\) is the size
of the input. This is called _polynomial time_. 

Problems with known algorithms that complete in polynomial time are
considered _tractable_, and problems where the fastest known algorithm
requires more than polynomial time are considered _intractable_. For
example, if the best known algorithm for solving a problem has
exponential running time (e.g., in \\( \Theta(2^n) \\)), that problem
would be considered intractable, and cannot be practically solved for
non-tiny inputs.

The complexity class <span class="cclass">NP</span> can be defined as
the set of functions where it there is a way to check in polynomial
time if an output is correct, when given some additional information
(known as a _witness_). This class includes all the functions in class
<span class="cclass">P</span>, but might include some additional
problems. The most famous open problem in computer science (and one of
the [Clay Mathematics Millennium
Problems](https://www.claymath.org/millennium-problems/p-vs-np-problem))
is to determine if there are any problems in class <span
class="cclass">NP</span> that are not also in class <span
class="cclass">P</span>. Intuitively (at least to most people), one
might expect it is obvious that <span class="cclass">P</span> \\(
\subsetneq \\) <span class="cclass">NP</span> since checking an answer
seems like it should be easier than finding that answer, but it is not
know if this is the case. There is an important class of problems
known as <span class="cclass">NP-Complete</span> that can be
considered the set of the "hardest" problems in <span
class="cclass">NP</span>. There is a way to convert any problem in
class <span class="cclass">NP</span> into any one of these problems in
polynomial time, so if any problem in the class <span
class="cclass">NP-Complete</span> is shown to have a polynomial time solution, then we know all of them do and <span class="cclass">P</span> \\(
= \\) <span class="cclass">NP</span>. This class includes many important problems we will see in this class, and there are ways to define genome assembly, protien folding, phylogenetic tree construction, etc. as <span class="cclass">NP-Complete</span> problems. 

We can prove a problem is _hard_ by showing a reduction. If we already
know some problem \\( Z \\) is hard (say, \\( Z \in \\) <span
class="cclass">NP-Complete</span>), then we can show a new problem \\( A \\)
is at least as hard as \\( Z \\) by devising an algorithm that uses \\( A \\) to solve \\( X \\). Then, if we have a function \\( f_A(a) \\) that solves \\( A \\), we show how to solve \\( Z \\) by implementing \\( \ f_Z(z) = t_o(f_A(t_i(z))) \\) where \\( t_i \\) is a function that transforms the input to \\( Z \\) into a corresponding input to \\( A \\), and \\( t_o \\) is a function that trasforms the output of \\( f_A \\) that solves \\( A \\) into the corresponding output for \\( Z \\). If we can find \\( t_i \\) and \\( t_o \\) that make this work, and that run in polynomial time, we have a reduction proof that shows \\( A \\) is at least as hard (within polynomial time differences) to solve as \\( Z \\).


The division of problems into _tractable_ and _intractable_ is a gross
simplification. For large \\( k \\) and medium-size inputs, or for
small \\( k \\) and huge inputs, such problems are not actually easy
to solve, and their (money) cost might still be prohibitive. Problems
that are intractable can often be "solved" usefully in practice, even
though they cannot be "solved" in
theory. [Recall](/models#terminology) that solving a problem in theory
means finding an algorithm that finds an exact output for all possible
inputs within the required time. For many intractable problems where
the best known solution that works exactly for all inputs is a brute
force search requiring exponential time, we can find heuristics that
either find exact solutions quickly for most inputs, or that find good
approximate solutions for all inputs. Once we know a problem like
genome assembly is <span class="cclass">NP-Complete</span> it doesn't
mean we should give up on solving it &mdash; it just means we will
need to settle for heuristics and provide good approximations (but
don't guarantee finding the best solution) efficiently.

<div class="additionalreading">
<center><b>Additional Materials</b></center>

- Several chapters of the TCS book cover this material: [Chapter 12: _Efficient computation: An informal introduction_](https://introtcs.org/public/lec_10_efficient_alg.html), [Chapter 13: _Modeling running time_](https://introtcs.org/public/lec_11_running_time.html), [Chapter 14: _Polynomial-time reductions_](https://introtcs.org/public/lec_12_NP.html), [Chapter 15: _NP, NP completeness, and the Cook-Levin Theorem_](https://introtcs.org/public/lec_13_Cook_Levin.html), [Chapter 16: _What if P equals NP?_](https://introtcs.org/public/lec_14_PvsNP.html) [[PDF](https://files.boazbarak.org/introtcs/lec_14_PvsNP.pdf)].
- Videos from [cs3102](https://uvatoc.github.io/f20/week11/): [_"Difficulty" of Functions_](https://www.youtube.com/watch?v=PosxxVwgggI) (9:13), [_Tractable and Intractable Problems_](https://www.youtube.com/watch?v=SspCMbUF6Xs) (6:39), [_Introduction NP_](https://www.youtube.com/watch?v=BmXyo9acRWA) (14:01), [_The P=NP Question_](https://www.youtube.com/watch?v=FQCWOeS9GC4) (9:11), [_P=NP Recap_](https://www.youtube.com/watch?v=my-mxCwArk8) (4:44). (These are selected, see the [full week guide](https://uvatoc.github.io/f20/week11/) for a more complete video sequence.)



</div>





