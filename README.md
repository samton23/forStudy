#### Задача 1

Реализовать функцию.

[Условие](https://kispython.ru/docs/0/%D0%98%D0%9D%D0%91%D0%9E-11-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

```python
import math


def main(y, z, x):
    a = (y ** 2 + z ** 3 / 56 + 61 * x) ** 6 / 69
    b = 17 * x ** 2 + math.log((y ** 3 - 54 * z - 0.01), 2) ** 3
    c = math.exp(x ** 2 - 77 * y) - z ** 8
    d = 59 * (72 * x - 68 * y ** 3 - 1) ** 2 - 27 * z ** 4
    return a / b - c / d
```

#### Задача 2

Реализовать кусочную функцию.

[Условие](https://kispython.ru/docs/1/%D0%98%D0%9D%D0%91%D0%9E-07-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

```python
from math import floor, pow


def main(z):
    if z < -17:
        b = 67 + 18 * (1 + 41 * z ** 2 + z)
    elif -17 <= z < 25:
        b = (z - 44 * z ** 3) / 78 + floor(z) ** 5
    elif 25 <= z < 110:
        b = pow(z, 3) / 78 - 73 - z ** 2 / 84
    elif 110 <= z < 151:
        b = 15 * pow(z, 7) - (z / 62 + z ** 3) ** 3
    else:
        a = (z / 63 + z ** 2 / 59 + 53 * z ** 3) ** 7
        b = z ** 3 + (70 * z ** 3 + 0.02) ** 6 + a
    return b
```

#### Задача 3

Реализовать итерационную функцию.

<img src="https://user-images.githubusercontent.com/6759207/169617721-bd496f38-2f08-47e3-8ab4-3a4d193272b6.png" width="500" />

[Условие](https://kispython.ru/docs/2/%D0%98%D0%9D%D0%91%D0%9E-07-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

```python
def main(n, m, b):
    summa = 0
    for j in range(1, b + 1):
        for k in range(1, m + 1):
            for i in range(1, n + 1):
                a = 57 * j ** 6
                b = 12 * (k ** 2 / 69 - 46 - i / 22) ** 2
                c = k ** 3
                summa += (a - b - c)
    return summa
```

#### Задача 4

Реализовать функцию по рекуррентной формуле.

[Условие](https://kispython.ru/docs/3/%D0%98%D0%9D%D0%91%D0%9E-07-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

```python
import math


def main(n):
    x = 0.26
    y = -0.17
    for i in range(n - 1):
        v = y - math.ceil(x) ** 2
        x = y
        y = v
    return y
```

#### Задача 5

Реализовать функцию, оперирующую векторами длины n.

[Условие](https://kispython.ru/docs/4/%D0%98%D0%9D%D0%91%D0%9E-11-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

```python
import math


def main(y, z):
    sum = 0
    n = len(y)
    y = [0] + y
    z = [0] + z
    for i in range(1, n + 1):
        a = (y[n + 1 - i] ** 3)
        b = (-18 * z[n + 1 - math.ceil(i / 2)] - 71)
        sum += 96 * (a + b) ** 2
    return 86 * sum
```

#### Задача 6

Реализовать функцию для вычисления дерева решений.

[Условие](https://kispython.ru/docs/5/%D0%98%D0%9D%D0%91%D0%9E-11-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

```python
def grace_lua(x, left, middle, right):
    if x[1] == 'GRACE':
        return left
    if x[1] == 'LUA':
        return middle
    return right


def bro(x, left, right):
    if x[0] == 'BRO':
        return left
    return right


def four(x, left, middle, right):
    if x[4] == 1978:
        return left
    if x[4] == 2006:
        return middle
    return right


def main(x):
    if x[3] == 2015:
        if x[2] == 'UNO':
            return grace_lua(x, bro(x, 0, 1), four(x, 2, 3, 4), bro(x, 5, 6))
        if x[2] == 'BRO':
            return four(x, grace_lua(x, 7, 8, 9), 10, 11)
    if x[3] == 1983:
        return 12
    return 13
```

#### Задача 7

Реализовать функцию для преобразования битовых полей.

> Для генерации [битовых масок](https://jakevdp.github.io/WhirlwindTourOfPython/04-semantics-operators.html#Bitwise-Operations) может быть полезно написать функцию `generate_mark(begin, end)`.

[Условие](https://kispython.ru/docs/6/%D0%98%D0%9D%D0%91%D0%9E-11-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

```python
def main(s):
    i = int(s)
    c1 = 0b1111111 & i
    c2 = 0b1111111111 & (i >> 7)
    c3 = 0b11 & (i >> 17)
    c5 = 0b111111111 & (i >> 27)
    return tuple(map(str, (c1, c2, c3, c5)))
```

#### Задача 8

Реализовать функцию для разбора строки, содержащей данные в текстовом формате.

> Для отладки [регулярных выражений](https://docs.python.org/3/library/re.html) можно воспользоваться сервисом [regexr.com](http://regexr.com) или [regex101.com](https://regex101.com/)

[Условие](https://kispython.ru/docs/7/%D0%98%D0%9D%D0%91%D0%9E-11-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

```python
import re


def main(x):
    r = r"\[\[\s*variable\s*list\(\s*([^)]*)\)\s*=>\s*([^.]*)"
    z = re.findall(r, x)
    ls2 = []
    for ints, key in z:
        ls = []
        for i in ints.split():
            if i == ".":
                continue
            ls.append(int(i))
        p = (key, ls)
        ls2.append(p)
    return ls2
```

#### Задача 9

Реализовать функцию преобразования табличных данных.

[Условие](https://kispython.ru/docs/8/%D0%98%D0%9D%D0%91%D0%9E-11-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

Способ решения 1

```python
def remove_none(x):
    res = []
    for row in x:
        if row[0] is None:
            continue
        temp = []
        for cell in row:
            if cell is None:
                continue
            temp.append(cell)
        res.append(temp)
    return res


def remove_duplicates(x):
    output = []
    control = set()
    for row in x:
        if row[0] in control:
            continue
        control.add(row[0])
        output.append(row)
    return output


def formatt(res):
    for row in res:
        row[0] = row[0].split()[1]
        row[1] = row[1].replace('/', '.')[2:]
        row[2] = row[2].replace('N', '0').replace('Y', '1')
        s = row[3]
        row[3] = s[3:6] + '-' + s[6:]
    return res


def transpose(A):
    C = []
    for i in range(len(A[0])):
        ci = []
        for j in range(len(A)):
            a = A[j][i]
            ci.append(a)
        C.append(ci)
    return (C)


def main(x):
    res = remove_none(x)
    res = remove_duplicates(res)
    res = formatt(res)
    res = transpose(res)
    return res
```

Способ решения 2

```python
def main(x):
    res = filter(len, map(lambda row: list(filter(bool, row)), x))
    res = map(list, dict.fromkeys(map(tuple, res)))
    res = [[name.split()[1],
            date.replace('/', '.')[2:], 
            str('NY'.index(bol)),
            f'{tel[3:6]}-{tel[6:]}'] for name, date, bol, tel in res]
    res = list(map(list, zip(*res)))
    return res
```

#### Задача 10

Реализовать конечный автомат Мили в виде класса.

> По условию задачи помимо функции `main`, возвращающей экземпляр класса, необходимо написать функцию `test`, тестирующую конечный автомат, причём степень покрытия кода тестами должна быть равна 100%. Для определения непокрытых тестами ветвей рекомендуется установить утилиту `coverage` командой `pip install coverage pytest`, визуализировать [процент покрытия кода тестами](https://github.com/true-grue/kispython/blob/main/lect5.ipynb) для файла `code.py`, содержащего текст Вашей программы, командами `coverage run --branch -m pytest code.py`, `coverage report`, `coverage html`. После выполнения команды `coverage html` перейдите в папку `htmlcov` и откройте в браузере файл `index.html`.

[Условие](https://kispython.ru/docs/9/%D0%98%D0%9D%D0%91%D0%9E-07-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

[Видео-инструкция](https://user-images.githubusercontent.com/6759207/235297961-189a7032-a570-4a46-81a4-d095fa7da661.mp4) по оценке покрытия кода тестами:

> Для управления зависимостями в видео-инструкции используется [poetry](https://github.com/python-poetry/poetry), надстройка над [pip](https://pypi.org/project/pip/). Использование `poetry` не является обязательным, достаточно выполнить `pip install coverage pytest` (см. [лекцию 5](https://github.com/true-grue/kispython/blob/main/lect5.ipynb)).

<div class="flex-video">
<video width="500" src="https://user-images.githubusercontent.com/6759207/235297961-189a7032-a570-4a46-81a4-d095fa7da661.mp4" autoplay controls loop>
</video>
</div>


```python
class MealyError(Exception):
    pass


class StateMachine:
    def __init__(self):
        self.state = 'A'

    def spin(self):
        if self.state == 'A':
            self.state = 'B'
            return 0
        if self.state == 'C':
            self.state = 'D'
            return 4
        if self.state == 'D':
            self.state = 'E'
            return 5
        if self.state == 'B':
            self.state = 'E'
            return 3
        if self.state == 'E':
            self.state = 'F'
            return 6
        raise MealyError('spin')

    def punch(self):
        if self.state == 'B':
            self.state = 'C'
            return 1
        if self.state == 'E':
            self.state = 'A'
            return 7
        if self.state == 'F':
            self.state = 'G'
            return 9
        raise MealyError('punch')

    def stand(self):
        if self.state == 'B':
            self.state = 'G'
            return 2
        if self.state == 'E':
            self.state = 'G'
            return 8
        raise MealyError('stand')


def main():
    return StateMachine()


def raises(func, error):
    output = None
    try:
        output = func()
    except Exception as e:
        assert type(e) == error
    assert output is None


def test():
    o = main()
    assert o.spin() == 0
    assert o.punch() == 1
    assert o.spin() == 4
    assert o.spin() == 5
    assert o.punch() == 7
    assert o.spin() == 0
    assert o.spin() == 3
    assert o.spin() == 6
    assert o.punch() == 9
    o = main()
    assert o.spin() == 0
    assert o.stand() == 2
    o = main()
    assert o.spin() == 0
    assert o.spin() == 3
    assert o.stand() == 8
    raises(lambda: o.stand(), MealyError)
    raises(lambda: o.punch(), MealyError)
    raises(lambda: o.spin(), MealyError)
```

#### Задача 11

[Условие](https://kispython.ru/docs/10/%D0%98%D0%9D%D0%91%D0%9E-11-21.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-40)

Способ решения 1

```python
from struct import *


FMT = dict(
    char='c',
    int8='b',
    uint8='B',
    int16='h',
    uint16='H',
    int32='i',
    uint32='I',
    int64='q',
    uint64='Q',
    float='f',
    double='d'
)


def parse(buf, offs, ty, order='>'):
    pattern = FMT[ty]
    size = calcsize(pattern)
    value = unpack_from(order + pattern, buf, offs)[0]
    return value, offs + size


def parse_e(buf, offs):
    e1, offs = parse(buf, offs, 'uint8')
    e2_size, offs = parse(buf, offs, 'uint32')
    e2_offs, offs = parse(buf, offs, 'uint16')
    e2 = []
    for _ in range(e2_size):
        val, e2_offs = parse(buf, e2_offs, 'int8')
        e2.append(val)
    e3, offs = parse(buf, offs, 'uint32')
    e4, offs = parse(buf, offs, 'uint8')
    e5, offs = parse(buf, offs, 'uint8')
    e6, offs = parse(buf, offs, 'int64')
    e7, offs = parse(buf, offs, 'int32')
    e8, offs = parse(buf, offs, 'uint64')
    return dict(E1=e1, E2=e2, E3=e3, E4=e4, E5=e5, E6=e6, E7=e7, E8=e8), offs


def parse_d(buf, offs):
    d1, offs = parse(buf, offs, 'float')
    d2, offs = parse(buf, offs, 'uint16')
    return dict(D1=d1, D2=d2), offs


def parse_c(buf, offs):
    c1, offs = parse(buf, offs, 'int8')
    c2, offs = parse(buf, offs, 'uint32')
    c3 = []
    for _ in range(5):
        val, offs = parse(buf, offs, 'char')
        c3.append(val)
    c3 = b''.join(c3).decode('utf-8')
    c4, offs = parse(buf, offs, 'double')
    c5, offs = parse(buf, offs, 'int16')
    return dict(C1=c1, C2=c2, C3=c3, C4=c4, C5=c5), offs


def parse_b(buf, offs):
    c_offset, offs = parse(buf, offs, 'uint16')
    b1, _ = parse_c(buf, c_offset)
    b2, offs = parse(buf, offs, 'int32')
    b3 = []
    for _ in range(3):
        d_offs, offs = parse(buf, offs, 'uint16')
        val, _ = parse_d(buf, d_offs)
        b3.append(val)
    b4_size, offs = parse(buf, offs, 'uint32')
    b4_offset, offs = parse(buf, offs, 'uint16')
    b4 = []
    for _ in range(b4_size):
        val, b4_offset = parse(buf, b4_offset, 'uint16')
        b4.append(val)
    b5, offs = parse(buf, offs, 'double')
    return dict(B1=b1, B2=b2, B3=b3, B4=b4, B5=b5), offs


def parse_a(buf, offs):
    a1, offs = parse(buf, offs, 'int8')
    a2, offs = parse_b(buf, offs)
    a3 = []
    for _ in range(7):
        val, offs = parse(buf, offs, 'uint8')
        a3.append(val)
    a4, offs = parse(buf, offs, 'float')
    a5, offs = parse(buf, offs, 'float')
    a6, offs = parse(buf, offs, 'int16')
    a7, offs = parse(buf, offs, 'uint64')
    a8, offs = parse_e(buf, offs)
    return dict(A1=a1, A2=a2, A3=a3, A4=a4, A5=a5, A6=a6, A7=a7, A8=a8), offs


def main(stream):
    return parse_a(stream, 4)[0]
```

Спопоб решения 2

> Приведенный способ решения вдохновлён типом [BinaryReader](https://docs.microsoft.com/ru-ru/dotnet/api/system.io.binaryreader?view=net-6.0) из стандартной библиотеки .NET.

```python
from struct import unpack_from, calcsize
from typing import Any, Callable


class Types:
    char = 'c'
    int8 = 'b'
    uint8 = 'B'
    int16 = 'h'
    uint16 = 'H'
    int32 = 'i'
    uint32 = 'I'
    int64 = 'q'
    uint64 = 'Q'
    float = 'f'
    double = 'd'


class BinaryReader:
    def __init__(self, stream, offset, order=">"):
        self.stream = stream
        self.offset = offset
        self.order = order

    def jump(self, offset):
        reader = BinaryReader(self.stream, offset, self.order)
        return reader

    def read(self, pattern):
        size = calcsize(pattern)
        data = unpack_from(self.order + pattern, self.stream, self.offset)
        self.offset += size
        return data[0]


def read_e(reader):
    e1 = reader.read(Types.uint8)
    e2_size = reader.read(Types.uint32)
    e2_offset = reader.read(Types.uint16)
    e2_reader = reader.jump(e2_offset)
    e2 = [e2_reader.read(Types.int8) for _ in range(e2_size)]
    e3 = reader.read(Types.uint32)
    e4 = reader.read(Types.uint8)
    e5 = reader.read(Types.uint8)
    e6 = reader.read(Types.int64)
    e7 = reader.read(Types.int32)
    e8 = reader.read(Types.uint64)
    return dict(E1=e1, E2=e2, E3=e3, E4=e4, E5=e5, E6=e6, E7=e7, E8=e8)


def read_d(reader):
    d1 = reader.read(Types.float)
    d2 = reader.read(Types.uint16)
    return dict(D1=d1, D2=d2)


def read_c(reader):
    c1 = reader.read(Types.int8)
    c2 = reader.read(Types.uint32)
    c3 = b''.join([reader.read(Types.char) for _ in range(5)]).decode('utf-8')
    c4 = reader.read(Types.double)
    c5 = reader.read(Types.int16)
    return dict(C1=c1, C2=c2, C3=c3, C4=c4, C5=c5)


def read_b(reader):
    c_offset = reader.read(Types.uint16)
    c_reader = reader.jump(c_offset)
    b1 = read_c(c_reader)
    b2 = reader.read(Types.int32)
    b3 = [read_d(reader.jump(reader.read(Types.uint16))) for _ in range(3)]
    b4_size = reader.read(Types.uint32)
    b4_offset = reader.read(Types.uint16)
    b4_reader = reader.jump(b4_offset)
    b4 = [b4_reader.read(Types.uint16) for _ in range(b4_size)]
    b5 = reader.read(Types.double)
    return dict(B1=b1, B2=b2, B3=b3, B4=b4, B5=b5)


def read_a(reader):
    a1 = reader.read(Types.int8)
    a2 = read_b(reader)
    a3 = [reader.read(Types.uint8) for _ in range(7)]
    a4 = reader.read(Types.float)
    a5 = reader.read(Types.float)
    a6 = reader.read(Types.int16)
    a7 = reader.read(Types.uint64)
    a8 = read_e(reader)
    return dict(A1=a1, A2=a2, A3=a3, A4=a4, A5=a5, A6=a6, A7=a7, A8=a8)


def main(stream):
    return read_a(BinaryReader(stream, 4))
```
