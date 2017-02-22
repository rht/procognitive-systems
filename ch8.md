#CHAPTER EIGHT

##Libraries and Question-Answering Systems

Marill's (1963) REPORT, "Libraries and QuestionAnswering Systems," laid the groundwork for subsequent research on question-answering systems. The report consists of three parts:

1. Two Concepts of a Library
2. Question-Answering Systems
3. Semantic Nets: Informal Introduction

The first of the "two concepts of a library" is a schematization of a present-day library. In the schema, the library consists of the collection of documents, the "tag" system (index, catalogue, terms, etc.), and the retrieval system that makes use of the tags to retrieve desired documents. The contributions that technology can make within this first concept are acceleration of document handling, automation of the process of "tagging" (assignment of terms to documents), and improvement of the retrieval process. Marill argues that this first concept, instrumented on a modest scale, would yield unsatisfactory results, and that, carried to its logical hmit, it would be absurd.

The second concept of a library, according to Marill, is one in which the primary function is to provide not documents but information. The "system" of the second concept will be able to "read" and "comprehend" the documents themselves and not merely their tags. It will have a high capability for organizing the information internally.

It will be able to accept questions worded in natural English. If it has the requisite information available, it will answer the questions in natural English. Thus Marill advocates a very sophisticated procognitive system. He is concerned that people may believe the goal unreachable because it will be thought to require that inanimate mechanisms "think." Marill refers to the question-answering system called "Baseball" to forestall that misconception (Green et al., 1961).

In his discussion of question-answering systems, Marill defines the primary concepts: the corpus, the question, and the answer. The corpus consists of a set of quantificational schemata and their attendant predicate definitions, one definition for each predicate in the corpus. Thus Marill immediately seizes upon a predicate calculus as the formalism for representation of the information in the body of knowledge. There are two kinds of questions: questions satisfied by yes-no answers, and questions that require sentence answers.

Answers, therefore, are also of two types: yes-no answers and sentence answers. The answer to a yes-no question is "yes" if the question can be deduced from the corpus if there exists a deduction that has the sentences of the corpus as premises and the question (in statement form) as the last line. The answer is "no" if the negation of the question can be deduced from the corpus. There is no answer (or the answer is, "I don't know,") if neither the question nor its negation can be deduced from the corpus. A sentence qualifies as a sentence answer if the sentence can be deduced from the corpus and if the schema of the sentence is the same as the schema of the question when the question is in statement form. There can be only one yes-no answer, but there can be any number of sentence answers.

Marill's treatment of semantic nets is an extension and formalization of the discussion of relational networks given in Part I. Marill takes the view that the proper structural analysis of a sentence is given by the quantificational schema of that sentence, as understood in symbolic logic. To this, he adds the view that the meaning of a one-place predicate is identified, ultimately, with the setof objects of which the predicate is true, and the meaning of a two-place predicate is identified with the set of all ordered pairs of objects of which the predicate is true, and so forth. Finally, he adds the notion that the meaning of an object is identified with, first, the set of one-place predicates that are true of the object, and, second, the set of two-place predicates that are true of it and something else, and so forth.

The sets (of predicates and objects) with which meanings are identified are extremely large. The machine cannot be required to prove its "understanding" of a meaning by producing all the members of the sets. Marill maintains that it is enough for the machine to produce a convincingly large sample.

The usual representation of a quantificational schema has the form of a string of symbols. Marill views the semantic net as an alternative notation, equivalent to the string notation, but more promising for computer exploitation. To demonstrate the relation between semantic nets and string-form schemata, Marill starts with three simple statements in string notation and transmutes them, by degrees, into diagrams in which lines tie together the several instances of a variable.

The elements of a semantic net in Marill's exposition are the following.

1. Rectangles -- which represent the truth functions corresponding to logical operators and their arguments. Each rectangle has one terminal for each argument.
2. Diamonds -- which represent quantifiers. There are two types, corresponding to "some" and "all."
3. A triangle with point down -- which represents "sentence." This triangle contains an "S."
4. A circle -- which represents a predicate. The circle has as many terminals as there are places in the predicate.
5. A triangle with point up -- which represents an individual.

Marill gives six rules governing the combination of elements and the formation of semantic nets. The rules are:

1 Connecting a predicate to a sentence symbol forms a sentence.
2. Inserting a negation rectangle between the sentence symbol and the predicate negates the sentence.
3. To connect two sentences, divert their predicates to a two-place truth-function rectangle and connect it to a single sentence-symbol triangle.
4. To add a quantifier to a sentence, insert it in the line between the sentence symbol and its nearest neighbor.
5. To terminate an unterminated predicate, attach an individual object to the unused terminal, or connect that terminal to a quantifier that is already in the diagram of the sentence.
6. To merge two or more networks into one: (step 1) for each individual, overlay all the triangles that represent the individual, retaining all the lines that are attached to any of the triangles; (step 2) associate all the occurrences of the same predicate by connecting them with "association lines."

In "Semantic Nets: An Informal Introduction," Marill presents diagrams to illustrate the rules and to demonstrate the interpretation of moderately complex semantic nets. Marill's diagrams and discussion make it clear that the semantic net is formally equivalent to the conventional representation of a system of statements in predicate calculus. Marill believes that semantic nets afford a promising path into computer representation and processing of complex systems of relations.
