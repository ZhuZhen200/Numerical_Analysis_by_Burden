### 20221202
#### Interpolation
Key:$p_k(x) = \sum_{k=0}^n a_k{\phi}_k(x)$ 

##### Different basis functions:

1. Monomial basis: $x^k$
2. Lagrange basis: $l_k(x)=\Pi_{j=0,j{\neq}k}^n \frac{(x-x_j)}{(x_k-x_j)}$
3. Newton basis: $\pi_k(x)=\Pi_{j=0}^{k-1}(x-x_j)$

##### Solving procedure:
1. Use x- and y-coordinates of data to create the system of linear equations: 
$$
        p_k(x_i) = \sum_{k=0}^n a_k{\phi}_k(x_i)=y_i
$$
2. Rewite it in matrix form: Aa=y
3. Solve the matrix
4. Forward subtitution (For Newton basis, divided difference is more stable than forward subtitution)

##### Complexity:
1. Monomial -> $O(n^3)$
2. Lagrange -> trivial
3. Neewton -> $O(n^2)$
