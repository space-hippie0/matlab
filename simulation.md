# # # UNO # # #
![simulation1](https://github.com/space-hippie0/matlab/assets/118982314/e5c2a254-372e-4a2f-a996-65e7ba04ce95)
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

f = @(x) sin(x);
x = linspace(0,1,9);
y = f(x);

z = linspace(0,1,180);

s = spline(x,y,z);
maxerr = max(abs(f(z)-s)) %e








# # # QUATTRO # # #

x = 10^-6;
exact = 1 - sqrt(1 + x^2);
approx = -x^2 / (1 + sqrt(1 + x^2));

relative_error = abs(approx - exact) / abs(exact)
%a


# # # CINQUE # # #

n = 100;
main_diag = 5;
off_diag = 1;
A = diag(main_diag * ones(n, 1)) + diag(off_diag * ones(n-1, 1), 1) + diag(-off_diag * ones(n-1, 1), -1);

eigenvalues = eig(A);

min_lambda = min(abs(eigenvalues))
max_lambda = max(abs(eigenvalues))
%b

# # # SEI # # #

# # # SETTE # # #

# # # OTTO # # #

format short
A = magic(3);
b = [1; 2; 3];

[Q, R] = qr(A);  

x = R \ b; 

%d
