---
layout: post
title: "Representation of Symmetric Groups: Basics"
---
Groups are amazing algebraic structures, with a whole field of study dedicated to it despite it having only 3 basic axioms to its construction, and it can seen in other parts of maths as well like in algebraic topology and number theory. However, this makes it hard to study some of the properties it might have; we might be having too little to work with. In order to study groups further, we would want to maybe look at them in a more richer environment; this is what homomorphisms allow us to do. This gives us what is known as Representation Theory: the study of representations of structures, such as groups, using other structures, such as vector spaces or algebras, that have more to work it. In fact, one of the mmost fundamental groups that we are interested in studying is the symmetric group $S_n$, as it pops up almost every in both pure and applied mathematics. Here I introduce the basic notions of representation theory with respect to the symmetric group, to show how interesting and beautiful it is. The reference text for this topic is Sagan's Symmetric Group if you would want to dive a bit further.

# Basic Definitions
We first introduce the notion of what a representation is, via something familiar to most undergrad maths: linear algebra.
> Let $G$ be a group. A **matrix representation** of $G$ of degree $d$ is a function $X:G\to GL_d(\mathbb{C})$ such that $X$ is a group homomorphism. If the representation is injective, we say that it is faithful.

This essentially tells us that the group has an action on $\mathbb{C}^d$, and the matrices tell us how each element from the group acts on it, i.e. they represent the group elements.

Examples:
- Let $d=1$. The map $X: G\to GL_1(\mathbb{C})$ such that $X(g)=(1)$ for all $g\in G$ is a group homomorphism and so is a matrix representation of $G$ of degree 1. This is known as the trivial representation.
	
- Let $d=1$ and $G=\{e,g,g^2,g^3\}$. The map $X: G\to GL_1(\mathbb{C})$ such that 
  $$X(e)=(1), X(g)=(i), X(g^2)=(-1), X(g^3)=(-i)$$
	is a group homomorphism and so is a matrix representation of $G$ of degree 1.
	
- Let $d=1$ and $G=S_n$. The map $X: G\to GL_1(\mathbb{C})$ such that 
	$$X(\sigma)=(sgn(\sigma))$$
	is a group homomorphism and so is a matrix representation of $G$ of degree 1.
	
- Let $d=2$ and $G=S_2$. The map $X: G\to GL_2(\mathbb{C})$ such that 
	$$X(e)=\begin{pmatrix}
1 & 0 \\\ 
0 & 1 
\end{pmatrix}, X((1\quad 2))=\begin{pmatrix}
0 & 1 \\\ 
1 & 0
\end{pmatrix}$$
	is a group homomorphism and so is a matrix representation of $G$ of degree 2.

In general, when $G=S_n$, we can talk about the defining representation of $S_n$ as follows:
Let $X:S_n\to GL_n(\mathbb{C})$ be the map $X(\sigma)=(a_{ij})$, where
$$a_{ij}=\begin{cases}
1 & \text{ if } \sigma(j)=i\\\
0 & \text{ otherwise } \\\
\end{cases}$$
Then $X$ is a matrix representation of $S_n$ of degree $n$, which is the defining representation of $S_n$.

Examples:
- The defining representation of $(1\quad 3\quad 2)\in S_3$ is $\begin{pmatrix}
0 & 1 & 0 \\ 
0 & 0 & 1 \\ 
1 & 0 & 0
\end{pmatrix}$
	
- The defining representation of $(1\quad 2\quad 3)\in S_4$ is $\begin{pmatrix}
0 & 0 & 1 & 0\\ 
1 & 0 & 0 & 0\\ 
0 & 1 & 0 & 0\\
0 & 0 & 0 & 1
\end{pmatrix}$

Since matrices are equivalent to linear transformations, we can also consider representations in terms of linear transformations.


> Let $G$ be a group and $V$ be a vector space over $\mathbb{C}$. V is called a **$G$-module** if there exists a group homomorphism
	$$\phi: G\to GL(V)$$
	Where $GL(V)$ is the group of invertible linear transformations from $V$ to itself.

A $G$-module is essentially a vector space with a group action defined on it. Note that if $\dim V= d$, then $GL(V)\cong GL_d(\mathbb{C})$. So if $V$ is a $G$-module, it induces a matrix representation of $G$ of degree $\dim V$. 

Examples:
- Let $V=\mathbb{C}^3, G=S_3$. Then $V$ is an $S_3$-module by the defining representation on $S_3$.
	
- Let $V=\mathbb{C}, G=\{e,g,g^2,g^3\}$. Then $V$ is a $G$-module by the map
	\[e\mapsto (x\mapsto x), g\mapsto (x\mapsto ix), g^2\mapsto(x\mapsto -x), g^3\mapsto(x\mapsto -ix)\]
	which is a group homomorphism.
