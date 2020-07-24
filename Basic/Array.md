### 1. Xoá phần tử trong mảng (Delete element from Array)

```c
#include <stdio.h>
void input_array(int M[],int n);
void delete_array(int M[],int n,int pos);
int main(int argc, char const *argv[]){
    int n,pos;
    printf("Enter the number of elements = ");
    scanf("%d",&n);
    int M[n];
    input_array(M,n);
    printf("Enter number position you want delete : ");
    scanf("%d",&pos);
    delete_array(M,n,pos);
    return 0;
}
void input_array(int M[],int n){
    for (int i = 0; i < n; i++){
        scanf("%d",&M[i]);
    }
}
void delete_array(int M[],int n,int pos){
    if(pos>=n+1)
        printf("Deletion not possible");
    else{
        for (int i = pos-1; i < n-1; i++){
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
    printf("Enter %d numbers : \n",n);
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

### 3.Đảo ngược mảng

```c
#include <stdio.h>
void input_array(int M[],int n);
void reserve_array(int M[],int N[],int n);
int main(int argc, char const *argv[]){
    int n;
    printf("Enter the number of elements = ");
    scanf("%d",&n);
    int M[n],N[n];
    printf("Enter %d numbers : \n",n);
    input_array(M,n);
    reserve_array(M,N,n);
    printf("Reverse array is : ");
    for (int i = 0; i < n; i++){
        printf("%d ",N[i]);
    }
    return 0;
}
void input_array(int M[],int n){
    for (int i = 0; i < n; i++){
        scanf("%d",&M[i]);
    }
}
void reserve_array(int M[],int N[],int n){
    for (int i = 0; i < n; i++){
        N[n-i-1]=M[i];
    }
}
```

| Input      | Output |
| ---------- | ------ |
| 3<br>1 2 3 | 3 2 1  |

---

### 4. Tổng các số âm, tổng các số dương, trung bình các số trong mảng (Sum of negative & positive and Average on Array)

```c
#include <stdio.h>
void input_array(int M[],int n);
int main(int argc, char const *argv[]){
    int n;
    printf("Enter the number of elements = ");
    scanf("%d",&n);
    int M[n];
    printf("Enter %d numbers : \n",n);
    input_array(M,n);
    int sum_negative=0,sum_positive=0;
    for (int i = 0; i < n; i++){
        if(M[i]<0)
            sum_negative+=M[i];
        else
            sum_positive+=M[i];
    }
    float average = (sum_positive+sum_negative)*1.0/n;
    printf("Sum of negative numbers = %d\n",sum_negative);
    printf("Sum of positive numbers = %d\n",sum_positive);
    printf("Average of all input numbers = %f\n",average);
    return 0;
}
void input_array(int M[],int n){
    for (int i = 0; i < n; i++){
        scanf("%d",&M[i]);
    }
}
```

| Input          | Output                                                         |
| -------------- | -------------------------------------------------------------- |
| 4<br>4 -7 -2 6 | sum of negative = -9<br>sum of positive = 10<br>Average = 0.25 |

---

### 5.Xoá số đã cho trong mảng (Delete given number from Array)

```c
#include <stdio.h>
void input_array(int M[],int n);
void delete_array(int M[],int n,int pos);
int main(int argc, char const *argv[]){
    int n,x;
    printf("Enter the number of elements = ");
    scanf("%d",&n);
    int M[n];
    printf("Enter %d numbers : \n",n);
    input_array(M,n);
    printf("Enter number you want delete on Array = ");
    scanf("%d",&x);
    int found=0;
    for (int i = 0; i < n; i++){
        if(M[i]==x){
            found++;
            delete_array(M,n,i);
        }  
    }
    for (int i = 0; i < n-found; i++){
        printf("%d ",M[i]);
    }
    return 0;
}
void input_array(int M[],int n){
    for (int i = 0; i < n; i++){
        scanf("%d",&M[i]);
    }
}
void delete_array(int M[],int n,int pos){
    if(pos>=n+1)
        printf("Deletion not possible");
    else{
        for (int i = pos; i < n-1; i++){
            M[i]=M[i+1];
        }
    }
}
```

| Input               | Output  |
| ------------------- | ------- |
| 5<br>1 7 6 8 4<br>8 | 1 7 6 4 |

---

### 6. Thực hiện bảng hàng đợi dùng mảng (Implement a queue using Array)

```c
#include <stdio.h>
#include <stdlib.h>

int rear=-1;
int front=-1;
int M[1000];

void insert();
void display();
void deleteElement();
int main(int argc, char const *argv[]){
    int choice;
    printf("1.Insert element to queue \n");
    printf("2.Delete element from queue \n");
    printf("3.Display all elements of queue \n");
    printf("4.Quit \n");
    while (1){
        printf("Enter your choice : ");
        scanf("%d",&choice);
        switch (choice){
            case 1:insert();break;
            case 2:deleteElement();break;
            case 3:display();break;
            case 4:exit(1);
            default:
                printf("Wrong choice \n");
        }
    }
    return 0;
}
void insert(){
    int item;
    if (front==-1){
        front=0;
    }
    printf("Enter the number you want insert : ");
    scanf("%d",&item);
    rear+=1;
    M[rear]=item;
}
void deleteElement(){
    if (front == -1 || front > rear){
        printf("Queue Underflow \n");
        return;
    }
    else{
        printf("Element deleted from queue is : %d\n", M[front]);
        front = front + 1;
    }
    printf("Delete Successful!\n");
}
void display(){
    if(front==-1)
        printf("Queue is empty");
    else{
        for (int i = front; i <= rear; i++){
            printf("Number %d = %d\n",i+1,M[i]);
        }
    }
}

```

---

### 7. In phần tử xen kẻ trong mảng (Print Alternate Elements)

```c

```

| Input                            | Output        |
| -------------------------------- | ------------- |
| 10<br>1 4 55 66 22 0 76 11 23 78 | 1 55 22 76 23 |

---

### 8.Sắp xếp tăng dần và  giảm dần trong mảng  (Sort Array in Ascecding&Descending Order)

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

### 11.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 12.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 13.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 14.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 15.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 16.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 17.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 18.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 19.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 20.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 21.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 22.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 23.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 24.

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

### 25.

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


