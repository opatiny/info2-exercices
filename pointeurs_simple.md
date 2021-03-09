## Les pointeurs

### Ex 1

Les variables suivantes sont déclarées :

```C
int val_i = 12;
double val_d = 2.34;
char val_c = 'a';

int* pi = NULL;
int* pi1 = NULL;
double* pd = NULL;
char* pc = NULL;
```
Emplacement des variables dans la mémoire

Variable | Adresse | Valeur
---|---|---
val_i | 10 | 12
val_d | 11 | 2.34
val_c | 12 | 'a'
pi | 20 | 0
pi1 | 21 |0
pd | 22 | 0
pc | 23 | 0

Donner la valeur des variables pour chaque point ci-dessous, vous pouvez
représenter le résultat avec un tableau comme celui-ci.

N'oubliez pas d'inscrire aussi la valeur des pointeurs

Variable | Adresse | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
---|---|---|---|---|---|---|---|---|---|---
val_i | 10 | 12
val_d | 11 | 2.34
val_c | 12 | 'a'
pi | 20 | 0
pi1 | 21 | 0
pd | 21 | 0
pc | 22 | 0
*pi | x | x
*pi1 | x | x
*pd | x | x
*pc | x | x

#### Point 1
```C
val_i = 10;
pi = &val_i;
```

#### Point 2
```C
val_i = 10;
val_d = 0.123;
pi = &val_i;
pd = &val_d;
val_i = 5;
```

#### Point 3
```C
val_c = 'a';
val_i = 2;
pc = &val_c;
*pc += val_i;
```

#### Point 4
```C
val_c = 4;
pc = &val_c;
pi = &val_c;
*pi = 6;
```

#### Point 5
```C
val_i = 3;
val_d = 2.3;
pi = &val_i;
pd = &val_d;
val_i = *pd;
pi = NULL;
```

#### Point 6
```C
val_i = 3;
pi = &val_i;
pi1 = &val_i;
*pi = 6;
```

#### Point 7
```C
val_i = 6;
pi = &val_i;
pi1 = &val_i;
*pi1 = 6;
pi1 = NULL;
val_i = 2;
```

#### Point 8
```C
val_i = 1;
pi1 = &val_i;
(*pi1)++;
val_i++;
pi = pi1;
```

#### Point 9
```C
val_c = 5;
val_i = 3;
pi1 = &val_i;
(*pi1)++;
val_i++;
pi = pi1;
pc = &val_c;
*pi = *pc;
```