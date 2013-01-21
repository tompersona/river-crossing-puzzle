river-crossing-puzzle
=====================

A while ago, a Flash puzzle was doing the rounds. The problem is a variation on the classic river crossing puzzle. In this version, there are 8 people: a mother and father, 2 daughters, 2 sons, a policeman and a thief.

The following rules apply:

- only 2 people can be on the boat at a time

- the father cannot stay with any of the daughters without their mother's presence

- the mother cannot stay with any of the sons without their father's presence

- the thief cannot stay with any family member if the policeman is not there

- only the father, the mother and the policeman know how to operate the boat


I decided to tackle the problem using Tony Hoare's _Communicating Sequential Processes_ (CSP). As the name suggests, the language is designed to model interactions in concurrent systems. Once modelled, properties of the system (such as deadlock and livelock) can be checked using a tool called _Failures-Divergence Refinement_ (FDR). This involves taking two processes modelled in CSP and determining whether one refines the other.

For my purposes, I wished to model the puzzle described above in CSP and, in order to find a valid solution, have FDR refute an assertion that an incomplete solution refined the puzzle.

The full model with comments can be found in river-crossing.csp followed by (spoiler alert!) a solution.