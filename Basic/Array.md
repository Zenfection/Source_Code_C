### 1. Xoá phần tử từ mảng (Delete element from Array)

```c
#include <stdio.h>
void input_array(int M[],int n);
void delete_array(int M[],int n,int x);
int main(int argc, char const *argv[]){
    int n,x;
    printf("Enter the number of elements = ");
    scanf("%d",&n);
    int M[n];
    input_array(M,n);
    printf("Enter number position you want delete : ");
    scanf("%d",&x);
    delete_array(M,n,x);
    return 0;
}
void input_array(int M[],int n){
    for (int i = 0; i < n; i++){
        scanf("%d",&M[i]);
    }
}
void delete_array(int M[],int n,int x){
    if(x>=n+1)
        printf("Deletion not possible");
    else{
        for (int i = x-1; i < n-1; i++){
            M[i]=M[i+1];
        }
    }
    printf("Array after delete : ");
    for (int i = 0; i < n-1; i++){
        printf("%d ",M[i]);
    }
}
```

| Input                | Output |
| -------------------- | ------ |
| n=3<br>2 44 5<br>x=5 | 2 44   |

---

### 2.Phần tử lớn nhất và nhỏ nhất trong mảng (Maxium and Minimum number is an Array)

```c
#include <stdio.h>
void input_array(int M[],int n);
int max_array(int M[],int n);
int min_array(int M[],int n);
int main(int argc, char const *argv[]){
    int n;
    printf("Enter the number of elements = ");
    scanf("%d",&n);
    int M[n];
    input_array(M,n);
    int min=M[0],max=M[0],lo_min,lo_max;
    for (int i = 1; i < n; i++){
        if(max<M[i]){
            max=M[i];
            lo_max=i+1;
        }
        if(min>M[i]){
            min=M[i];
            lo_min=i+1;
        }
    }
    printf("Maximum number at locate %d, it's value = %d\n",lo_max,max);
    printf("Minimum number at locate %d, it's value = %d\n",lo_min,min);
    return 0;
}
void input_array(int M[],int n){
    for (int i = 0; i < n; i++){
        scanf("%d",&M[i]);
    }
}
```

| Input           | Output                                    |
| --------------- | ----------------------------------------- |
| 4<br>4  9 53  6 | Min: locate 1 is 4<br>Max: locate 3 is 53 |

---

### 3.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 4.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 5.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 6.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 7.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 8.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

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

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

v

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 1.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |


