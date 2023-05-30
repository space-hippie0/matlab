(Type trivial)
￼![SS 2023-05-27 at 11 19 43](https://github.com/space-hippie0/matlab/assets/118982314/64195005-2db0-4b14-b71f-5a61e1c66b3b)

(Type trivial 2)
￼![SS 2023-05-27 at 11 19 48](https://github.com/space-hippie0/matlab/assets/118982314/32b913a0-42c0-4b83-9bcb-51c708ea171c)

(Type trivial 3)
￼![SS 2023-05-27 at 12 21 02](https://github.com/space-hippie0/matlab/assets/118982314/c2533977-848e-458b-b877-9c25d18b8ce1)

(Type trivial 4)
￼![SS 2023-05-27 at 11 39 04](https://github.com/space-hippie0/matlab/assets/118982314/dbe9f893-22c5-49ca-bb38-d7691649f360)

(Type trivial 5)
￼![SS 2023-05-27 at 12 29 19](https://github.com/space-hippie0/matlab/assets/118982314/fbbb5057-88c8-4e29-a29d-92da23bbe611)

(Type trivial 6)
￼![SS 2023-05-27 at 12 34 47](https://github.com/space-hippie0/matlab/assets/118982314/38e627da-3def-438d-a921-e8e001f32cd8)



Type (1) - B
￼![uno](https://github.com/space-hippie0/matlab/assets/118982314/2377f861-cf38-44e4-9f37-7e7e09b406cc)
```
x = [-5 4 5 11];
y = [6 2 4 10];
z = sqrt(1.8);
```
```
y0 = 10;
yn = 4;
```
```
spline(x, [y0,y,yn], z)
```

Type (2) - A
￼![due](https://github.com/space-hippie0/matlab/assets/118982314/ab05854f-78ee-4123-a25f-2f0749f1b7a6)
```
x = [-1 1 7 9 19];
y = [4 3 10 10 9];
z = log(0.9);
```
```
spline(x,y,z)
```
Type (3) - D
￼![tre](https://github.com/space-hippie0/matlab/assets/118982314/71da110a-8d08-4da8-97df-e6924bbe8ce9)
```
x = [-5 4 5 11];
y = [6 2 4 10];
z = sqrt(1.8);
```
```
y0 = 10;
yn = 4;
```
```
spline(x, [y0,y,yn], z)
```

Type (4) - B
￼![quattro](https://github.com/space-hippie0/matlab/assets/118982314/e540a5ba-08eb-4d54-9b0a-693fe0b6b676)
```
f = @(x) sqrt(1+x.^2);
a = 0;      % interval start
b = 5;      % interval end
n = 4;      % nodes (n-1)
```
```
for i = 1:n+1
    t(i) = -cos((((2.*i)-1)*pi)./(2*(n+1)));
    x(i) = (((b-a)/2).* t(i)) + ((b+a)/2);
end
```
```
y = f(x);
c = polyfit(x,y,n)
```

Type (5) - D
￼![cinque](https://github.com/space-hippie0/matlab/assets/118982314/9626716f-710f-45b9-bc7e-2dc49bd9d9a9)
```
x = [0.0 0.5 1.0 1.5 2.0]; 					% x degerlerini verildiği gibi yazdık
f =@(x) (sin(x) - (x+1).^2)./((x.^2)+3); 		% fonksiyonu da ayni sekilde
y=f(x);
```
```
z=1.97;
spline(x,y,z)
```

Type (6) - B
￼![sei](https://github.com/space-hippie0/matlab/assets/118982314/2e085f1c-2641-41fe-8a42-f36620772132)
```
n=5;
```
```
x = [3 6 7 14 21];
y = [8 4 5 5 7];
z= exp(0.7);
```
```
c = polyfit(x, y , n-1);
polyval(c,z)
```

Type (7) - D
￼![sette](https://github.com/space-hippie0/matlab/assets/118982314/49169173-3564-43fc-911e-7dad99176801)
```
n=4; 			% x,y eleman sayisi
```
```
x = [1,2,3,4];
y = [1,-1,1,-1];
```
```
polyfit(x,y,n-1)
```

Type (8) - A
￼![SS 2023-05-27 at 11 35 48](https://github.com/space-hippie0/matlab/assets/118982314/2d5c9fde-99db-4a5b-a2c5-e1528f749907)

```
n=5;
f=@(x) sin(x);
```
```
x=linspace(0,pi,n);
y=f(x);
```
```
c=polyfit(x,y,(n-1));
z=pi/8;
```
```
p=polyval(c,z)
```

Type (9) - D
￼![SS 2023-05-27 at 11 39 59](https://github.com/space-hippie0/matlab/assets/118982314/e18b6367-f17f-44b7-81ad-65f76a6e1331)
```
n=8;
f= @(x) atan(x.*(x+1));
x= linspace(0,1,n);
y= f(x);
```
```
c= polyfit(x,y,(n-1));
```
```
p1= polyval(c,0.5);
err1= abs(f(0.5)-p1)
```
```
p2= polyval(c,0.7);
err2=abs(f(0.7)-p2)
```

Type (10) - A
￼![SS 2023-05-27 at 12 17 10](https://github.com/space-hippie0/matlab/assets/118982314/d8a3ffc6-d93b-4d00-b5d6-a5e9cd118680)
```
n=4;
f=@(x) cos(x);
x=linspace(0,2*pi,n);
y=f(x);
```
```
c=polyfit(x,y,(n-1));
z=pi/8;
p=polyval(c,z)
```
