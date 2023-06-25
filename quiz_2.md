# # # Type (1) - C # # #
![quiz2_1](https://github.com/space-hippie0/matlab/assets/118982314/8e84b80e-2a62-465c-b0b3-c8585c928be0)
```
f = @(x) 1 + x.^2.*log(2+x);
x = [0.3,0.6,0.9,1.2,1.5];
y = f(x);
```
```
c = polyfit(x,y,4);
abs(f(3)-polyval(c,3))
```

# # # Type (2) - C # # #
![quiz2_2](https://github.com/space-hippie0/matlab/assets/118982314/1c2dcbaa-150f-4f06-80b5-0c33392d6327)
```
A=6*eye(18) + 3*diag(ones(17,1),1) + 3*diag(ones(17,1),-1);
```
```
b=linspace(5,8,18)';
```
```
R=chol(A);
```
```
y=R'\b;
x=R\y;
```
```
norm(x+y,1)
```


# # # Type (3) - A # # #
![quiz2_3](https://github.com/space-hippie0/matlab/assets/118982314/a2dec9b1-691a-4ad2-b349-e758873da87d)
```
x=[-2, -1.3, -1, -0.7, -0.4, -0.1];
y=[0.3, 0.5, 1.5, 1.3, 0.8, 0.1];
```
```
c=polyfit(x,y,2);
abs(polyval(c,4)-1.5)
```


# # # Type (4) - A # # #
![quiz2_4](https://github.com/space-hippie0/matlab/assets/118982314/de6825cf-ab15-4d4d-be6f-e41caf1412b0)
```
f = @(x) cos(x);
x = linspace(0,1,9);
y = f(x);
```
```
z = linspace(0,1,180);
```
```
s = spline(x,y,z);
maxerr = max(abs(f(z)-s))
```

# # # Type (5) - E # # #
![quiz2_5](https://github.com/space-hippie0/matlab/assets/118982314/257a2217-e5b5-4e6b-89e7-bb017eec6277)
```
x=10^-8;
f=@(x) sqrt((exp(x)-1)/x);
yerr=f(x);
f2=0;
```
```
for i=1:10
    f2 = f2+x^(i-1)/factorial(i);
end
```
```
y=sqrt(f2);
err=abs(y-yerr)/abs(y)
```

# # # Type (6) - D # # #
![quiz2_6](https://github.com/space-hippie0/matlab/assets/118982314/690db15e-31ad-46d8-9c4d-2c42808a0604)
```
f=@(x) exp(-x.^2).*cos(5.*x);
x=linspace(-1,1);
y=f(x);
plot(x,y)
```
% y=0 oldugu yerler real root


# # # Type (7) - D # # #
![quiz2_7](https://github.com/space-hippie0/matlab/assets/118982314/889249b0-37e8-403d-971d-7edfd690ab37)
```
f=@(x) x.^3-3.*x+1;
x=linspace(0,1,7);
y=f(x);
polyfit(x,y,6)
```

# # # Type (8) - E # # #
![quiz2_8](https://github.com/space-hippie0/matlab/assets/118982314/527d9c2c-340a-4736-8b24-e5b21cc0fcd3)

```
A = hilb(100);
```
% extract to B
```
B = A(1:2:end, 1:2:end);
```

% sum
```
sum_B = sum(B(:));
sum
```


# # # Type (9) - C # # #
![quiz2_9](https://github.com/space-hippie0/matlab/assets/118982314/799ca44d-d5aa-4999-a551-95905414da1f)
```
f = @(x) 1 + x.^2.*log(2+x);
x = [0.3,0.6,0.9,1.2,1.5];
y = f(x);
```
```
c = polyfit(x,y,4);
abs(f(5)-polyval(c,5))
```

# # # Type (10) - WTF (5.000) # # #
![quiz2_10](https://github.com/space-hippie0/matlab/assets/118982314/daa27aed-c22a-4eba-b432-5de12fcd47fc)
```
x=10^-5;
f=@(x) (1-cos(x))/(x^2);
yerr=f(x);
f2=0;
```
```
for i=1:10
    f2 = f2+x^(i-1)/factorial(i);
end
```
```
y=sqrt(f2);
err=abs(y-yerr)/abs(y)
```

# # # Type (11) - B  # # #
![quiz2_11](https://github.com/space-hippie0/matlab/assets/118982314/15cb29f2-1e49-47b6-a1ff-7de8ca96cfee)
```
A=hilb(50);
s=0;
```
```
for i=1:50
    for j=1:50
        if cos(A(i,j))>0.999
            s = s+1;
        end 
    end
end
s
```

# # # Type (12) - A  # # #
![quiz2_12](https://github.com/space-hippie0/matlab/assets/118982314/72adb729-a87d-4c61-8ad7-99acc0b259b5)
```
f=@(x) exp(-x.^2).*sin(5.*x);
x=linspace(-1,1);
y=f(x);
plot(x,y)
```
% y=0 oldugu yerler real root


# # # Type (13) - A  # # #
![quiz2_13](https://github.com/space-hippie0/matlab/assets/118982314/3eefb016-cbee-4ad3-a94e-0f4ac3319e4a)
```
f=@(x) exp(2*x)-exp(3*x);
x=linspace(-2,1,14);
y=f(x);
c=polyfit(x,y,6);
```
```
polyval(c,-1)
```
% pay attention it is 0.08…..


# # # Type (14) - E # # #
![quiz2_14](https://github.com/space-hippie0/matlab/assets/118982314/7c15d812-7535-4938-9b3d-7dd2006672bb)
```
n=7;
f = @(x) x.^4-x.^2-6;
x = linspace(0,1,n);
y=f(x);
polyfit(x,y,6)
```

# # # Type (15) - A # # #
![quiz2_15](https://github.com/space-hippie0/matlab/assets/118982314/d6a4cec3-fa33-4d8f-9125-147fd9e324d6)
```
f = @(x) sin(x);
x = linspace(0,1,9);
y = f(x);
```
```
z = linspace(0,1,180);
```
```
s = spline(x,y,z);
maxerr = max(abs(f(z)-s))
```


# # # Type (16) - E # # #
![quiz2_16](https://github.com/space-hippie0/matlab/assets/118982314/b4278691-1cd0-423a-90db-ee5d21836dcd)

```
f = @(x) 1 + x.^2.*log(2+x);
x = [0.3, 0.6, 0.9, 1.2, 1.5];
y = f(x);
```
```
c = polyfit(x, y, 4);           		% len(x) = 4
p = polyval(c, 3);
diff = abs(f(3) - p);
diff
```


# # # Type (17) - A # # #
![quiz2_17](https://github.com/space-hippie0/matlab/assets/118982314/e29d6f42-227f-4a23-a97f-be61723eb876)
```
A = hilb(70);
sum = 0;
```
```
for i=1:70
    for j=1:70
        if A(i,j)<0.01
            sum = sum + A(i,j);
        end
    end
end
sum
```
