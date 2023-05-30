 # # Type (1) - D # # 
![machine-1](https://github.com/space-hippie0/matlab/assets/118982314/7b827234-cef6-49bb-a53b-9a66936fed1e)
```
for n=1:14
    L(n) = (1-cos(10^-n))./(10^-n)^2;
end

[min,index] = min(abs(L-1/2))
```

 # # Type (2) - E # # 
![machine-2](https://github.com/space-hippie0/matlab/assets/118982314/f14176da-5a42-4d71-be37-582216107b49)
```
N=2;
t=3;
U=3;
L=-2;
```
```
res = (N-1)*(N.^(t-1))*((U-L)+1)
```
 # # Type (3) - A # # 
![machine-3](https://github.com/space-hippie0/matlab/assets/118982314/d3a2b841-de64-444b-bede-22f448b97707)

```
x1 = 1.7;
d1 = 2.1 * 10 ^ -9;
x2 = 31000;
d2 = 7.1 * 10 ^ -4;
```
```
f = @(x,d) sqrt(x+d) - sqrt(x);
fn = @(x,d) d/(sqrt(x+d)+sqrt(x));
```
```
abs(f(x1,d1)-fn(x1,d1))/abs(fn(x1,d1))
abs(f(x2,d2)-fn(x2,d2))/abs(fn(x2,d2))
```

 # # Type (4) - E # # 
![machine-4](https://github.com/space-hippie0/matlab/assets/118982314/a005241f-962d-4c52-b8c9-a51bb05d6d49)

```
N=2;
t=2;
U=2;
L=0;
```
```
res = (N-1)*(N.^(t-1))*((U-L)+1)
```


 # # Type (5) - B # # 
![machine-5](https://github.com/space-hippie0/matlab/assets/118982314/7b670a98-ebe1-4400-b5f3-6a38be906dc0)
```
x(1) = 2;
for n = 2:40
    x(n) = 2.^(n-1/2) .* sqrt(1-sqrt(1-(4.^(1-n) .* x(n-1).^2)));
end
```
```
min(abs(x-pi))/pi
```

 # # Type (6) - D # # 
![machine-6](https://github.com/space-hippie0/matlab/assets/118982314/b5a54690-780b-4c4f-9f07-f1034e0f03f9)
```
x = 10^-6;
f1 =@(x) 1-sqrt(1+x.^2); 				% ilk verilen y fonksiyonu
y1= f1(x);
```
```
f2 = @(x) -x.^2 / (1+ sqrt(1+x.^2)); 		% ilk verilen y fonksiyonunun eşleniğiyle 
y2 = f2(x);
```
```
err= abs(y1-y2)/ abs(y2) 				% basic rel. error
```
