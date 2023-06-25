# # # Type (1) - D # # #
![SS 2023-05-27 at 19 03 39](https://github.com/space-hippie0/matlab/assets/118982314/9503abbd-3675-492c-a707-7d375297425b)

% Initialize a 12x12 matrix A with zeros
```
A = zeros(12); 
```
% Iterate over rows and columns of A
```
for i = 1:12
    for j = 1:12
        % Check the relationship between i and j
        if i == j
            A(i, j) = 2 * i;  				% Set diagonal elements
        elseif i < j
            A(i, j) = (-2) / j;  			% Set elements below the diagonal
        elseif i > j
            A(i, j) = 2 / j;  				% Set elements above the diagonal
        end
    end
end
```
% Compute the eigenvalues of matrix A
```
aval = eigs(A); 
```
% Find the maximum absolute eigenvalue
```
max_eigenvalue = max(abs(aval)) 	
```




# # # Type (2) - B # # #
![SS 2023-05-27 at 19 17 20](https://github.com/space-hippie0/matlab/assets/118982314/6617e49c-f94a-4064-8f50-8a0c7aac100f)

% Initialize Matrix A
```
A=[2,3,4; 3,4,6; 1,0,3];
```
% Compute the product of A transpose and A
```
B=A'*A
```


# # # Type (3) - C # # #
![SS 2023-05-27 at 19 21 09](https://github.com/space-hippie0/matlab/assets/118982314/6012e64d-70ec-4993-87a6-2f4895c3103c)
% Generate vector x with 10 equally spaced values from -1 to 1
```
x = linspace(-1, 1, 10);
```
% Construct Vandermonde matrix A using vector x
```
A = vander(x);  
```

% Initialize vector z with ones
```
z = ones(10, 1);  
```
% Normalize vector w
```
w = z / norm(z);  
```

% Perform iterations
```
for i = 1:24
    z = A * w;  		% Multiply matrix A with vector w
    lambda(i + 1) = w' * z;  	% Compute scalar product of w and z
    w = z / norm(z);  		% Normalize vector z and update w
end
```
% Display the third element of vector w
```
w(3)  
```





# # # Type (4) - B # # #
![SS 2023-05-27 at 20 18 30](https://github.com/space-hippie0/matlab/assets/118982314/527c9eb2-a94d-4cfb-b0b6-392a9050c17d)
% Generate the Hilbert matrix of order 18
```
A = hilb(18);
```
% Apply QR factorization to matrix A

% Update A by multiplying the orthogonal and upper triangular matrices
```
for i = 1:6
    [Q, R] = qr(A);   						
     A = R * Q;        
end
```
% maximum absolute difference between the diagonal elements and its eigenvalues.

% This difference can be an indicator of how accurately the diagonal elements of A represent its eigenvalues.
```
eigen_diff = max(abs(diag(A) - eig(A))) 	
```




# # # Type (5) - A # # #
![sorulacak](https://github.com/space-hippie0/matlab/assets/118982314/bf30c24d-2c52-4d51-89eb-94edf869ea77)
% Create the tridiagonal matrix A
```
A = 6*eye(18) + 3*diag(ones(17,1),1) + (-3)*diag(ones(17,1),-1);
```
% Build the vector b with equally spaced values in [0,1]
```
b = linspace(0,1,n)';
```
% Perform SVD decomposition of A
```
[U, S, V] = svd(A);
```
% Solve the linear system Ax = b
```
x = V * inv(S) * U' * b;
```
% Calculate the solution y of the linear system with coefficient matrix S
```
y = inv(S) * U' * b;
```
% Calculate the quantity ||x||_2 + ||y||_2
```
norm_x = norm(x, 2);
norm_y = norm(y, 2);
result = norm_x + norm_y
```



# # # Type (6) - B # # #
![SS 2023-05-27 at 19 33 13](https://github.com/space-hippie0/matlab/assets/118982314/a4f4d228-2815-4c01-819a-197c10c49f00)
% Set the size of the matrix A
```
n = 6;
```
% Generate the Hilbert matrix A
```
A = hilb(n);
```
% Set the value of parameter p
```
p = 0.2;
```
% Initialize vectors and variables
```
z = ones(n, 1);
w = z / norm(z);
lambda(1) = p;
```
% Perform LU factorization with partial pivoting
```
[L, U, P] = lu(A - p * eye(n));
```
% Perform power iteration for 4 iterations
```
for i = 1:4
    					% Solve the lower triangular system Ly = Pw
    y = L \ (P * w);
    					% Solve the upper triangular system Uz = y
    z = U \ y;
    					% Update the eigenvalue estimate
    lambda(i + 1) = p + 1 / (w' * z);
    					% Normalize the eigenvector estimate
    w = z / norm(z);
end
```

% Compute the true eigenvalue using eigs function
```
aval = eigs(A, 1, p);
```

% Calculate the relative error
```
err = abs(lambda(i + 1) - aval) / abs(aval);
```

% Display the error
```
err
```


# # # Type (7) - C # # #
![SS 2023-05-27 at 19 36 13](https://github.com/space-hippie0/matlab/assets/118982314/cba55078-e508-48a9-92d0-c14718bf4fcc)
% Generate an 8x8 Pascal matrix A
```
A = pascal(8);
```
% Perform the singular value decomposition (SVD) of A
```
[U, S, V] = svd(A);
```
_________________________________________________
% U: Orthogonal matrix of left singular vectors |
% S: Diagonal matrix of singular values	        |
% V: Orthogonal matrix of right singular vectors|
________________________________________________|

% Reconstruct a lower-rank approximation of A using 5 singular values and vectors
```
k = 5;
```
% An: Approximation of matrix A using the most significant singular values and vectors
```
An = U(:, 1:k) * S(1:k, 1:k) * V(:, 1:k)';
```
% error: Frobenius norm, which measures the difference between A and An
```
error = norm(A - An);
```
% Display the result
```
error
```




# # # Type (8) - E # # #
![SS 2023-05-27 at 19 45 46](https://github.com/space-hippie0/matlab/assets/118982314/43d5b4fa-2a55-49bf-a32e-39661a7cec25)
% Generate a vector x with 10 equally spaced values between 0 and 1
```
x = linspace(0, 1, 10);
```
% A: Vandermonde matrix with powers of x as columns
```
A = vander(x);
```
% Perform the singular value decomposition (SVD) of A
```
[U, S, V] = svd(A);
```
_________________________________________________
% U: Orthogonal matrix of left singular vectors |
% S: Diagonal matrix of singular values	        |
% V: Orthogonal matrix of right singular vectors|
________________________________________________|

% Initialize a matrix An with zeros
```
An = zeros(10, 10);
```
% Reconstruct An using the first 7 singular values and corresponding vectors
```
k = 7; 			 % Number of singular values/vectors to consider
for i = 1:k
    An = An + S(i, i) * U(:, i) * V(:, i)';
			 % An: Reconstructed matrix using the selected singular values and vectors
end
```
% normAn: Infinity norm, which measures the maximum absolute row sum of An
```
normAn = norm(An, inf);
```

% Display the result
```
normAn
```


# # # Type (9) - D # # #
![SS 2023-05-27 at 19 49 02](https://github.com/space-hippie0/matlab/assets/118982314/f597afc3-7a16-422d-bcce-586e68b18d41)
% Generate a 12x12 Hilbert matrix A
```
A = hilb(12);
```

% Perform QR factorization of A for 8 iterations
```
for i = 1:8
    % QR factorization of A
    [Q, R] = qr(A);
    
    % Update A by multiplying R and Q
    A = R * Q;
end
```

% Retrieve and display the value at the (3, 3) position of A
```
value = A(3, 3);
value
```


# # # Type (10) - E # # #
![SS 2023-05-27 at 20 00 42](https://github.com/space-hippie0/matlab/assets/118982314/8bbcc088-1c87-48d9-b35d-59e037f070a6)
% Set the order of the matrix
```
n = 6;
```

% Create a Pascal matrix of order n
```
A = pascal(n);
```

% Set the value of p
```
p = 2;
```

% Initialize the vector z with all ones
```
z = ones(n, 1);
```

% Perform iterations to compute lambda
```
for i = 1:4
    % Normalize z
    w = z / norm(z);
    
    % Solve the linear system (A-p*I)z = w
    z = (A - p * eye(n)) \ w;
end
```

% Compute the value of lambda
```
lambda = p + 1 / (w' * z);
```

% Compute the approximate eigenvalue using the eigs function
```
aval = eigs(A, 1, p);
```

% Compute the error between aval and lambda
```
err = abs(aval - lambda);
```
