# AI-Theorem-Prover
Resoulution Refutation on FOL (First Order Predicate Logic)

# Input:  
"Number of task to solve"  
"n:Number of clauses in base set(KB) m:Number of clauses in goal set(G)"  
"KB Clauses (Line n+1)  
G Clauses (Line m+n+1)"  

# Example input:  
1  
3 1  
p(A,f(t))  
q(z),~p(z,f(B))  
~q(y),r(y)  
~r(A)  
  
Represents the universe :  
KB = p(A,f(t)) AND (q(z) OR ~p(z,f(B))) AND (~q(y) OR r(y))  
G = ~r(A)  

# Output:  
"Resolution Steps"  
"Is it Derivable : YES or NO"  

# Example Output:  
p(A,f(t))$q(z),~p(z,f(B))$q(A)  
q(A)$~q(y),r(y)$r(A)  
r(A)$~r(A)$empty_clause  
YES  
  
Each clause are separated with $ sign. First two clause are resolved to the third one in each resolution step.  
Shows the resoulution steps in each row.  
Prover returns the theorem is derivable or not in last line of the output.txt.  
