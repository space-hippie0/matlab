# # # (Type trivial 1) # # #
![SS 2023-05-27 at 12 47 05](https://github.com/space-hippie0/matlab/assets/118982314/914f039e-3cde-4529-af99-f2d694f963d3)

# # # (Type trivial 2) # # #
![SS 2023-05-27 at 13 03 09](https://github.com/space-hippie0/matlab/assets/118982314/41021b42-c58a-45c3-9144-ac3878a935e8)

# # # (Type trivial 3) # # #
![SS 2023-05-27 at 13 04 36](https://github.com/space-hippie0/matlab/assets/118982314/8b57bcc4-f95a-43f8-ac8f-3d0a6c0f2843)

# # # (Type trivial 4) # # #
![SS 2023-05-27 at 13 09 57](https://github.com/space-hippie0/matlab/assets/118982314/540f5498-5abd-4798-97d7-6976938324c0)


# # # Type (1) - A # # #

![SS 2023-05-27 at 12 57 15](https://github.com/space-hippie0/matlab/assets/118982314/0fac9f40-7e9d-4195-a0bc-9c7cc47aaa5b)
```
x = [0.01, 1];
f=@(x)sin(1./(x));
y=f(x);
semilogx(x,y)
```


# # # Type (2) - C # # #

![SS 2023-05-27 at 13 02 29](https://github.com/space-hippie0/matlab/assets/118982314/7f767741-6bd3-4e24-869c-89539aaf607d)
```
f1=inline('x.^2');
f2=inline('(x-1).^2');
x=linspace(0,2);
y1=f1(x);
y2=f2(x);
plot(x,y1,x,y2)
```


# # # Type (3) - A # # #

![SS 2023-05-27 at 13 07 39](https://github.com/space-hippie0/matlab/assets/118982314/43888a28-3d55-4c7c-9229-bfe7e9d9667d)
```
x = linspace(0,4);
f = @(x) exp(x.^2);
y = f(x);
```
```
semilogy(x,y);
```


# # # Type (4) - C # # #
![SS 2023-05-27 at 13 11 46](https://github.com/space-hippie0/matlab/assets/118982314/721131cd-d0c2-4d5a-a8ed-c4840a94a87e)
```
x = linspace(1,100);
y = linspace(1,100);
```
```
for k=1:100
    x(k)= log(k) + sqrt(k);
    y(k)= (k)./(6*pi);
end
```
```
c=dot(x,y)
```

# # # Type (5) - D # # #
![SS 2023-05-27 at 13 20 25](https://github.com/space-hippie0/matlab/assets/118982314/56e2cc62-ec2f-465e-b064-599085719394)
```
x = linspace(28, 52, 1000);
```
```
for i = 1:1000

    if mod(i,2) == 0
        x(i) = 2 * x(i);

    elseif mod(i,2) == 1
        x(i) = 5 * x(i);
    end
end
```
```
x(456)
```
