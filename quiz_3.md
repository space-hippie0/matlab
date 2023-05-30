# # # (Trivial 1) # # #
![quiz3_trv1](https://github.com/space-hippie0/matlab/assets/118982314/69f91ca8-776a-4ef6-886d-ff51f7628053)

B = 5 000
A = 1
s = a+b

# # # (Trivial 2) # # #
![quiz3_trv2](https://github.com/space-hippie0/matlab/assets/118982314/7db1f80e-1d68-43fa-acff-7078add6947e)



# # # Type (1) - D # # #
![quiz3_1](https://github.com/space-hippie0/matlab/assets/118982314/aac846c9-f3e6-4a46-a2d8-d47d0423c7c9)

```
x=linspace(1,2,6);
A=vander(x);
[U,S,V]=svd(A);
```
```
An=zeros(6,6);
```
```
for k=1:4
    An=An+S(k,k)*U(:,k)*V(:,k)';
end
norm(An,2)
```

# # # Type (2) - B (IDK) # # #
![quiz3_2](https://github.com/space-hippie0/matlab/assets/118982314/0e6c0a08-5313-44fd-a7eb-59dfaafd7ea1)




# # # Type (3) - C # # #
![quiz3_3](https://github.com/space-hippie0/matlab/assets/118982314/13031265-858e-4b4f-b160-22ee79215463)
```
A=hilb(6);
p=0.2;
```
```
z=ones(6,1);
w=z/norm(z);
lambda(1)=p;
[L,U,P]=lu(A-p*eye(6));
```
```
for i=1:4
y=L\P*w;
z=U\y; lambda(i+1)=p+1/(w'*z); w=z/norm(z);
end
```
```
aval=eigs(A,1,p);
err=abs(aval-lambda(i+1))/abs(aval)
```


# # # Type (4) - IDK (2.9021e+00) # # #
![quiz3_4](https://github.com/space-hippie0/matlab/assets/118982314/59b1ba03-19dc-43bc-b159-0dfcf6b01365)

```
f=@(x) x.^3.*exp(x);
x=linspace(0,1,9);
y=f(x);
```
```
d=@(x) 3.*x.^2.*exp(x)+x.^3.*exp(x);
z=linspace(0,1,100);
```
```
s=spline(x,[d(1) y d(2)],z);
maxerr=max(abs(f(z)-s))
```
% the result is 1.2032e-04 (A)



# # # Type (5) - B # # #
![quiz3_5](https://github.com/space-hippie0/matlab/assets/118982314/72eccbd1-c337-4cdd-b5ab-f0440495d47f)

```
H=hilb(10);
b=[2:2:20]';
x=H\b;
x(5)
```



# # # Type (6) - IDK # # #
![quiz3_6](https://github.com/space-hippie0/matlab/assets/118982314/594eef41-ccc0-4e70-b4eb-dce4a0dacca2)
```
f=@(x) exp(-x.^2).*sin(x); 
x=linspace(0,1);
y=f(x);
max(x)
```
% credo should be D but it is A




# # # Type (7) - IDK (C) # # #
![quiz3_7](https://github.com/space-hippie0/matlab/assets/118982314/0925033e-2fd1-47f1-b90a-39ecd12ca984)




# # # Type (8) - IDK (A) # # #
![quiz3_8](https://github.com/space-hippie0/matlab/assets/118982314/cc2c82bb-4db1-49db-a102-f9d79b626641)





# # # Type (9) - C # # #
![quiz3_9](https://github.com/space-hippie0/matlab/assets/118982314/51f749ee-efeb-4bae-9696-5b9c5eab8b75)

```
H=hilb(10);
b=[2:2:20]';
x=H\b;
x(3)
```



# # # Type (10) - A # # #
![quiz3_10](https://github.com/space-hippie0/matlab/assets/118982314/f95f42ab-8c99-4a60-82e9-7461a29a2095)

```
A=hilb(6);
p=0.2;
```
```
z=ones(6,1);
w=z/norm(z);
lambda(1)=p;
[L,U,P]=lu(A-p*eye(6));
```
```
for i=1:6
y=L\P*w;
z=U\y; lambda(i+1)=p+1/(w'*z); w=z/norm(z);
end
```
```
aval=eigs(A,1,p);
err=abs(aval-lambda(i+1))/abs(aval)
```

# # # Type (11) - B # # #
![quiz3_11](https://github.com/space-hippie0/matlab/assets/118982314/d2589da0-89a3-43c7-bb20-d2c52a9675b4)
```
f=@(x) exp(-x.^2).*cos(x); 
x=linspace(0,1);
y=f(x);
max(x)
```

# # # Type (12) - E # # #
![quiz3_12](https://github.com/space-hippie0/matlab/assets/118982314/ad4c8709-d273-4fe2-8cb7-7fe122f7a2d5)


