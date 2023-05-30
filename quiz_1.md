# # # (Trivial 1) # # #

![quiz1_trv1](https://github.com/space-hippie0/matlab/assets/118982314/f56ced90-2c68-4cb6-bef5-6ada2423dfc1)

 # # # Type (1) - E # # # 
![quiz1_1](https://github.com/space-hippie0/matlab/assets/118982314/c3f07ff1-66df-432b-9c0a-8e66561c5457)

```
A=magic(4320)+10*eye(4320);
```
```
z=ones(4320,1);
```
```
b=A*z;
x=A\b;
```
```
residuo=b-A*x;
nr=norm(residuo,inf)
```


 # # # Type (2) - B # # # 
![Quiz1_2](https://github.com/space-hippie0/matlab/assets/118982314/ee8c145b-1cf8-4a0f-ab7a-bf317387d583)
```
f = @(x) sin(3.*cos(x)).*cos(3.*sin(x));
x = linspace(-4,4);
y = f(x);
```
```
plot(x,f(x))
```

 # # # Type (3) - B # # # 
![quiz1_3](https://github.com/space-hippie0/matlab/assets/118982314/209cfc74-726f-43cb-9b1d-2b4c91bd4d9f)
```
A=6*eye(180) + 3*diag(ones(179,1),1) + 3*diag(ones(179,1),- 1);
x=zeros(180,3);
```
```
for j=1:5
    b=linspace(0,j,180)';
    x(:,j)=A\b;
end
```
```
s=sum(x,2);
norm(s)
```

 # # # Type (4) - A # # # 
![quiz1_4](https://github.com/space-hippie0/matlab/assets/118982314/0d0a0d6f-68ef-410e-8557-2bdca60c55fa)
```
n=7;
f=@(x) exp(x.^2);
x=linspace(0,1,n);
y=f(x);
```
```
c=polyfit(x,y,(n-1));
```
```
z=linspace(0,1,150);
p=polyval(c,z);
```
```
errmax=max(abs(f(z)-p))
```


 # # # Type (5) - C # # # 
![quiz1_5](https://github.com/space-hippie0/matlab/assets/118982314/5882b689-5e72-4112-a3bf-ecfbf2f99b0a)
```
for i=1:100
    for j=1:100
    A(i,j)=cos(max(i,j));
    end 
end
```
```
cond(A,inf)
```


 # # # Type (6) - B # # # 
![quiz1_6](https://github.com/space-hippie0/matlab/assets/118982314/2f14b586-e8c6-4528-bf65-a97627a12e06)
```
x=10^(-6);
y=5-sqrt(25+x^2);
```
```
y_=(-x^2)/(5+sqrt(25+x^2));
```
```
err=abs(y-y_)/abs(y_)
```


 # # # Type (7) - C # # # 
![quiz1_7](https://github.com/space-hippie0/matlab/assets/118982314/dfde9fcc-6774-434e-8707-71a34d4a25b3)
```
A=hilb(100)+(0.001)*eye(100);
z=[1:1:100]';
```
```
b=A*z;
x=A\b;
```
```
err=norm(abs(x-z),inf)
```

 # # # Type (8) - E # # # 
![quiz1_8](https://github.com/space-hippie0/matlab/assets/118982314/351812ed-8f9f-4513-b51b-1f834f8a1e83)
```
n = 9;
f = @(x) exp((x-2).^2);
```
```
x = linspace(0,1,n);
y = f(x);
```
```
c=polyfit(x,y,(n-1));
```
```
z=linspace(0,1,150);
p=polyval(c,z);
```
```
errmax=max(abs(f(z)-p))
```

 # # # Type (9) - A # # # 
![quiz1_9](https://github.com/space-hippie0/matlab/assets/118982314/1d346bc9-6063-4574-adeb-b1a45e9fa157)
```
f = @(x) sin(5.*cos(x)).*cos(5.*sin(x))
x = linspace(0,1);
y = f(x);
```
```
plot(x,f(x))
```


 # # # Type (10) - A # # # 
![quiz1_10](https://github.com/space-hippie0/matlab/assets/118982314/cc4a3e2d-14bd-41db-8688-c9f7529e219f)
```
x = 10^(-6);
y = 9-sqrt(81+x^2);
```
```
y_=(-x^2)/(9+sqrt(81+x^2));
```
```
err = abs(y-y_)/abs(y_)
```


 # # # Type (11) - D # # # 
![quiz1_11](https://github.com/space-hippie0/matlab/assets/118982314/c9184d43-cf22-4abd-bca1-69a0cf6897a4)
```
A = 6*eye(18) + 3*diag(ones(17,1),1) + 3*diag(ones(17,1),-1);
x=zeros(18,3);
```
```
for j=1:3
    b=linspace(0,j,18)';
    x(:,j)=A\b;
end
```
```
s=sum(x,2);
norm(s)
```
 # # # Type (12) - C # # # 
![quiz1_12](https://github.com/space-hippie0/matlab/assets/118982314/3887cfca-3255-4b88-a8d2-8f88e8367952)
```
A=magic(432)+10*eye(432);
z=ones(432,1);
```
```
b=A*z;
x=A\b;
```
```
residuo=b-A*x;
nr=norm(residuo,inf)
```

 # # # Type (13) - D # # # 
![quiz1_13](https://github.com/space-hippie0/matlab/assets/118982314/908a0327-6bb2-4603-82e0-b5b16a496e2e)
```
A = hilb(7)+(0.001)*eye(7);
```
```
z=[1:1:7]';
b=A*z;
x=A\b;
```
```
err=norm(abs(x-z),inf)
```
 # # # Type (14) - B # # # 
![quiz1_14](https://github.com/space-hippie0/matlab/assets/118982314/03cdd933-238d-4f4a-905a-3fdd6f9605bc)
```
v=[1:1:30];
   w=1./sqrt(v);
   sum(w)
```

 # # # Type (15) - B # # # 
![quiz1_15](https://github.com/space-hippie0/matlab/assets/118982314/d606736f-8d9c-4cab-ba9f-21ece8c8422a)
```
for i=1:100
    for j=1:100
    A(i,j)=sin(max(i,j));
    end 
end
cond(A,2)
```

 # # # Type (16) - C # # # 
![quiz1_16](https://github.com/space-hippie0/matlab/assets/118982314/f68326cc-60d2-4614-b723-9376df3e99d7)
```
v=linspace(1,3,30);
w=linspace(0,5,30);
ps=sum(v.*w)
```
