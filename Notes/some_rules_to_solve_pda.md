### 1) Language : a^nb^n+1 , where n>0  

**PDA Construction Strategy**   

- For each a, push A onto the stack.
- For each b, pop one A from the stack.
- After popping all As, read one extra b.
- Accept when input is done and stack is empty

### 2) Language: a^n+2b^n, where n>=0 
**PDA Construction Strategy**   
- First read 2 extra as (don’t push them to stack — just consume).
- Then, for each remaining a, push one symbol (A) onto the stack.
- For each b, pop one A.
- If input is finished and stack is empty → accept.