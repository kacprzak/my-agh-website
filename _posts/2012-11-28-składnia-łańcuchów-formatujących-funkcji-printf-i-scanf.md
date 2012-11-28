Niektóre znaki formatujące w tych funkcjach są mało intuicyjne więc
oto mała ściągawka:

    +---------------+-------------+-------------+
    |Typ            |printf       |scanf        |
    +---------------+-------------+-------------+
    |char           |%c           |%c           |
    +---------------+-------------+-------------+
    |char*          |%s           |%s           |
    +---------------+-------------+-------------+
    |int            |%d lub %i    |%d lub %i    |
    +---------------+-------------+-------------+
    |unsigned int   |%u           |%u           |
    +---------------+-------------+-------------+
    |long           |%ld lub %li  |%ld lub %li  |
    +---------------+-------------+-------------+
    |unsigned long  |%lu          |%lu          |
    +---------------+-------------+-------------+
    |float          |%f           |%f           |
    +---------------+-------------+-------------+
    |double         |%f           |%lf          |
    +---------------+-------------+-------------+
    |void*          |%p           |%p           |
    +---------------+-------------+-------------+

Uwaga! Funkcja `scanf` tak naprawdę przyjmuje wskaźniki to typów z
tabelki. W funkcji `printf` `%f` spodziewa się double, a jeśli
przekazany zostanie `float` to jest niejawnie rzutowany na `double`.

#### Literatura:
* <http://www.cplusplus.com/reference/cstdio/printf/>
* <http://www.cplusplus.com/reference/cstdio/scanf/>
