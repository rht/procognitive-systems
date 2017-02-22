#CHAPTER FIVE

##Syntactic Analysis of Natural Language by Computer

The relevance of automated syntactic analysis to library procognitive systems lies in machine processing, and in eventual machine "understanding," of naturallanguage text. There is no thought that syntactic analysis alone whether by man or machine is sufficient to provide a useful approximation to understanding. On the other hand, there is no doubt that appreciation of the syntactic structure of natural-language text is a part, and an important part, of the over-all problem. Accordingly, Bobrow (1963) surveyed the work that has been done, and is being done, toward automation of syntactic analysis of English.

The efforts to automate syntactic analysis have been, essentially, efforts to implement various theories of grammar through the preparation of computer programs that operate on natural-language text in the form of strings of encoded alphanumeric characters. The output of a successful syntactic-analysis program is one or more sets of assignments of the words of a sentence to grammatical categories ("parts of speech") plus, for each set of assignments, a representation of the grammatical structure of the sentence.

The grammars that have been used as bases for syntactic-analysis programs include dependency grammars, phrase-structure grammars with continuous and with discontinuous constituents, predictive grammars, stringtransformation grammars, and phrase-structure transformational grammars. The main characteristics of, and differences among, these grammars are set forth in Bobrow's report. Although it is too early to say with assurance which of them is (or are) best for our purposes much expert intuition favors the phrase-structure, transformational approach.

Many of the programs that have been successful in making syntactic analyses have depended upon a distinction between "function words" and "content words." The distinction is a simple and familiar one. Function words are words such as "and," "or," "to," "from," "a," "an," "the," "neither," "nor," "if," and "whether." Content words are words such as "grammar," "equivalent," "structural," "diagram," "sentence," "minimum," "weekly," "accept," and "develop." There are, of course, many more types of content words than of function words. It is therefore reasonable to store in a computer memory very detailed descriptions of the functions, characteristics, idiomatic uses, and so forth, of the function words. The successful analytic programs have, in addition, employed dictionaries containing, for each content word, the grammatical categories into which it is normally expected to fall.

It is the intention here, not to give a complete summary of Bobrow's report, but rather to relate the idea of syntactic analysis by computer to the over-all picture set forth in Part I, Perhaps the best way to do that is to show in diagrammatic form some of the analyses that are described in detail by Bobrow.

The notion of "dependency" gives a direction and a hierarchical structure to syntactic relations. Adjectives depend on nouns, nouns depend on verbs and prepositions, adverbs and auxiliary verbs depend on main verbs, prepositions depend on the words modified by their phrases, and so forth. The system of dependency can be represented diagrammatically in the way illustrated for the sentences, "The man treats the boy and the girl in the park,"

TODO: render the syntax tree with a caption "Dependency Analysis"

and "The man at the door turned the light out."


TODO: render the syntax tree with a caption "Dependency Analysis"

This second sentence will be used to illustrate other grammars also, in order to display similarities and differences.

Computer programs capable of implementing dependency analysis have been developed or described by Hays (1962) of the RAND Corporation, by Kelly \* (\* footnote: H. Kelly, Personal communication, September 1963.) of the RAND Corporation, by Gross (1962) of M.I.T., by Klein and Simmons (1963) of the System Development Corporation, and by several Russian workers, including Moloshnava (I960) and Andreyev (1962).

In a phrase-structure analysis that assumes continuous, immediate constituents, \dagger (\dagger footnote: Immediate constituents are parts that are separated by the first step of an analysis, i.e., that are encountered immediately; they are to be contrasted with ultimate constituents. Continuous constituents are parts whose subparts are contiguous; continuous constituents are to be contrasted with discontinuous constituents.) the diagrammatic representation is again treelike, but the nodes of the branching structure are, at all levels except the lowest, syntactic or gram- matical categories. At the lowest level, the actual words of the sentence appear. An immediate-constituent analysis of "The man ate the apple" is shown in the diagram.

TODO: render the syntax tree with a caption "Immediate-Constituent Analysis"

The analysis starts at the bottom of the diagram with the string of words and proceeds to discover a superstructure consistent with their grammatical class memberships. However, the analysis may involve trial-and-error differentiation downward from assumed categories to strings of words.

The analysis substitutes for "Sentence" the two category names, "Noun Phrase" and "Verb Phrase." It then substitutes for "Noun Phrase" the category names "Definite Article" (or, since there is only one definite article in English, the symbol "T") and "Noun." For "Verb Phrase" it substitutes "Verb" and "Noun Phrase." It is then in a position to substitute actual words for three of the category names. "Noun Phrase," however, has to be passed through one more stage of analysis before the substitution of actual words can be made. The result of the analysis the diagram displays the roles of the individual words of the sentence and, in addition, shows how the several roles are interrelated.

The next diagram illustrates immediate-constituent analysis of "The man at the door turned the light out."

TODO: render the syntax tree with a caption "Immediate-Constituent Analysis, read the minus sign (not hypen) as minus"

In the foregoing example, the analysis proceeded in a succession of binary branchings. An alternative formulation makes use of multiple branching to produce coordinate structures with fewer levels. Bobrow compares binary structure and coordinate structure in the phrase, "the old black heavy stone."

TODO: render the syntax tree with a caption "Immediate-Constituent Analysis"

Computer programs capable of making immediate-constituent analyses have been developed or described by Robinson (1962) of the RAND Corporation, Cocke \* (\* footnote: John Cocke, Personal communication, September 1963.) of the International Business Machines Corporation, and Klein (1963) of the System Development Corporation.

Kuno and Oettinger of Harvard (1963) have developed extensively the technique of predictive analysis advocated by Rhodes (1961) of the National Bureau of Standards. Predictive analysis takes advantage of the fact that, once he has heard the beginning of a sentence, the listener can rule out many of the myriad syntactic patterns into which sentences are, a priori, capable of falling. Predictive analyses keep track only of the alternative interpretations that are consistent with the part of the sentence that has already been analyzed. At the very beginning, there are usually but few alternatives, for then the interpretations are not differentiated. In the mid-course of an analysis, there may be many possible ways in which the sentence can go. At the end, however, the analysis should converge upon one pattern of grammatical categories, or, at any rate, upon a set of patterns among which a choice can be made on the basis of semantic interpretation of the sentence itself and of its context. (Unfortunately for the prospects of machine "understanding," "context" must embrace both linguistic context and circumstantial or nonlinguistic context.) The KunoOettinger programs determine all the alternatives. Related programs developed by Lindsay (1963) of the University of Texas find only one syntactic pattern but provide diagnostic information on the basis of which it is possible to clear up misinterpretation through "post-editing."

A minor problem for machine analysis is introduced by the fact that two words may together fill a grammatical category without being contiguous in text. This problem is not faced squarely by immediate-constituent grammars. In discontinuous-constituent grammars, however, the problem is recognized, and a special linkage is introduced to connect the separated parts. The diagram illustrates an analysis of "He called her up."

TODO: render the syntax tree with a caption "Discontinuous-Constituent Analysis"

The linkage from "Verb" to "Particle" connects "up" to "called," from which it has been separated by "her." The diagram shows a discontinuous-constituent analysis of the standard sentence, "The man at the door turned the light out."

TODO: render the syntax tree with a caption "Discontinuous-Constituent Analysis"

For the purposes of library procognitive systems, the most important problem in this subject area may well be one raised by Chomsky (1956, 1957). Chomsky was concerned that two expressions of the same idea, such as "The man drives the car" and "The car is driven by the man" do not have similar phrase structures and do not yield similar diagrams when analyzed in the ways we have been discussing. Chomsky handled this problem by setting up "transformation rules" that transform one sentence into another, or combine n sentences into one, or subdivide one sentence into n sentences. For example, one transformation takes a sentence from active voice to passive voice. Another transformation combines two singleclause sentences into a compound sentence. With transformation rules, one can build up complex syntactic structures from simple ones or analyze complex syntactic structures into simple ones. Bobrow gives an example in which the simple statements

1. X's are the airfields.
2. The airfields are in Ohio.
3. The airfields have runways.
4. The runways are long.
5. Two miles is long.

are derived from the question, "What are the airfields in Ohio having runways longer than two miles?" Analysis and synthesis based on such transformations will surely be important for machine-aided organization of the body of knowledge.

The transformational-grammar approach handles the discontinuous-constituent problem neatly. A transformation changes "turned the light out" into "turned out the light." As the diagram shows, the analysis then proceeds without any diffilculty.

TODO: render the syntax tree with a captin "Intermediate Stage in Chomsky's Transformational Derivation"

Walker and Bartlett (1962) of the Mitre Corporation are developing a parsing program based on a transformational grammar.

Harris (1962) and his associates at the University of Pennsylvania have developed a method of syntactic analysis that is intermediate between constituent analysis and transformational analysis. Although their method does not lend itself to representation by a tree diagram, a rough idea of its approach is conveyed by relating some of its terms to our standard sentence. In the sentence, the "string center" is ". . . man . . . turned out . . . light." One "the" is the "left adjunct" of "man," and the other is the "left adjunct" of "light." "At the door" is the "right adjunct" of "man." This "string-transformational grammar" has been implemented in the form of computer programs. The "Baseball" program developed by Green and associates (1961) at the Lincoln Laboratory -- a program capable of answering questions about the outcomes of the baseball games played in the major leagues during one season -- has a methodological kinship to the Pennsylvania work.

From Bobrow's survey, it is clear that automation of syntactic analysis is possible. Indeed, there are several operating syntactic-analysis programs. It is equally clear, however, that syntactic analysis is only a part -- and perhaps, relatively, only a small part -- of the over-all problem. The fact is that even the best analysis programs (excepting Lindsay's, which arbitrarily limits itself to a single syntactic pattern) produce discouragingly many alternative patterns. Selection among the alternatives has to be made on nonsyntactic grounds, and there has not been much progress toward automation of that selection. Furthermore, it is evident that one is a very long way from understanding what is being said when all he knows is the pattern or structure of syntactic categories into which the words of the message fit.

The question was raised in Part I, whether it is desirable, in formulating the basic concepts of this field, to separate syntactic and semantic factors into the two insulated bins of a rigid dichotomy, or whether, as subtler and subtler distinctions are made in the process now called syntactic analysis, that process will start to become semantic as well as syntactic. Although we are not in a position to decide, one way or the other, on that question, we have an intuitive feeling that the latter is more promising as a line of development. We should, in this connection, refer to work that we regard as extremely promising, work being carried out by F. B. Thompson and his colleagues (Thompson, 1963).
