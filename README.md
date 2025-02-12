# Little-o

In addition to the big-O, big- $\Omega$, and big- $\Theta$ notation that
we covered at the beginning of this class, a few other notations are sometimes
used in asymptotic analysis.  For example, "little- $o$" notation.

Prove (i.e.\ give a formal mathematical proof) that $f(n)\in o(g(n))$ implies
that $f(n)\in O(g(n))$.

Hint: The proof will be *very* short and *very* easy. You can start by
identifying the differences between the definitions of O and o.

I have started with the formal definition of $o$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$


## <span style="color: #f2cf4a; font-family: Babas; font-size: 2em;"> The Differences between Big-O and Little-O</span>

### The Definitions:

Little-o: $f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$

Big-O: $ T(n) \in  O(f(n))$ if $\exists \hspace{2mm}c >0 $  and $n_o$ such that $ T(n) \leq cf(n)$ $\forall \hspace{2mm }n \geq n_o$


###  The Conceptual Differences:

In essence all that's difference between Little o and Big O is that Little o is a less tight bound than Big O. This is because Little o can only be strictly larger than your $T(n)$ and not equal or larger to in the case of Big O. 

Another difference is that Little o applies for all positive constants and Big O only need one value to satify its conditions.


### The Proof:

Assume $T(n) \in o(f(n)),$ then we have that $T(n)\in o(f(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: T(n) < c f(n)$.

Then we can proceed with a purely logical argument to see why this must imply Big O. 
We know that the relation $\leq$ means:

$(a<b\hspace{1mm} or \hspace{1mm}a=b).$ 

And since we already have $T(n)< c(f(n))$ it must be also be that $T(n) \leq cf(n) \implies T(n) \in O(f(n))$. 

If this doesn't seem convincing look at the two number lines below

![Screenshot 2025-02-11 213422](https://github.com/user-attachments/assets/715ef020-6ba6-428d-afd4-5a9db66b57c8)
*Figure 1* Interval $[0,3)$

![Screenshot 2025-02-11 213504](https://github.com/user-attachments/assets/a2a85479-8fd9-42f3-8451-0697c33ac8cd)
*Figure 2* Interval $[0,3]$

Here we can use the figures above as an analogy for the logic. The first interval is strictly less than 3 and the second number line is less than or equal to containing all points less than 3 and the number 3. This is a good visualization becasue it essentially shows us that the first line is a subset of the second. Aka it is contained within the set that contains 3. Thus we can say if something is less than it is also less than or equal to.

Q.E.D

