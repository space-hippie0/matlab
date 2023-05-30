(Trivial 1)
![quiz1_trv1](https://github.com/space-hippie0/matlab/assets/118982314/f56ced90-2c68-4cb6-bef5-6ada2423dfc1)
![](sscreen/quiz1/quiz1_1 "1")

Type (1) - E

A=magic(4320)+10*eye(4320);
z=ones(4320,1);
b=A*z;
x=A\b;
residuo=b-A*x;
nr=norm(residuo,inf)


Type (2) - B

f = @(x) sin(3.*cos(x)).*cos(3.*sin(x));
x = linspace(-4,4);
y = f(x);
plot(x,f(x))


Type (3) - B

A=6*eye(180) + 3*diag(ones(179,1),1) + 3*diag(ones(179,1),- 1);
x=zeros(180,3);

for j=1:5
    b=linspace(0,j,180)';
    x(:,j)=A\b;
end
s=sum(x,2);
norm(s)


Type (4) - A

n=7;
f=@(x) exp(x.^2);
x=linspace(0,1,n);
y=f(x);
c=polyfit(x,y,(n-1));
z=linspace(0,1,150);
p=polyval(c,z);
errmax=max(abs(f(z)-p))


Type (5) - C

for i=1:100
    for j=1:100
    A(i,j)=cos(max(i,j));
    end 
end
cond(A,inf)


Type (6) - B

x=10^(-6);
y=5-sqrt(25+x^2);
y_=(-x^2)/(5+sqrt(25+x^2));
err=abs(y-y_)/abs(y_)


Type (7) - C

A=hilb(100)+(0.001)*eye(100);
z=[1:1:100]';
b=A*z;
x=A\b;
err=norm(abs(x-z),inf)

Type (8) - E

n = 9;
f = @(x) exp((x-2).^2);
x = linspace(0,1,n);
y = f(x);

c=polyfit(x,y,(n-1));
z=linspace(0,1,150);
p=polyval(c,z);
errmax=max(abs(f(z)-p))


Type (9) - A

f = @(x) sin(5.*cos(x)).*cos(5.*sin(x))
x = linspace(0,1);
y = f(x);
plot(x,f(x))


Type (10) - A

x = 10^(-6);
y = 9-sqrt(81+x^2);
y_=(-x^2)/(9+sqrt(81+x^2));
err = abs(y-y_)/abs(y_)


Type (11) - D

A = 6*eye(18) + 3*diag(ones(17,1),1) + 3*diag(ones(17,1),-1);
x=zeros(18,3);

for j=1:3
    b=linspace(0,j,18)';
    x(:,j)=A\b;
end
s=sum(x,2);
norm(s)

Type (12) - C

A=magic(432)+10*eye(432);
z=ones(432,1);
b=A*z;
x=A\b;
residuo=b-A*x;
nr=norm(residuo,inf)


Type (13) - D

A = hilb(7)+(0.001)*eye(7);
z=[1:1:7]';
b=A*z;
x=A\b;
err=norm(abs(x-z),inf)

Type (14) - B

v=[1:1:30];
   w=1./sqrt(v);
   sum(w)


Type (15) - B

for i=1:100
    for j=1:100
    A(i,j)=sin(max(i,j));
    end 
end
cond(A,2)




Type (16) - C

v=linspace(1,3,30);
w=linspace(0,5,30);
ps=sum(v.*w)
