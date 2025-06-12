# Множества 

Всегда отсортированы! (в порядке, в котором заданы)

```
#include <iostream>
#include <set>
 
int main()
{
    std::set<int> numbers;   // пустое множество чисел int
}
```

## Перебор множества
Для перебора множества можно применять циклы for. Например, в стиле for-each:

```
#include <iostream>
#include <set>
 
int main()
{
    std::set<int> numbers{1, 2, 3, 4, 5};
 
    for (int n : numbers)
        std::cout << n << "\t";
    std::cout << std::endl;
}
```

## Удаление элементов
Для удаления из множества применяется функция erase(), в которую передается удаляемый элемент. Кстати, если попытаться удалить элемент, которого во множестве не было, никакой ошибки не будет.

```
#include <iostream>
#include <set>
 
 
int main()
{
    std::set<int> numbers{2, 3, 4, 5};
 
    numbers.erase(1);
    numbers.erase(2);
    numbers.erase(3);
 
    for (int n : numbers)
        std::cout << n << "\t";
    std::cout << std::endl;
}
```

