---
layout: post
title: "Draft"
---
> Let $G$ be a group. A matrix representation of $G$ of degree $d$ is a function $X:G\to GL_d(\mathbb{C})$ such that $X$ is a group homomorphism. If the representation is injective, we say that it is faithful.

Examples:
- Let $d=1$. The map $X: G\to GL_1(\mathbb{C})$ such that $X(g)=(1)$ for all $g\in G$ is a group homomorphism and so is a matrix representation of $G$ of degree 1. This is known as the trivial representation.
	
- Let $d=1$ and $G=\{e,g,g^2,g^3\}$. The map $X: G\to GL_1(\mathbb{C})$ such that 
  $$X(e)=(1), X(g)=(i), X(g^2)=(-1), X(g^3)=(-i)$$
	is a group homomorphism and so is a matrix representation of $G$ of degree 1.
	
- Let $d=1$ and $G=S_n$. The map $X: G\to GL_1(\mathbb{C})$ such that 
	\[X(\sigma)=(sgn(\sigma))\]
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
