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

| [Chạy thử](https://repl.it/@Zenfection/perfect-number) |
| ------------------------------------------------------ |

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

| [Chạy thử](https://repl.it/join/xvvjdxat-zenfection) |
| ---------------------------------------------------- |

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

**Ví dụ**: ![](https://latex.codecogs.com/gif.latex?3%5E3&plus;7%5E3&plus;1%5E3%3D371)

```c
#include <stdio.h>
#include <math.h>
int count_digit(int n);
int main(int argc, char const *argv[]){
    int a,n,b=0,t;
    printf("Enter an integer : ");
    scanf("%d",&n);
    t=n;
    while(t>0) {
        a=t%10;
        b+=pow(a,count_digit(n));
        t/=10;
    }
    if (b==n)
        printf("%d is an Armstrong number",n);
    else
        printf("%d is not an Armstrong number",n);
    return 0;
}
int count_digit(int n){
    int count=0;
    while(n!=0) {
        n/=10;
        count++;
    }
    return count;
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

### 4.Tìm số chẵn hoặc lẻ (Find Even or Odd number)

Số chẵn là số chia hết cho 2, còn số lẻ thì không

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

HCF : (ước chung lớn nhất): Là số nguyên lớn nhất là ước chung của a và b

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

### 9. Tổng các chữ số của 1 số sử dụng Đệ quy (Sum Digits of a number using recursion)

```c
#include <stdio.h>
int sum_digits(int n);
int main(int argc, char const *argv[]){
    int n;
    printf("Enter an integer : ");
    scanf("%d",&n);
    printf("Sum digits of %d is %d",n,sum_digits(n));
    return 0;
}
int sum_digits(int n){
    static int sum=0;
    if(n==0)
        return 0;
    sum=(n%10)+sum_digits(n/10);
    return sum;
}
```

| Input | Output |
| ----- | ------ |
| 123   | 6      |

---

### 10. In n số nguyên tố đầu tiên (Print Primes till 'n')

Số nguyên tố là số chia hết cho 1 và chính nó => bắt đầu từ 2

```c
#include <stdio.h>
#include <math.h>
int check_prime(int n);
int main(int argc, char const *argv[]){
    int n;
    printf("Enter number of prime numbers : ");
    scanf("%d",&n);
    int count=0;
    int i=2;
    printf("Frist %d prime numbers are : ",n);
    while(count < n){
        if(check_prime(i)){
            printf("%d ",i);
            count++;
        }
        i++;
    }
    return 0;
}
int check_prime(int n){
    if(n<2)
        return 0;
    else{
        for (int i = 2; i <= sqrt(n); i++)
            if(n%i==0)
                return 0;
    }
    return 1;
}
```

| Input | Output       |
| ----- | ------------ |
| 6     | 2 3 5 7 9 11 |

---

### 11. Thêm n số và tính tổng nó (Add 'n' numbers and Sum)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int n;
    int sum=0;
    printf("Enter an integer you want add : ");
    scanf("%d",&n);
    printf("Enter %d integers number : ",n);
    for (int i = 1; i <= n; i++){
        int value;
        scanf("%d",&value);
        sum+=value;
    }
    printf("Sum of entered number =  %d",sum);
    return 0;
}
```

| Input        | Output |
| ------------ | ------ |
| 4<br>1 2 3 4 | 10     |

---

### 12.Thêm n số và tính tổng nó bằng Mảng (Add 'n' numbers and Sum using Array)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int n;
    int sum=0;
    printf("Enter an integer you want add : ");
    scanf("%d",&n);
    int M[n];
    printf("Enter %d integers number : ",n);
    for (int i = 0; i < n; i++){
        scanf("%d",&M[i]);
        sum+=M[i];
    }
    printf("Sum of entered numbers = %d",sum);
    return 0;
}
```

| Input        | Output |
| ------------ | ------ |
| 4<br>5 6 7 8 | 26     |

---

### 13. Kiểm tra số nguyên tố (Check prime number)

```c
#include <stdio.h>
#include <math.h>
int check_prime(int n);
int main(int argc, char const *argv[]){
    int n;
    printf("Enter an integer you want check : ");
    scanf("%d",&n);
    if(check_prime(n))
        printf("%d is a prime number",n);
    else
        printf("%d is not a prime number",n);
    return 0;
}
int check_prime(int n){
    if(n<2) return 0;
    else{
        for (int i = 2; i <= sqrt(n); i++){
            if(n%i==0)
                return 0;
        }
    }
    return 1;
}
```

| Input | Output              |
| ----- | ------------------- |
| 7     | 7 is a prime number |

---

### 14. Kiểm tra số đối xứng (Check Palinedrome)

**Palindrome** là số mà viết ngược hay xuôi vẫn là nó, hiểu là **số đối xứng** cũng được

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int n,temp;
    int reserve=0;
    printf("Enter an integer you want check : ");
    scanf("%d",&n);
    temp=n;
    while(temp!=0) {
        reserve*=10;
        reserve+=(temp%10);
        temp/=10;
    }
    if(reserve==n)
        printf("%d is a palindrome number",n);
    else
        printf("%d is not a palindrome number",n);
    return 0;
}
```

| Input | Output                       |
| ----- | ---------------------------- |
| 12321 | 12321 is a palindrone number |

---

### 15. Hoán vị 2 số bằng xor (Swap two number using bitwise xor)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    long a, b;
    printf("Enter number 1 : ");
    scanf("%ld",&a);
    printf("Enter number 2 : ");
    scanf("%ld",&b);
    a^=b; 
    b^=a; 
    a^=b;
    printf("Number 1 : %ld\n",a);
    printf("Number 2 : %ld\n",b);
    return 0;
}
```

| Input | Output |
| ----- | ------ |
| 5 3   | 3 5    |

---

### 16. In bình phương 1 tới n (Calculate Square till 'n' number)

```c
#include <stdio.h>
#include <math.h>
int main(int argc, char const *argv[]){
    int n;
    printf("Enter the range : ");
    scanf("%d",&n);
    for (int i = 1; i <= n; i++){
        int square=pow(i,2);
        printf("Square of %d is %d\n",n,square);
    }
    return 0;
}
```

| Input | Output      |
| ----- | ----------- |
| 5     | 1 4 9 16 25 |

---

### 17. Hệ số của 1 số (Factors of Number)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int n;
    printf("Enter an integer : ");
    scanf("%d",&n);
    printf("Factors of %d are : ",n);
    for (int i = 1; i <= n; i++){
        if(n%i==0){
            printf("%d ",i);
        }
    }
    return 0;
}
```

| Input | Output    |
| ----- | --------- |
| 26    | 1 2 13 26 |

---

### 18.Số neon (Neon number)

**Số neon** là số mà **tổng các chữ số trong bình phương của nó bằng chính nó**:

Ví dụ: $9^2=81 , 8+1=9$

```c
#include <stdio.h>
#include <math.h>
int main(int argc, char const *argv[]){
    int n,sum=0;
    printf("Enter number you want check : ");
    scanf("%d",&n);
    int square = pow(n,2);
    while(square!=0) {
        sum+=(square%10);
        square/=10;
    }
    if(sum==n)
        printf("%d is a neon number",n);
    else
        printf("%d is not a neon number",n);
    return 0;
}
```

| Input | Output           |
| ----- | ---------------- |
| 9     | 9 is neon number |

---

### 19. (Sine series)

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 20. In 5 số tiếp theo (Next 5 successive numbers)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int n;
    printf("Enter an integer : ");
    scanf("%d",&n);
    printf("Successive Numbers from %d: ",n);
    for (int i = n+1; i <= n+5; i++){
        printf("%d ",i);
    }
    return 0;
}
```

| Input | Output     |
| ----- | ---------- |
| 5     | 6 7 8 9 10 |

---

### 21. Tổng của các bình phương tới n (Sum of Squares till 'n')

```c
#include <stdio.h>
#include <math.h>
int main(int argc, char const *argv[]){
    int n,sum=0;
    printf("Enter an integer : ");
    scanf("%d",&n);
    for (int i = 1; i <= n; i++){
        sum+=pow(i,2);
    }
    printf("Sum of Squares till %d : %d",n,sum);
    return 0;
}
```

| Input | Output |
| ----- | ------ |
| 5     | 55     |

---

### 22. Số lớn nhất trong 3 số sử dụng toán tử ? (Largest among 3 number using ternary operator)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int a, b, c, big;
    printf("Enter 3 numbers: ");
    scanf("%d %d %d", &a, &b, &c);
    big = (a > b && a > c ? a : b > c ? b : c);
    printf("The biggest number is: %d", big);
    return 0;
}
```

| Input | Output |
| ----- | ------ |
| 5 8 4 | 8      |

---

### 23. Hoán vị 2 số sử dụng con trỏ (Swap two number using Pointer)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int a,b;
    printf("Enter number 1 : ");
    scanf("%d",&a);
    printf("Enter number 2 : ");
    scanf("%d",&b);
    int *ptr1,*ptr2,*temp;
    ptr1=&a;
    ptr2=&b;
    temp=ptr1;
    ptr1=ptr2;
    ptr2=temp;
    printf("Number 1 = %d\n",*ptr1);
    printf("Number 2 = %d\n",*ptr2);
    return 0;
}
```

| Input | Output |
| ----- | ------ |
| 3 5   | 5 3    |

---

### 24. Tính tổng n số (Sum of n number)

```c
#include <stdio.h>
int main(int argc, char const *argv[]){
    int n,sum=0;
    printf("Enter an integer you want add : ");
    scanf("%d",&n);
    int M[n];
    printf("Enter %d numbers : ",n);
    for (int i = 0; i < n; i++){
        scanf("%d",&M[i]);
        sum+=M[i];
    }
    printf("Sum of %d numbers are = %d",n,sum);
    return 0;
}
```

| Input           | Output |
| --------------- | ------ |
| 5 <br>1 6 7 4 2 | 20     |

---

### 25. In Armtrong từ tới n (Armtrong numbers till 'n')

```c
#include <stdio.h>
#include <math.h>
int count_digit(int n);
int check_armtrong(int n);
int main(int argc, char const *argv[]){
    int n;
    printf("Enter an integer : ");
    scanf("%d",&n);
    printf("Armtrong numbers from 1 to %d : 1 ",n);
    for(int i=100;i<=n;i++){
        if(check_armtrong(i))
            printf("%d ",i);
    }
    return 0;
}
int count_digit(int n){
    int count=0;
    while(n!=0) {
        n/=10;
        count++;
    }
    return count;
}
int check_armtrong(int n){
    int a,b=0,t;
    t=n;
    int count=count_digit(n);
    if(count<2)
        return 0;
    else{
    while(t>0){
        a=t%10;
        b+=pow(a,count_digit(n));
        t/=10;
    }
}
    if(b==n)
        return 1;
    return 0;
}
```

| Input | Output            |
| ----- | ----------------- |
| 500   | 1 153 370 371 407 |

---

### 26. Kiểm tra 2 số  là số thân thiện (Check whether two numbers are Amicable number )

**Số thân thiện** là số **2 hay nhiều số tự nhiên** nếu chúng có chung tỷ lệ giữa tổng các ước số của một số chia cho chính số đó

**Ví dụ:**

$\frac{∂(30)}{30}=\frac{1+2+3+5+6+10+15+30}{30}=\frac{12}{5}$

$\frac{∂(140)}{140}=\frac{1+2+4+5+7+10+14+20+28+35+70+140}{140}=\frac{12}{5}$

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 27.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 28.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 29.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 30.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 31.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---
