# Ctype.h

## 1. Ví dụ hàm isalnum (isalnum() example)

Hàm **void isalnum(int c)** kiểm tra xem ký tự đã truyền có phải là **ký tự - số** hay không.

```c
#include <stdio.h>
#include <ctype.h>
int main(int argc, char const *argv[]){
       char c;
       printf("Enter any key : ");
       c=getchar();
       if (isalnum(c)){
           printf("%c is an alphanumeric",c);
       }
       else{
           printf("%c is not an alphanumeric",c);
       }
    return 0;
}
```

| Input               | Output                                                                                       |
| ------------------- | -------------------------------------------------------------------------------------------- |
| 2<br>d<br>\t<br>" " | is an alphanumeric<br>is an alphanumeric<br>is not an alphanumeric<br>is not an alphanumeric |

---

## 2. Ví dụ hàm isalpha (isalpha() example)

Hàm **void isalnum(int c)** kiểm tra xem ký tự đã truyền có phải là **ký tự** hay không

```c
#include <stdio.h>
#include <ctype.h>
int main(int argc, char const *argv[]){
       char c;
       printf("Enter any key : ");
       c=getchar();
       if (isalnum(c)){
           printf("is an alphabet");
       }
       else{
           printf("is not an alphabet");
       }
    return 0;
}
```

| Input               | Output                                                                        |
| ------------------- | ----------------------------------------------------------------------------- |
| 2<br>d<br>\t<br>" " | is an alphabet<br>is an alphabet<br>is not an alphanbet<br>is not an alphabet |
