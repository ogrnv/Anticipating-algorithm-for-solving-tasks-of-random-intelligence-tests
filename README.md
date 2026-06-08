# Anticipating-algorithm-for-solving-tasks-of-random-intelligence-tests


When a LLM solves a complex task of random intelligence tests it as a rule results in infinite loops or infinite wandering. 

In the anticipating algorithm AI should first create a future state of the test board with chips. And then it should come to the state. 
The determination of the future state eliminates the loops or wanderings.

Anticipating algorithm recalls the fragment: "A spider conducts operations that resemble those of a weaver, and a bee puts to shame many an architect in the construction of her cells. But what distinguishes the worst architect from the best of bees is this, that the architect raises his structure in imagination before he erects it in reality." from Karl Marx's Capital. 

This is a example of prompt for the algorithm:

Your code should first rearrange the chips of a given TB to obtain a different optimal TB in which formation of a straight horizontal or vertical or diagonal line of five or more chips with the same marking is completed. 
The code should then make an array of optimal moves i.e. array from-to addresses leading from the given TB to the optimal TB.
The code should then issue as TTSR results x0, y00, x1, y01 from the array, ignoring new input TBs until the step completes.
Optimal means "in accordance with the goal of the test round".
