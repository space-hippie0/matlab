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
￼
x = [-5 4 5 11];
y = [6 2 4 10];
z = sqrt(1.8);

y0 = 10;
yn = 4;

spline(x, [y0,y,yn], z)


Type (2) - A
￼
x = [-1 1 7 9 19];
y = [4 3 10 10 9];
z = log(0.9);

spline(x,y,z)

Type (3) - D
￼
x = [-5 4 5 11];
y = [6 2 4 10];
z = sqrt(1.8);

y0 = 10;
yn = 4;

spline(x, [y0,y,yn], z)


Type (4) - B
￼
f = @(x) sqrt(1+x.^2);
a = 0;      % interval start
b = 5;      % interval end
n = 4;      % nodes (n-1)

for i = 1:n+1
    t(i) = -cos((((2.*i)-1)*pi)./(2*(n+1)));
    x(i) = (((b-a)/2).* t(i)) + ((b+a)/2);
end

y = f(x);
c = polyfit(x,y,n)


Type (5) - D
￼
x = [0.0 0.5 1.0 1.5 2.0]; 					% x degerlerini verildiği gibi yazdık
f =@(x) (sin(x) - (x+1).^2)./((x.^2)+3); 		% fonksiyonu da ayni sekilde
y=f(x);
z=1.97;
spline(x,y,z)


Type (6) - B
￼
n=5;

x = [3 6 7 14 21];
y = [8 4 5 5 7];
z= exp(0.7);

c = polyfit(x, y , n-1);
polyval(c,z)


Type (7) - D
￼
n=4; 			% x,y eleman sayisi

x = [1,2,3,4];
y = [1,-1,1,-1];

polyfit(x,y,n-1)


Type (8) - A
￼
4
n=5;
f=@(x) sin(x);

x=linspace(0,pi,n);
y=f(x);

c=polyfit(x,y,(n-1));
z=pi/8;

p=polyval(c,z)


Type (9) - D
￼
n=8;
f= @(x) atan(x.*(x+1));
x= linspace(0,1,n);
y= f(x);

c= polyfit(x,y,(n-1));

p1= polyval(c,0.5);
err1= abs(f(0.5)-p1)

p2= polyval(c,0.7);
err2=abs(f(0.7)-p2)


Type (10) - A
￼
n=4;
f=@(x) cos(x);
x=linspace(0,2*pi,n);
y=f(x);
c=polyfit(x,y,(n-1));
z=pi/8;
p=polyval(c,z)

