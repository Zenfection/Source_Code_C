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

Hàm **trả về giá trị khác 0** nếu *đối số* là một [**ký tự điều khiển**](https://daynhauhoc.com/t/wiki-cac-ky-tu-dieu-khien-va-ky-tu-dac-biet-trong-c-c/2295). Nếu không, **hàm trả về 0**

```c
#include <stdio.h>
#include <ctype.h>
int main(int argc, char const *argv[]){
   int i = 0, j = 0;
   char str1[] = "Learn \a code \t programing";
   char str2[] = "by \n Zen";
   // in chuỗi tới khi gặp ký tự \a
   while(!iscntrl(str1[i])) {
      putchar(str1[i]);
      i++;
   }
   // in chuỗi cho tới khi gặp ký tự \n
   while(!iscntrl(str2[j])) {
      putchar(str2[j]);
      j++;
   }
   return 0;
}
```

| Input | Output   |
| ----- | -------- |
| none  | Learn by |

---

## 4. Hàm `isdigit`

Hàm này **kiểm tra** xem ký tự đã truyền có phải là **chữ số thập phân** không

```c
#include <stdio.h>
#include <ctype.h>
int main(int argc, char const *argv[]){
   char c1;
   printf("Enter the character : ");
   c1=getchar();
   if (isdigit(c1))
      printf("|%c| is digit",c1);
   else
      printf("|%c| is not digit",c1);
   return 0;
}
```

| Input  | Output                              |
| ------ | ----------------------------------- |
| h<br>2 | |h\| is digit<br>\|2\| is not digit |

---

## 5. Hàm `isgraph`

Hàm **trả về giá trị khác 0** nếu *đối số* là một **ký tự graphical** (*có thể nhìn thấy*). Nếu không, **hàm trả về 0**.

```c
#include <stdio.h>
#include <ctype.h>
int main(int argc, char const *argv[]){
   int var;
   printf("Enter the character : ");
   var=getchar();
   if (isgraph(var))
      printf("|%c| can be printed",var);
   else
      printf("|%c| can't be printed",var);
   return 0;
}
```

| Input          | Output                                                                 |
| -------------- | ---------------------------------------------------------------------- |
| 3<br>h<br>'  ' | |3\| can be printed<br>\|h\| can be printed<br>\|  \| can't be printed |

---

## 6. Hàm `islower`

```c
#include <stdio.h>
#include <ctype.h>
int main(int argc, char const *argv[]){
   char var;
   printf("Enter the character : ");
   var=getchar();
   if (islower(var))
      printf("|%c| is lowercase character",var);
   else
      printf("|%c| is not lowercase character",var);
   return 0;
}
```

| Input       | Output                                                                                              |
| ----------- | --------------------------------------------------------------------------------------------------- |
| a<br>Q<br>3 | |a\| is lowercase character<br>\|Q\| is not lowercase character<br>\|3\| is not lowercase character |

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