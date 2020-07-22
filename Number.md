### 1.Số hoàn thiện (Perfect Number)

Số hoàn thiện là một số nguyên dương mà tổng các ước nguyên dương chính thức của nó bằng chính nó

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int n
    int sum=0;
    printf("Enter number = ");
    scanf("%d",&n);
    for (int i = 1; i < n; i++){
        if (n%i==0){
            sum+=i;
        }
    }
    if (sum==n)
        printf("%d is a perfect number",n);
    else
        printf("%d not is a perfect number",n);
    return 0;
}
```

---

### 2.Dãy Fibonacci (Fibonacci Series)

Dãy Fibonacci là **dãy vô hạn** các **số tự nhiên** bắt đầu bằng 2 phần tử 0 và 1 hoặc 1 và 1, các phần tử sau đó được thiếp lập theo quy tắc mỗi phần tử luôn bằng tổng 2 phần tử trước nó. 

**<u>Công thức truy hồi sau đây:</u>**

<img src="https://raw.githubusercontent.com/Zenfection/Image/master/2020/07/22-16-14-55-A%CC%89nh%20chu%CC%A3p%20Ma%CC%80n%20hi%CC%80nh%202020-07-22%20lu%CC%81c%2016.13.20.png" title="" alt="Ảnh chụp Màn hình 2020-07-22 lúc 16.13.20.png" width="305">

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
	int a,b,c,n;
	a=0;
	b=1;
	printf("Enter length of the range : ");
	scanf("%d",&n);
	printf("Fibonacci Series : %d %d ",a,b);
	for (int i = 0; i < n; i++){
		c=a+b;
		a=b;
		b=c;
		printf("%d ",c);
	}
	return 0;
}
```

---

### 3.Nhân tố của 1 số  (Factorial of a Number)

```c

```

---

### 4.Số Armstrong (Armstrong Number)

---

### 5.Đảo ngược của 1 số

---

### 4.Tìm số chẳn hoặc lẻ
