# CKY Probabilistic Parser

This program generates the most likely parse tree for a sentence given a Context-Free Grammar and a lexicon using the CKY algorithm.

**usage: python cky.py \<grammar-rules> <text_for_parsing>**

*CKY Algorithm*: In computer science, the Cocke–Younger–Kasami algorithm (alternatively called CYK, or CKY) is a parsing algorithm for context-free grammars, named after its inventors, 
John Cocke, Daniel Younger and Tadao Kasami. It employs bottom-up parsing and dynamic programming.

*Parse tree* : a tree that represents the syntactic structure of a string according to some context-free grammar.

*Context-Free Grammar* : 

A context-free grammar (CFG) consisting of a finite set of grammar rules is a quadruple (N, T, P, S) where:

**N** is a set of non-terminal symbols.

**T** is a set of terminals where N ∩ T = NULL.

**P** is a set of rules, P: N → (N ∪ T)*, i.e., the left-hand side of the production rule P does have any right context or left context.

**S** is the start symbol.

Why do we care? 

Probabilistic parsing is specially important in the case of sentence ambiguity. For example, when presented with the sentence "I shot an elephant in my pajamas", what is the author/speaker trying to say...

1. He was wearing his pajamas when he shot an elephant
2. He shot an elephant that was wearing his pajamas

As ridiculous as this example may seem, it is important for computers to be able to derive the appropriate meaning from the given context. This is why probabilistic parsers like CKY are important. 
