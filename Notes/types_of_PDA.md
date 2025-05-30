# Types of Pushdown Automata  
## 1) DPDA (Deterministic Pushdown Automata)   

A DPDA is similar as DFA, but it also considers the top symbol on the stack when making a transition. For each combination of state, input symbol, and stack symbol, there is only one possible action.

### Properties of Deterministic Pushdown Automata
DPDAs have several important properties that distinguish them from non-deterministic PDAs.

- **Uniqueness of Transitions** − Every transition is unique, meaning there are no duplicate actions for the same combination of state, input symbol, and stack symbol.
- **Predictability** − The behaviour of a DPDA is completely predictable, as there is only one possible action for every situation.
- **Ease of Implementation** − DPDAs are easier to implement than non-deterministic PDAs, as there is no need to handle multiple possible transitions.  

**Example of Deterministic Pushdown Automata**   

 `L = anb2n, n > 0:` This language consists of strings where the number of 'b's is twice the number of 'a's, and the number of 'a's is greater than 0.

So how to solve this using PDA?

- For every 'a', push it onto the stack.
- For every two 'b', pop 'a's from the stack.
- If the stack is empty at the end of the input, the string is accepted.   
[PDA of this example](PDA_solved_examples.pdf)
  
### Applications of Deterministic Pushdown Automata
DPDAs have applications in various areas of computer science, including.

- **Formal Language Theory** − DPDAs are used to define and recognize a class of languages known as deterministic context-free languages.
- **Compilers and Interpreters** − DPDAs are used in parsing, the process of converting source code into a form that can be understood by a computer.
- **Natural Language Processing** − DPDAs are used in analyzing and understanding human language.

<br> 

## 2) NPDA (Nondeterministic pushdown Finite Automata)   
In some cases, a machine must face a choice to select the next state; it can either move to one state or another. In a non-deterministic pushdown automata (NPDA), this machine has the freedom to explore all possible paths. It can simultaneously follow multiple paths based on the input and the stack's content. This means that the machine can accept a string if even one of its possible paths leads to an accepting state.   


### How Does an NPDA Work?
The following steps highlight how a non-deterministic pushdown automaton works

- **Initialization** − The NPDA starts in the initial state q0 with the stack containing only the initial stack symbol Z0.
- **Reading input** − The NPDA reads the input symbol one at a time.
- **Transition** − For each input symbol a and the current stack top X, the transition function δ is consulted. It provides a set of possible transitions. The NPDA can choose any of these transitions. This choice is non-deterministic.
- **Stack manipulation** − The NPDA modifies the stack according to the chosen transition. It can push symbols onto the stack, pop symbols from the stack, or leave the stack unchanged.
- **State change** − The NPDA moves to the new state q' specified by the chosen transition.
- **Acceptance** − The NPDA accepts the input string if it reaches a final state after reading the entire input string.

**Example of Nondeterministic Pushdown Automata**  
Construct a PDA that accepts Even Palindromes of the form  
        `L = {ww^R | w = (a+b)*}`  

[PDA of this example](PDA_solved_examples.pdf)   
