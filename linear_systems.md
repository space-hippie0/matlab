(Type trivial 1)
![SS 2023-05-27 at 16 31 22](https://github.com/space-hippie0/matlab/assets/118982314/679f41ca-e116-46a9-9816-0f65fa5ae98e)

(Type trivial 2)
![SS 2023-05-27 at 16 38 59](https://github.com/space-hippie0/matlab/assets/118982314/511eccb9-0f34-4300-acbe-8d8f9126f94c)

(Type trivial 3)
![SS 2023-05-27 at 16 38 46](https://github.com/space-hippie0/matlab/assets/118982314/e83f6bbf-5407-456e-a9d7-530650ccf373)

(Type trivial 4)
![SS 2023-05-27 at 16 51 59](https://github.com/space-hippie0/matlab/assets/118982314/ea9f8091-5bdc-47fe-94e5-3c76d9ad2221)

(Type trivial 5)
![SS 2023-05-27 at 17 00 03](https://github.com/space-hippie0/matlab/assets/118982314/4a491f2e-b4f6-4039-9797-05a00cccd971)

(Type trivial 6)
![SS 2023-05-27 at 17 03 30](https://github.com/space-hippie0/matlab/assets/118982314/340b7917-bd63-4046-9d65-35bacdfb0dcc)



Type (1) - A
![SS 2023-05-27 at 16 29 06](https://github.com/space-hippie0/matlab/assets/118982314/fe473f91-396c-43a7-b453-29f32d28f254)
```
A = [6*pi, 3, 7;  6, 9, -1;  -3, -2, 7];
b = [log(2), 6, pi*(-2)]';
x = A\b;
x(2)
```

Type (2) - C
![SS 2023-05-27 at 16 34 16](https://github.com/space-hippie0/matlab/assets/118982314/f3166fd2-ce71-41f5-8250-e812981338d1)
```
İlk adım, matrisin (A|b) ilk satırın ilk öğesinin altında
tüm sıfırlara sahip olacak şekilde manipüle edilmesinden oluşur.
```

Type (3) - C
![SS 2023-05-27 at 16 42 22](https://github.com/space-hippie0/matlab/assets/118982314/d76d7d1d-1bd0-4620-94e6-99a233d559b2)
```
A = 6*eye(18) + 3*diag(ones(17,1),1) + 3*diag(ones(17,1),-1);
```
```
b = linspace(5,8,18)';
```
```
R = chol(A);
```
```
y = R'\b;
x = R\y;
s = x+y;
norm(s,1)
```

Type (4) - A
![SS 2023-05-27 at 16 46 46](https://github.com/space-hippie0/matlab/assets/118982314/dd06b48d-7404-4b4d-aac8-29d6f4f53b2c)
```
A=4*eye(100) ...
+(-1)*diag(ones(99,1),1) ...
+(-1)*diag(ones(99,1),-1) ...
+(-2)*diag(ones(90,1),10) ...
+(-2)*diag(ones(90,1),-10);
```
```
cond(A,inf)
```

Type (5) - E
![SS 2023-05-27 at 16 48 28](https://github.com/space-hippie0/matlab/assets/118982314/5c426fb0-f20e-4bae-8a89-a32ecc71752a)
```
A=[6*pi,3,2,1; 3,7*pi,1,0; 2,1,6,0; 1,0,0,4];
R=chol(A);
R(3,3)
```


Type (6) - C
![SS 2023-05-27 at 16 53 50](https://github.com/space-hippie0/matlab/assets/118982314/f8c3d005-4e11-4a0b-8d76-cc9ef63a2755)
```
A=6*eye(18) + 3*diag(ones(17,1),1) ...
+3*diag(ones(17,1),- 1);
```
```
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

Type (7) -  C
![SS 2023-05-27 at 16 56 10](https://github.com/space-hippie0/matlab/assets/118982314/5c157a28-7e62-4ea8-b955-171bceaa4aaa)

```
A = hilb(4);
[L,U,P] = lu(A);
P
```

Type (8) -  B
![SS 2023-05-27 at 16 58 07](https://github.com/space-hippie0/matlab/assets/118982314/681d1899-bebe-455e-8c52-c084fe27066f)
```
A=[4,6; 3/5,1]; 
cond(A,inf) 
```
