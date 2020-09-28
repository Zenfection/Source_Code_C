# Ctype.h

## 1. Hàm `isalnum `

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

## 2. hàm `isalpha`

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

## 3. Hàm `iscntrl`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

## 4. Hàm `isdigit`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

## 5. Hàm `isgraph`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

## 6. Hàm `islower`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

## 7. Hàm `isprint`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

## 8. Hàm `ispunct`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

## 9. Hàm `isspace`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

## 10. Hàm `isupper`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

## 11. Hàm `isxdigit`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

## 12. Hàm `tolower`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---

## 13. Hàm `toupper`

```c

```

| Input | Output |
| ----- | ------ |
|       |        |

---