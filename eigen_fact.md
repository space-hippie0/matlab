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
            A(i, j) = 2 * i;  				% Set diagonal elements of A as 2 times i
        elseif i < j
            A(i, j) = (-2) / j;  				% Set elements below the diagonal as -2 divided by j
        elseif i > j
            A(i, j) = 2 / j;  				% Set elements above the diagonal as 2 divided by j
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
max_eigenvalue = max(abs(aval));  	
```
% Display the result
```
disp("Maximum Absolute Eigenvalue: " + max_eigenvalue);
```



Type (2) - B
![SS 2023-05-27 at 19 17 20](https://github.com/space-hippie0/matlab/assets/118982314/6617e49c-f94a-4064-8f50-8a0c7aac100f)
A=[2,3,4; 3,4,6; 1,0,3];
B=A'*A					% Compute the product of A transpose and A


Type (3) - C
![SS 2023-05-27 at 19 21 09](https://github.com/space-hippie0/matlab/assets/118982314/6012e64d-70ec-4993-87a6-2f4895c3103c)
x=linspace(-1,1,10);
A=vander(x);

z=ones(10,1);
w=z/norm(z);

for i=1:24
    z=A*w;
    lambda(i+1)=w'*z;
    w=z/norm(z);
end
w(3)



Type (4) - B
![SS 2023-05-27 at 20 18 30](https://github.com/space-hippie0/matlab/assets/118982314/527c9eb2-a94d-4cfb-b0b6-392a9050c17d)

A = hilb(18);          						% Generate the Hilbert matrix of order 18
for i = 1:6
    [Q, R] = qr(A);   						% Apply QR factorization to matrix A
     A = R * Q;         						% Update A by multiplying the orthogonal and upper triangular matrices
end

eigen_diff = max(abs(diag(A) - eig(A))); 	

% Display the result
disp("Max Absolute Difference: " + eigen_diff);




Type (5) - A
![sorulacak](https://github.com/space-hippie0/matlab/assets/118982314/bf30c24d-2c52-4d51-89eb-94edf869ea77)
% Define the parameters
n = 18;             		% Order of the matrix A
diag_val = 6;       		% Value of the diagonal elements
upper_diag_val = 3; 	% Value of the upper diagonal elements
lower_diag_val = -3;	% Value of the lower diagonal elements

% Create the tridiagonal matrix A
diagonal = diag(diag_val*ones(n,1));
upper_diagonal = diag(upper_diag_val*ones(n-1,1),1);
lower_diagonal = diag(lower_diag_val*ones(n-1,1),-1);
A = diagonal + upper_diagonal + lower_diagonal;

% Build the vector b with equally spaced values in [0,1]
b = linspace(0,1,n)';

% Perform SVD decomposition of A
[U, S, V] = svd(A);

% Solve the linear system Ax = b
x = V * inv(S) * U' * b;

% Calculate the solution y of the linear system with coefficient matrix S
y = inv(S) * U' * b;

% Calculate the quantity ||x||_2 + ||y||_2
norm_x = norm(x, 2);
norm_y = norm(y, 2);
result = norm_x + norm_y;

% Display the result
disp(['The quantity ||x||_2 + ||y||_2 is approximately: ' num2str(result)]);



Type (6) - B
![SS 2023-05-27 at 19 33 13](https://github.com/space-hippie0/matlab/assets/118982314/a4f4d228-2815-4c01-819a-197c10c49f00)
% Set the size of the matrix A
n = 6;

% Generate the Hilbert matrix A
A = hilb(n);

% Set the value of parameter p
p = 0.2;

								% Initialize vectors and variables
z = ones(n, 1);
w = z / norm(z);
lambda(1) = p;

								% Perform LU factorization with partial pivoting
[L, U, P] = lu(A - p * eye(n));

% Perform power iteration for 4 iterations
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

% Compute the true eigenvalue using eigs function
aval = eigs(A, 1, p);

% Calculate the relative error
err = abs(lambda(i + 1) - aval) / abs(aval);

% Display the error
disp(['Relative error: ' num2str(err)]);


Type (7) - C
![SS 2023-05-27 at 19 36 13](https://github.com/space-hippie0/matlab/assets/118982314/cba55078-e508-48a9-92d0-c14718bf4fcc)
% Generate an 8x8 Pascal matrix A
A = pascal(8);

% Perform the singular value decomposition (SVD) of A
[U, S, V] = svd(A);
				% U: Orthogonal matrix of left singular vectors
				% S: Diagonal matrix of singular values
				% V: Orthogonal matrix of right singular vectors

% Reconstruct a lower-rank approximation of A using the first 5 singular values and vectors
k = 5; 							% Number of singular values/vectors to consider

% An: Approximation of matrix A using the most significant singular values and vectors
An = U(:, 1:k) * S(1:k, 1:k) * V(:, 1:k)';

% error: Frobenius norm, which measures the difference between A and An
error = norm(A - An);

% Display the result
disp(['The Frobenius norm of the difference between A and An is: ' num2str(error)]);




Type (8) - E
![SS 2023-05-27 at 19 45 46](https://github.com/space-hippie0/matlab/assets/118982314/43d5b4fa-2a55-49bf-a32e-39661a7cec25)
% Generate a vector x with 10 equally spaced values between 0 and 1
x = linspace(0, 1, 10);

% A: Vandermonde matrix with powers of x as columns
A = vander(x);

% Perform the singular value decomposition (SVD) of A
[U, S, V] = svd(A);
				% U: Orthogonal matrix of left singular vectors
				% S: Diagonal matrix of singular values
				% V: Orthogonal matrix of right singular vectors

% Initialize a matrix An with zeros
An = zeros(10, 10);

% Reconstruct An using the first 7 singular values and corresponding vectors
k = 7; 					  % Number of singular values/vectors to consider
for i = 1:k
    An = An + S(i, i) * U(:, i) * V(:, i)';
end
% An: Reconstructed matrix using the selected singular values and vectors

% normAn: Infinity norm, which measures the maximum absolute row sum of An
normAn = norm(An, inf);

% Display the result
disp(['The infinity norm of An is: ' num2str(normAn)]);


Type (9) - D

% Generate a 12x12 Hilbert matrix A
A = hilb(12);

% Perform QR factorization of A for 8 iterations
for i = 1:8
    % QR factorization of A
    [Q, R] = qr(A);
    
    % Update A by multiplying R and Q
    A = R * Q;
end

% Retrieve and display the value at the (3, 3) position of A
value = A(3, 3);
value
 


Type (10) - E

% Set the order of the matrix
n = 6;

% Create a Pascal matrix of order n
A = pascal(n);

% Set the value of p
p = 2;

% Initialize the vector z with all ones
z = ones(n, 1);

% Perform iterations to compute lambda
for i = 1:4
    % Normalize z
    w = z / norm(z);
    
    % Solve the linear system (A-p*I)z = w
    z = (A - p * eye(n)) \ w;
end

% Compute the value of lambda
lambda = p + 1 / (w' * z);

% Compute the approximate eigenvalue using the eigs function
aval = eigs(A, 1, p);

% Compute the error between aval and lambda
err = abs(aval - lambda);
