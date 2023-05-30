 # # (Type trivial 1) # # 
![SS 2023-05-27 at 17 15 53](https://github.com/space-hippie0/matlab/assets/118982314/cd2b7c15-663b-4755-a0dd-e9046fa2a883)

 # # Type (1) - E # # 
![SS 2023-05-27 at 17 08 41](https://github.com/space-hippie0/matlab/assets/118982314/4c2ff754-9c49-44da-8c13-6b95629066da)
```
x=[0,1,2];
y=[1,2,4];
c=polyfit(x,y,1)
```
 # # Type (2) - C # # 
![SS 2023-05-27 at 17 10 09](https://github.com/space-hippie0/matlab/assets/118982314/f5443428-a8ff-4b89-8a50-91f14c047bf5)
```
x=[-2, -1.3, -1, -0.7, -0.4, -0.1];
y=[0.3, 0.5, 1.5, 1.3, 0.8, 0.1];
```
```
c=polyfit(x,y,2); 					% bir parabol istiyor, bu nedenle 2. dereceden olmalı
z=3;
```
```
p=polyval(c,z);
abs(p-1.5)
```
 # # Type (3) - A # # 
![SS 2023-05-27 at 17 12 48](https://github.com/space-hippie0/matlab/assets/118982314/d6e17649-39dc-42da-9a29-87c9a4c4f6c5)
```
n=30; 
f=@(x) x.*sin(x);
```
```
x=linspace(0,1/2*pi);
```
```
y=f(x);
c=polyfit(x,y,2) 
```

 # # Type (4) - C # # 
![SS 2023-05-27 at 17 17 13](https://github.com/space-hippie0/matlab/assets/118982314/fd7e0fee-c6fd-44e1-b8b8-99f7d6b8e6d6)
```
x=[0.2, 1.14, 0.54, 0.87, 1.25, 2.36, 0.19, 0.54, 0.51, 0.33];
y=[1.25, 2.36, 2.58, 1.87, 2.68, 3.41, 0.65, 0.47, 1.36, 1.25];
```
```
c=polyfit(x,y,1)                  % Eğim, c'nin ilk terimidir.
```

 # # Type (5) - B # # 
![SS 2023-05-27 at 17 20 01](https://github.com/space-hippie0/matlab/assets/118982314/d310c2ea-d8db-42a8-b667-b69b3855e040)
```
x=[0, 8, 18];
y=[44, 43, 67];
```
```
c=polyfit(x,y,1);
z=2;
polyval(c,z)
```

 # # Type (6) - B # # 
![SS 2023-05-27 at 17 21 47](https://github.com/space-hippie0/matlab/assets/118982314/b2cd3d18-6862-4c29-828d-7c49ef21df79)
```
x=[0.34, 0.19, 0.25, 0.61, 0.47, 0.35, 0.83];
y=[0.58, 0.54, 0.91, 0.28, 0.75, 1.17, 0.38];
```
```
z=exp(x);
c=polyfit(z,y,2)
```


 # # Type (7) - E # # 
![SS 2023-05-27 at 17 23 39](https://github.com/space-hippie0/matlab/assets/118982314/8b251965-94fd-4aef-befb-a748429b1932)
```
x=[0,1,2,3];
y=[1,2,4,8];
z=exp(x);
```
```
c=polyfit(z,y,1)
p=polyval(c,z);
res=norm(p-y)
```

 # # Type (8) - D # # 
![SS 2023-05-27 at 17 29 23](https://github.com/space-hippie0/matlab/assets/118982314/3827b74a-90c0-4826-8f51-002bbfe6bdb0)
```
n=22;
f=@(x) x.^2.*log(1+x);
x=linspace(0,5,n); y=f(x);
```
```
c=polyfit(x,y,4);
p=polyval(c,2) 
```
