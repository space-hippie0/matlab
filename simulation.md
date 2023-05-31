# # # UNO # # #
![simulation1](https://github.com/space-hippie0/matlab/assets/118982314/e5c2a254-372e-4a2f-a996-65e7ba04ce95)
% create matrix
```
A = magic(3);
```
% QR factorization
```
[Q, R] = qr(A);
```

% solve lineer system
```
b = [1; 2; 3];

x = Q' * b
```
%b




# # # DUE # # #
![simulation2](https://github.com/space-hippie0/matlab/assets/118982314/5a832037-4719-4a59-a0ec-5a82f4f96a22)
% creating a matrix
```
n = 100;
A = zeros(n);
```
% generic element transformation
```
for i = 1:n
    for j = 1:n
        A(i, j) = max(i, j);
    end
end
```
% Choleski factor of B
```
B = A' * A;
L = chol(B, 'upper');
element = L(52, 64)
```
%a



# # # TRE # # #
![simulation3](https://github.com/space-hippie0/matlab/assets/118982314/f210be82-cef6-40ed-87bc-2e41b21bae35)
% function and interval
```
f = @(x) sin(x);
x = linspace(0,1,9);
y = f(x);
```
```
z = linspace(0,1,180);
```
% spline 
```
s = spline(x,y,z);
% absolute interpolation error
```
```
maxerr = max(abs(f(z)-s))
```
%e








# # # QUATTRO # # #
![sim4](https://github.com/space-hippie0/matlab/assets/118982314/5da81156-d540-491c-af7b-6b7fc48d8f78)
% function
```
x = 10^-6;
exact = 1 - sqrt(1 + x^2);
```
% eslenik ile carpilmis hali
```
approx = -x^2 / (1 + sqrt(1 + x^2));
```
% relative error
```
err = abs(approx - exact) / abs(exact)
```
%a


# # # CINQUE # # #
![sim5](https://github.com/space-hippie0/matlab/assets/118982314/a43d8b97-6b69-4109-b549-52e75ce5c206)
% creating the matrix
```
A = diag(5 * ones(100, 1)) + diag(1 * ones(99, 1), 1) + diag(-1 * ones(99, 1), -1);
```
% eigen values
```
eigenvalues = eig(A);
```
% min and max lambda
```
min_lambda = min(abs(eigenvalues))
max_lambda = max(abs(eigenvalues))
```
%b

# # # SEI # # #
![sim6](https://github.com/space-hippie0/matlab/assets/118982314/2bcf18db-19aa-4526-b50a-9c37aedf17b5)

# # # SETTE # # #
![sim7](https://github.com/space-hippie0/matlab/assets/118982314/e7037d77-228c-4863-b983-63fee6791bde)

# # # OTTO # # #
![sim8](https://github.com/space-hippie0/matlab/assets/118982314/f2c39e11-a7c6-41b9-b687-1d0d97083c72)
% change format
```
format short
```
```
A = magic(3);
b = [1; 2; 3];
```
% QR factorization
```
[Q, R] = qr(A);  
```
% linear system
```
x = R \ b; 
```
%d
