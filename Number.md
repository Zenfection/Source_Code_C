### 1.Số hoàn thiện (Perfect Number)

Số hoàn thiện là một số nguyên dương mà tổng các ước nguyên dương chính thức của nó bằng chính nó

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
	int n
    long sum=0;
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

```c

```

---

### 3.Nhân tố của 1 số  (Factorial of a Number)



---

### 4.Số Armstrong (Armstrong Number)



---

### 5.Đảo ngược của 1 số



---

### 4.Tìm số chẳn hoặc lẻ








