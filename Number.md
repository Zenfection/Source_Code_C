### 1.Số hoàn thiện (Perfect Number)

Số hoàn thiện là một số nguyên dương mà tổng các ước nguyên dương chính thức của nó bằng chính nó

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int n;
    int sum=0;
    printf("Enter an integer = ");
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

| Input | Output                |
| ----- | --------------------- |
| 6     | 6 is a perfect number |

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

| Input | Output        |
| ----- | ------------- |
| 5     | 0 1 1 2 3 5 8 |

---

### 3.Giai thừa của 1 số  (Factorial of a Number)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int n;
    long fact=1;
    printf("Enter an integer : ");
    scanf("%d",&n);
    for (int i = 1; i <= n; i++){
        fact*=i;
    }
    printf("Factorial of %d is %ld",n,fact);
    return 0;
}
```

| Input | Output |
| ----- | ------ |
| 5     | 120    |

---

### 4.Số tự mãn (Armstrong Number)

**Số tự mãn** cũng được gọi là **số tuyệt hảo bất biến**, là 1 số mà có tổng các chữ số mũ n (n≥2) bằng chính nó.

Ví dụ: pow(3,3)+pow(7,3)+pow(1,3)=371

```c
#include <stdio.h>
#include <math.h>
int main(int argc, char const *argv[]){
	int a,n,b=0,t;
	printf("Enter an integer : ");
	scanf("%d",&n);
	t=n;
	while(t>0) {
	    a=t%10;
	    b+=pow(a,3);
	    t=t/10;
	}
	if (b==n)
		printf("%d is an Armstrong number",n);
	else
		printf("%d is not an Armstrong number",n);
	return 0;
}
```

| Input | Output                     |
| ----- | -------------------------- |
| 153   | 153 is an Armstrong number |

---

### 5.Đảo ngược của 1 số (Reverse of a number)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
	int n,t;
	int reverse=0;
	printf("Enter an integer : ");
	scanf("%d",&n);
	t=n;
	while(t!=0) {
	    reverse*=10;
	    reverse+=(t%10);
	    t/=10;
	}
	printf("Reverse of %d is = %d",n,reverse);
	return 0;
}
```

| Input | Output |
| ----- | ------ |
| 12345 | 54321  |

---

### 4.Tìm số chẳn hoặc lẻ (Find Even or Odd number)

Số chẳn là số chia hết cho 2, còn số lẻ thì không

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
	int n;
	printf("Enter number = ");
	scanf("%d",&n);
	if(n%2==0)
		printf("%d is Even number",n);
	else
		printf("%d is Odd number",n);
	return 0;
}
```

| Input | Output            |
| ----- | ----------------- |
| 10    | 10 is Even number |

---

### 5. Ước chung lớn nhất và bội chung nhỏ nhất (HCF & LCM)

HCF : (ước hcung lớn nhất): Là số nguyên lớn nhất là ước chung của a và b

LCM : (bội chung nhỏ nhất): là số nguyên nhỏ nhất chia hết cho cả a và b

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
	int num1,num2,a,b,t,gcd,lcm;
	printf("Enter number 1 : ");
	scanf("%d",&num1);
	printf("Enter number 2 : ");
	scanf("%d",&num2);
    a=num1;
    b=num2;
    while(b!=0) {
        t=b;
        b=a%b;
        a=t;
    }
    gcd = a;
    lcm = (a*b)/gcd;
    printf("Greatest common divisor of %d and %d = %d\n",num1,num2,gcd);
    printf("Least common multiple of %d and %d = %d\n",num1,num2,lcm);
	return 0;
}
```

| Input | Output               |
| ----- | -------------------- |
| 2 5   | GCD = 1 <br>LCD = 10 |

---

### 6.Hoán đổi 2 số (Swap two numbers)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
	int a,b,temp;
	printf("Enter number 1 : ");
	scanf("%d",&a);
	printf("Enter number 2 : ");
	scanf("%d",&b);
    temp=a;
    a = b;
    b = temp;
    printf("Number 1 = %d\n",a);
    printf("Number 2 = %d\n",b);
	return 0;
}
```

| Input | Output |
| ----- | ------ |
| 3 6   | 6 3    |

---

### 7.Kiểm tra chữ cái là nguyên âm (Check if Alphabet is Vowel)

có 5 chữ nguyên âm là : anh (a), ốm (o), em (e), ú (u), ì (i) và cả chữ viết hoa của chúng.

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
	char ch;
	printf("Enter a character : ");
	scanf("%c",&ch);
	if (ch=='a'||ch=='A'||ch=='O'||ch=='o'||ch=='E'||ch=='e'||ch=='U'||ch=='u'||ch=='I'||ch=='i')
		printf("%c is a Vowel.\n",ch);
	else	
		printf("%c is not a Vowel.\n",ch);	
	return 0;
}
```

| Input | Output        |
| ----- | ------------- |
| a     | a is a Vowel. |

---

### 8. Tổng các chữ số của 1 số (Sum Digits of a Number)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
	int n,t;
	int sum=0;
	printf("Enter an integer : ");
	scanf("%d",&n);
	t=n;
	while(t!=0) {
	    sum+=(t%10);
	    t/=10;
	}
	printf("Sum of digits of %d is %d",n,sum);
	return 0;
}
```

| Input | Output |
| ----- | ------ |
| 1234  | 10     |

---

### 9.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 10.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |
