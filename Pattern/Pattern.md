# Pattern

## 1. Mẫu nhị phân (Binary Pattern)

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int n;
	printf("Enter n = ");scanf("%d",&n);
    int count = 1;
    for (int i = 1; i <= n; i++){
        for (int j = 1; j <= i; j++){
            printf("%d", count++ % 2);
            	if (j == i && i != n){
                	printf("\n");
            	}
        }
        if (i % 2 == 0)
            count = 1;
        else
            count = 0;
    }
	return 0;
}
```

| Input | Output                          |
| ----- | ------------------------------- |
| 5     | 1<br>01<br>101<br>0101<br>10101 |

---

## 2. Mẫu kim cương (Diamond Pattern)

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int n, space = 1;
    printf("Enter number of rows : ");
    scanf("%d", &n);
    space = n - 1;
    for (int k = 1; k <= n; k++){
        for (int c = 1; c <= space; c++){
            printf(" ");
        }
        space--;
        for (int c = 1; c <= 2 * k - 1; c++){
            printf("#");
        }
        printf("\n");
    }
    space = 1;
    for (int k = 1; k <= n - 1; k++){
        for (int c = 1; c <= space; c++){
            printf(" ");
        }
        space++;
        for (int c = 1; c <= 2 * (n - k) - 1; c++){
            printf("#");
        }
        printf("\n");
    }
	return 0;
}
```

| Input | Output                                                                            |
| ----- | --------------------------------------------------------------------------------- |
| 4     | <br>       #<br>     ###<br>  #####<br>#######<br>  #####<br>     ###<br>       # |

---

## 3. Mẫu số kim cương (Diamond of number Pattern)

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int n;
	printf("Enter number of rows : ");
	scanf("%d",&n);
    for (int i = 1; i <= n; i++){
        for (int j = i; j < n; j++){
            printf(" ");
        }
        for (int k = 1; k < (i*2); k++){
            printf("%d", i);
        }
        printf("\n");
    }
    for (int i = n-1; i >= 1; i--){
        for (int j = n; j > i; j--){
            printf(" ");
        }
        for (int k = 1; k < (i*2); k++){
            printf("%d", i);
        }
        printf("\n");
    }
	return 0;
}
```

| Input | Output                                                                        |
| ----- | ----------------------------------------------------------------------------- |
| 4     | <br>      1<br>    222<br>  33333<br>4444444<br>  33333<br>    222<br>      1 |

---

## 4. Mẫu sao kim cương

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int n;
	printf("Enter of number rows : ");
	scanf("%d",&n);
    for (int i = 1; i <= n; i++){
        for (int j = n; j > i; j--){
            printf(" ");
        }
        printf("*");
        for (int j = 1; j < (i-1) * 2; j++){
            printf(" ");
        }
        if (i == 1){
            printf("\n");
        }
        else
        printf("*\n");
    }
    for (int i = n-1; i >= 1; i--){
        for (int j = n; j > i; j--){
            printf(" ");
        }
        printf("*");
        for (int j = 1; j < (i-1)*2; j++){
            printf(" ");
        }
        if (i == 1)
            printf("\n");
        else
        	printf("*\n");
    }
	return 0;
}
```

| Input | Output                                                                                                                                                                                                                                        |
| ----- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 3     | <br>              #<br/>          #      #<br/>      #              #<br/>   #                     # <br/>#                            #<br/>   #                     #<br/>       #             #<br/>          #      #<br/>              # |

---

## 5.Tam giác Floyds (Floys Triangle)

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int n;
    printf("Enter the number of rows : ");
    scanf("%d",&n);
    int a=1;
    for (int i = 1; i <= n; i++) {
        for (int c = 1; c <= i; c++) {
            printf("%d ", a);
            a++;
        }
        printf("\n");
    }
	return 0;
}
```

| Input | Ouput                                                                |
| ----- | -------------------------------------------------------------------- |
| 6     | 1<br>2 3<br>4 5 6<br>7 8 9 10<br>11 12 13 14 15<br>16 17 18 19 20 21 |

---

## 6. Kim cương rỗng (Hollow Diamond)

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int n;
	printf("Enter number of rows : ");
	scanf("%d",&n);
    for (int i = 1; i <= n; i++){
        for (int j = 1; j <= n+1-i; j++){
            printf("*");
        }
        for (int k = 1; k < i; k++){
            printf("  ");
        }
        for (int j = 1; j <= n+1-i; j++){
            printf("*");
        }
        printf("\n");
    }
    
    for (int i = 2; i <= n; i++){
        for (int j = 1; j <= i; j++){
            printf("*");
        }
        for (int k = 1; k <= n-i; k++){
            printf("  ");
        }
        for (int j = 1; j <= i; j++){
            printf("*");
        }
        printf("\n");
    }
	return 0;
}
```

| Input | Ouput                                                                                                                                                                      |
| ----- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 5     | ##########<br>####     ####<br>###          ###<br>##               ##<br>#                    #<br>##               ##<br>###          ###<br>####     ####<br>########## |

---

## 7. Hình vuông rõng

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int n;
    printf("Enter value of n : ");
    scanf("%d", &n);
    printf("\n");
    for (int i = 1; i <= n; i++){
        for (int j = 1; j <= n; j++){
            if (i != 1 && i != n && j != 1 && j != n){
                printf(" ");
            }
            else{
                printf("*");
            }
        }
        printf("\n");
    }
	return 0;
}
```

| Input | Output                                                   |
| ----- | -------------------------------------------------------- |
| 5     | #####<br>#        #<br>#        #<br>#        #<br>##### |

---

## 8. Mẫu đồng hồ cát (Hourglass Pattern)

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int num, n;
    printf("Enter number of rows: ");
    scanf("%d", &num);
    printf("\n");
    n = num;
    for (int r = 1; r <= num; r++){
        for (int sp = 1; sp <= r; sp++){
            printf(" ");
        }
        for (int c = 1; c <= n; c++){
            printf("*");
        }
        for (int c = num-r; c >= 1; c--){
            printf("*");
        }
        n--;
        printf("\n");
    }

    for (int r = 2; r <= num; r++){
        for (int sp = num-r+1; sp >= 1; sp--){
            printf(" ");
        }
        for (int c = 1; c <= r; c++){
            printf("*");
        }
        for (int c = r - 1; c >= 1; c--){
            printf("*");
        }
        printf("\n");
    }
	return 0;
}
```

| Input | Output                                                                                                                            |
| ----- | --------------------------------------------------------------------------------------------------------------------------------- |
| 5     | ##########<br>  ########<br>      #####<br>         ###<br>           #<br>         ###<br>     #####<br>  ########<br>########## |

---

## 9. Mẫu số chữ cái (Number alphabet Pattern)

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int n;
    int i = 1;
    char ch = 'A';
    printf("Enter no. of rows : ");
    scanf("%d", &n);
    printf("\n");
    for (int r = 1; r <= n; r++){
        for (int c = 1; c <= r; c++){
            if (r % 2 == 0){
                printf(" %c", ch++);
            }
            else{
                printf(" %d", i++);
            }
        }
        printf("\n");
    }
	return 0;
}
```

| Input | Output                                                 |
| ----- | ------------------------------------------------------ |
| 6     | 1<br>A B<br>2 3 4<br>C D E F<br>5 6 7 8<br>G H I J K L |

---

## 10. Mẫu số kim cương (Number Diamond Pattern)

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int n;
	printf("Enter number of rows : ");
	scanf("%d",&n);
    for(int i = 1;i <= n;i++){
        for(int j = i;j < n;j++){
            printf(" ");
        }
        for(int k = 1;k < (i*2);k++){
                printf("%d",k);
        }
        printf("\n");
    }
    for(int i = n-1;i >= 1;i--){
        for(int j=n;j>i;j--){
                printf(" ");
        }
        for(int k = 1;k < (i*2);k++){
                printf("%d",k);
        }
        printf("\n");
    }
	return 0;
}
```

| Input | Output                                                                                                                |
| ----- | --------------------------------------------------------------------------------------------------------------------- |
| 5     | <br>        1<br>      123<br>    12345<br>  1234567<br>123456789<br>  1234567<br>    12345<br>      123<br>        1 |

---

## 11. Mẫu hình chữ nhật loại 1 (Rectangle Pattern 1)

```c
#include<stdio.h>
int main(int argc, char const *argv[]){
	int n;
    printf("Enter number of rows : ");
    scanf("%d", &n);
    printf("\n");
    int r=1;
    for (; n >= 1; n--, r++){
        for (int c = 1; c <= n; c++){
            printf("%d", c);
        }
        for (int sp = r; sp > 1; sp--){
            printf("_");
        }
        for (int sp = r; sp > 1; sp--){
            printf("_");
        }
        for (int c = n; c >= 1; c--){
            printf("%d", c);
        }
        printf("\n");
    }
	return 0;
}
```

| Input | Output                                                                   |
| ----- | ------------------------------------------------------------------------ |
| 5     | 1234554321<br>1234 __4321<br>123_____321<br>12 _______21<br>1__________1 |

---

## 12. Mẫu số loại 1 (Number Pattern 1)

## 13. Mẫu số loại 2 (Number Pattern 2)

## 14. Mẫu số loại 3 (Number Pattern 3)

## 15. Mẫu số loại 4 (Number Pattern 4)

## 16. Kim tự tháp số (Number Pyramid)

## 17.Tam giác pascal không sử dụng hàm riêng (Pascal's Triangle Without Using Function)

## 18. Mẫu loại 1 (Pattern 1)

## 19. Mẫu loại 2 (Pattern 2)

## 20. Mẫu loại 3 (Pattern 3)

## 21. Mẫu loại 4 (Pattern 4)

## 22. Mẫu loại 5 (Pattern 5)

## 23. Mẫu loại 6 (Pattern 6)

## 24. Mẫu loại 7 (Pattern 7)

## 25. Mẫu loại 8 (Pattern 8)

## 26. Mẫu loại 9 (Pattern 9)

## 27. Mẫu loại 10 `(Pattern 10)`

## 28. Kim tự tháp (Pyramid)

## 29.
